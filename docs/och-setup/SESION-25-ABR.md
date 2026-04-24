# Sesión 25 abr 2026 — resumen de cierre

Sábado largo: cierre del plan 6 días, acta Talent Class, whitepaper HIS, copy de las dos landings, diagnóstico Ads.


## Entregables del día

| # | Artefacto | Dónde |
|---|-----------|-------|
| 1 | Acta reunión **FPV–Talent–Proportione 24-Abr** (fusionada con transcripción Gemini + contexto de actas Mónica y Cristina) | Drive `1P4MamWElPvJnD223-KonTGK-6wLgLt_BpgT7fgi04Is` · carpeta `01 Actas PorqueViven` |
| 2 | Sección F · Cronograma 6 días (24-29 abr) añadida al acta Mónica | Drive `1WxvGWV47488nrWTL2CBN0D6xAk4jg4cRLrCSWN7mhoI` |
| 3 | **Whitepaper HIS del CAPPI v0.1** (13 secciones, 2.600 palabras) | Drive `1M8cMin0Z2sH-PbS-1Ywl_uUOycAtHJ1Pi5DzVe-DySA` · carpeta `06 Arquitectura` |
| 4 | Copy landing **Inicio al duelo** (10 bloques, SEO, Schema Course, formulario) | `docs/landings/formacion-inicio-al-duelo.md` |
| 5 | Copy producto WC + landing **Farmacias que cuidan** + QR + flyer + pegatina | `docs/landings/farmacias-que-cuidan.md` |
| 6 | Diagnóstico Google Ads 24-abr (KPIs 7d, recomendaciones, plan) | `docs/ads/estado-24-abr.md` |
| 7 | 18 tareas Upbase creadas + prioridades normalizadas | Upbase lista `Porqueviven WEB & ARQ` (id `2boyTNv65mex62fZjMPiJ`) |
| 8 | 3 drafts Gmail a `soporte@porqueviven.org` (Mónica Stripe, Cristina CNAME+marca+WhatsApp, Alfredo BIM CSV) | Gmail borradores |
| 9 | Tab **FinOps** en BI dashboard `bi.proportione.com/porqueViven` | `/IT Proportione/Dashboard/pages/4_porqueViven.py` (deploy pendiente) |


## Tareas ejecutadas

### Mañana — consolidación plan 6 días
- Sección F del acta Mónica (Gantt textual + dependencias + bloqueos externos).
- 18 tareas Upbase con due dates 24-29 abr.
- Diagnóstico 6 días con bloqueantes y buffer.

### Mediodía — reunión Talent Class + acta
- Captura Meet + cruce con convocatoria Calendar → identificación de asistentes (corrección "Grañado" → Chapado, "Jorge Bl..." → Yago Barca).
- Transcripción Gemini recibida por email → fusionada con contexto previo.
- Acta cerrada con 10 temas tratados, 10 acuerdos, 5 decisiones estructurales.
- 7 tareas de seguimiento creadas en Upbase.
- Memoria `project_reunion_talent_20260424.md` con equipo + decisiones.

### Tarde — whitepaper HIS + landings + Ads
- Whitepaper HIS v0.1 redactado (viabilidad GCP, arquitectura 4 capas, roadmap MVP→v1→v2, seguridad RGPD, integraciones, coste estimado 60-80 K€ MVP). Sección 9 (procesos internos) placeholder hasta lunes con los 55 procesos de Ana.
- Copy completo landing formación — pegable en Elementor.
- Copy completo producto farmacéuticos — WC skeleton + landing + QR + flyer A5 + pegatina Ø80 mm.
- Diagnóstico Ads 24-abr: gasto 173,70 €/7d (obj 300 €/día), CTR 3,9 % (riesgo Ad Grant), estrella `01_Paliativos_Fundacion` CPA 8,22 €, solo 2 recomendaciones automáticas (ninguna aplicable batch).

### Noche — cierre del día (auto-mode continuo)
- Push de 5 commits locales a `origin/main`.
- Task tracker Upbase: 5 tareas V+S marcadas completadas.
- 3 drafts Gmail internos creados para ingesta automática a tickets Firestore.
- Diagnóstico Ads y plan para 28-abr (Ismael) + 1-may (transcripciones Talent).


## Pendientes del usuario

1. **Enviar 3 drafts Gmail** a `soporte@porqueviven.org` (cron ingesta crea tickets automáticamente en <15 min).
2. **Deploy BI dashboard** para activar el tab FinOps:
   ```
   cd "/Users/javiercuervolopez/code/IT Proportione/Dashboard"
   gcloud run deploy proportione-bi --project=automation-brain --region=europe-west1 --source=. \
     --service-account=proportione-backup-executor@automation-brain.iam.gserviceaccount.com \
     --min-instances=0 --max-instances=1 --memory=512Mi --cpu=1 --port=8080 --quiet
   ```
3. **Revisar 2 drafts Gmail** pendientes (Alfredo, CNAME GoDaddy) — enviar directamente a sus destinatarios.


## Bloqueantes externos vigilados

- **Ana** — 55 procesos validados (lunes 27) → bloquea IAM [L1] y whitepaper v0.2 [X2].
- **Alfredo / EPCM** — CSV BIM → bloquea prueba QR [X1] miércoles.
- **Mónica** — datos representante legal Stripe → bloquea activación pagos 19,90 € curso Inicio al duelo.
- **Mayte / Cristina** — CNAME en GoDaddy → bloquea SSL cursos.porqueviven.org.
- **Clara + Yago (Talent)** — transcripciones podcast → bloquea extracción de keywords para Ad Grants.
- **Cristina** — manual de marca + grupo WhatsApp Talent.
- **Fundación IE + EOI** — modelo donación cursos (normativa <20 %) → afina landing formación.


## Próxima parada (domingo 26-abr)

**D1** · Maquetar en Elementor la landing de formación "Inicio al duelo" usando el copy ya preparado. ~90 min.
Después: nada más hasta que lleguen inputs externos. El lunes se reactiva con los procesos de Ana y el producto farmacéuticos.


## Estado del repo porqueViven

```
commits locales vs origin/main:  0  (todo pusheado hasta 7d268b0)
working tree:  limpio
branch activa:  main
```


## Consolidado tareas tracker (25-abr 23:00)

- **Completadas hoy:** 12 tareas
- **En progreso:** #5 (CNAME), #24 (landing formación)
- **Pendientes con bloqueo externo:** #2 (Stripe), #19 (farmacéuticos — inicio lunes), #20 (IAM — lunes), #23 (BIM — Alfredo)


— Sesión cerrada limpia. Good night.
