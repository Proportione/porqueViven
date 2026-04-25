# Landing "Inicio al duelo" — deploy 25-abr-2026

## URL pública
`https://porqueviven.org/curso-inicio-duelo/`

## Implementación

Mu-plugin `pv-landing-inicio-duelo.php` (repo `porqueviven-wp-muplugins`, commit `ca28138`).

- Registra el shortcode `[pv_landing_inicio_duelo]`.
- El post 22868 contiene **únicamente** el shortcode (todo el HTML vive en el plugin, versionado en git).
- 10 secciones: hero, público objetivo (4 cards), contenido (6 checks + 4 lecciones numeradas), entregables (3 cards), marco fiscal, CAPPI + Ricardo Martino, testimonio, FAQ acordeón, CTA final, captación de leads.
- CSS scoped con prefijo `.pvlid` (no contamina otras páginas).
- Schema.org Course JSON-LD inyectado en `<head>` solo en `is_page(22868)`.
- H1 del theme oculto (`.entry-title { display:none }` con scope `.page-id-22868`) para evitar doble H1.
- Reutiliza `[pv_interest_form list="curso-duelo"]` de `pv-interest-forms.php` (lista Acumba **1285114**).
- Branding: `#0C4DA2` / `#770E75` / Lato.

## Backup

Contenido anterior del post 22868 guardado en prod: `siteground-porqueviven:/tmp/post_22868_backup_20260425_190736.txt`.

Restaurar:
```bash
ssh siteground-porqueviven "cd /home/customer/www/porqueviven.org/public_html && wp post update 22868 --post_content=\"\$(cat /tmp/post_22868_backup_20260425_190736.txt)\""
```

## Verificación visual

Screenshot: `~/code/porqueViven/.playwright-mcp/landing-inicio-duelo-fullpage.png` (full page) + `landing-inicio-duelo-hero.png` (viewport hero).

## Estado actual del CTA

Los CTAs primario y final apuntan a `https://cursos.porqueviven.org/course/inicio-al-duelo`. **Esa URL no resuelve todavía** (ver bloqueos abajo). El CTA secundario (`#quiero-saber-mas`) sí funciona y captura leads en Acumba.

## Bloqueos para lanzamiento end-to-end (campañas con conversión)

Tres bloqueos en serie antes de poder llevar tráfico Ads al checkout completo del curso:

| # | Bloqueo | Quién | Lead time |
|---|---------|-------|-----------|
| 1 | **Stripe OAuth en OCH** — bloqueado por datos personales del representante legal (Mónica: DNI, fecha nac., domicilio) | Mónica | inmediato cuando facilite datos |
| 2 | **CNAME en GoDaddy** para `_94071871e5f204d10b8534576a1585fe.cursos` → `_8b80103a08ae5dc2734a6a7d610783b9.jkddzztszm.acm-validations.aws`. Los NS de `porqueviven.org` son de GoDaddy, no SiteGround. | Mayte/Cristina con acceso GoDaddy | propagación AWS 15-30 min |
| 3 | **Publicar los 2 cursos en OCH** (ahora "Inicio al duelo" + "Formación Básica de Voluntariado" están en Draft) | proportione@porqueviven.org (Website Admin) | un click |

Detalle completo: `docs/och-setup/ESTADO.md`.

## Qué se puede lanzar HOY (sin esperar bloqueos)

**Campañas de captación de leads, no de venta.** El formulario del bloque 10 (`#quiero-saber-mas`) escribe a Acumba lista 1285114 y funciona. Permite:

- Reactivar `26_Curso_Inicio_Duelo` (€30/d, MAXIMIZE_CONVERSIONS, RARELY_SERVED por PHRASE long-tail) → cambiar CTA del anuncio a "Apúntate al lanzamiento" en lugar de "Empezar el curso".
- Reactivar `27_FBI_Voluntariado` (€30/d, mismo estado) — la landing equivalente `/formacion-basica-voluntariado/` (post 22869) sigue siendo HTML simple, pendiente maquetar igual.
- Conversion action a usar mientras tanto: `Newsletter_Signup` (AW-11167646206/Ndz-CJTntf8bEP6Dk80p, valor 5 €) o crear una específica `Curso_Lead`.

**Riesgo en mantener CTA actual**: si se lanza Ads con el CTA primario "Empezar ahora" llevando a `cursos.porqueviven.org/course/inicio-al-duelo`, el clic devuelve error de DNS (la URL no resuelve). Pésima UX y desperdicio de presupuesto. Solución temporal: editar el mu-plugin para que ambos CTAs apunten a `#quiero-saber-mas` hasta desbloquear los 3 puntos.

## Pendientes de cara al curso publicado

- Reemplazar testimonio genérico (Elena/Carlos) por cita real de las grabaciones de Mónica.
- Confirmar foto de Ricardo Martino con Cristina.
- Validar bloque 5 (donativo) con Jara + modelo Fundación IE/EOI.
- Maquetar `/formacion-basica-voluntariado/` (post 22869) con el mismo enfoque (mu-plugin + shortcode).
