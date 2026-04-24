# Google Ads porqueViven — estado 24-abr-2026

Customer ID: `114-832-7525` (porqueViven, Ad Grants)
Revisión: sábado 25-abr tras reuniones Mónica + Talent 24-abr.

## KPIs últimos 7 días (17-abr → 24-abr)

| Métrica | Valor | Observación |
|---------|-------|-------------|
| Gasto | 173,70 € | 24,80 €/día — muy por debajo del objetivo 300 €/día (9 K€/mes) |
| Clicks | 122 | |
| Impressions | 3.126 | |
| Conversions | 3 | |
| CTR | 3,9 % | Bajo del umbral Ad Grant 5 % — **riesgo de elegibilidad** |
| CPC | 1,42 € | |
| CPA | 57,90 € | |

## Campañas que convierten

| Campaña | Conv | Cost | CPA | Comentario |
|---------|------|------|-----|------------|
| `01_Paliativos_Fundacion` | 2 | 16,44 € | 8,22 € | La estrella. Mantener y expandir. |
| `13_Branded_Fundacion` | 1 | 0,62 € | 0,62 € | Branded muy eficiente. Mantener. |

## Campaña que quema sin convertir

| Campaña | Cost | Clicks | Bidding | Problema |
|---------|------|--------|---------|----------|
| `08_Dynamic_Search` | 98,47 € | 68 | TARGET_SPEND | DSA catch-all. Atrae tráfico pero no convierte. Revisar páginas negativas o desactivar en favor de campañas con keyword explícita. |
| `v6_04_Cuidador_Familiar` (PAUSED) | 45,47 € | 9 | MAXIMIZE_CONVERSIONS | Ya pausada. Bajar budget antes de reactivar. |

## Recomendaciones automáticas Google Ads

Solo **2 recomendaciones activas** en el account:

- `RESPONSIVE_SEARCH_AD_IMPROVE_AD_STRENGTH` × 1 — no aplicable vía API (requiere editar el anuncio manualmente).
- `USE_BROAD_MATCH_KEYWORD` × 1 — no aplicar automáticamente (afecta a matching, revisar con criterio).

**Conclusión**: no hay recomendaciones seguras para aplicar en batch. El optimizador de Google no tiene mucho que sugerir — la cuenta está relativamente madura.

## Campañas ya preparadas sin activar (ENABLED pero 0 impresiones 7d)

Preparadas en el plan de escalado del 21-abr, esperando keywords y contenido:

- `14_Diagnostico_Sin_Cura`
- `15_Cuidador_Agotado_Respiro`
- `16_Duelo_Hijo_Fallecido`
- `17_Hermanos_En_La_Sombra`
- `18_Despedirse_Explicar`
- `19_Enfermedades_Concretas`
- `20_Cada_Momento_Recuerdos`
- `21_Profesionales_Sanitarios`
- `22_RSE_Empresa_Solidaria`
- `24_Dr_Ricardo_Martino`
- `25_Psicologia_Duelo_Infantil`
- `26_Curso_Inicio_Duelo` ← alineada con D1 del plan
- `27_FBI_Voluntariado` ← alineada con voluntariado
- `04_Voluntariado_Comunidad`
- `v6_03_Paliativos_Pediatricos`

**Acción recomendada**: completar keywords + RSA de `26` y `27` cuando Talent entregue transcripciones de podcasts (acuerdo #1 acta Talent-FPV 24-abr, fecha prevista 1-may).

## Campañas pausadas que revisar (posible cierre)

Existe un "montón" de campañas PAUSED con 0 gasto y 0 impresiones. Candidatas a archivar por limpieza:

- `https://porqueviven.org/navidad2025/` — claramente obsoleta
- `Concierto solidario` — obsoleta
- `Cada_momento_cuenta`, `Marca genérica`, `CAPPI genérico` — nombres placeholder antiguos
- `FPV - Donacion`, `FPV - Voluntariado`, `FPV - Programas` — deprecadas por las numeradas nuevas
- `Acompañamiento Familiar`, `Cuidados en Casa`, `Qué Hacemos - Programas`, `Colabora con CAPPI`, `Nano y Choco - Cortometraje Solidario`
- `09_Donaciones_Portal`, `10_Galeria_Banderas`, `11_Fila_Cero`, `12_Hazte_Socio` — candidatas a reactivar, no cerrar

**Acción**: no toco masivo sin confirmación. Dejo para la llamada con Ismael del 28-abr + revisión con Talent.

## Siguientes pasos (alineados con plan 6 días)

### M3 (martes 28-abr) — Llamada Ismael
- Preguntar por: subida de pujas sector sanitario, aumento de budget Ad Grant, estado del CPC Waiver.
- Aprovechar para repasar `08_Dynamic_Search` (98 € sin conversiones).

### Cuando lleguen transcripciones podcast (~1-may, acuerdo Talent)
- Extraer 20-30 keywords ancladas a temas concretos.
- Cargar como keywords de exact match en:
  - `26_Curso_Inicio_Duelo`
  - `27_FBI_Voluntariado`
  - Nueva campaña `28_Farmacias_Que_Cuidan` (crear cuando landing de Cristina esté online, martes-miércoles).
  - Nueva campaña `29_Psicologa_Paliativos_Pediatricos` (ángulo sugerido en acta Talent).

### Inmediato (reviso el lunes tras fin de semana)
- Confirmar que CTR no ha caído por debajo de 5 % (cron diario `~/code/porqueViven/scripts/ctr_monitor.py`).
- Si CTR < 5 %, pausar campañas con CTR peor y activar branded exacto.

## No se ha tocado nada en vivo

Esta sesión ha sido diagnóstico + documentación. Los cambios estructurales (pausar DSA, crear #28 y #29, aplicar keywords de podcast) quedan para:
1. La llamada con Ismael (martes).
2. La recepción de transcripciones Talent (viernes próximo).
3. La landing de farmacéuticos online (martes).
