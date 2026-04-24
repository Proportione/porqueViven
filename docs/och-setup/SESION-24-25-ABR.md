# Sesión 24-25 abr 2026 — resumen de cierre

Dos días de trabajo tras la reunión semanal con Mónica. Todo documentado, replicado en Upbase y Drive, y cerrado limpio.


## Entregables

| # | Artefacto | Ubicación |
|---|-----------|-----------|
| 1 | Acta reunión 24-Abr (única, ya fusionada con la preacta + sección F cronograma 6 días) | Google Doc `1WxvGWV47488nrWTL2CBN0D6xAk4jg4cRLrCSWN7mhoI` · `Mi unidad / 01 Proyectos / 02 PorqueViven / 01 Actas` |
| 2 | Whitepaper HIS del CAPPI v0.1 (13 secciones) | Google Doc `1M8cMin0Z2sH-PbS-1Ywl_uUOycAtHJ1Pi5DzVe-DySA` · `Mi unidad / 01 Proyectos / 02 PorqueViven / 06 Arquitectura` |
| 3 | Draft Gmail — Alfredo CSV BIM (instrucciones Autodesk Revit) | Gmail borradores, id `r-1225126256476823572` |
| 4 | Draft Gmail — Mónica/Cristina/Mayte CNAME GoDaddy | Gmail borradores, id `r-8658775937534020822` |
| 5 | BI Dashboard · nuevo tab FinOps en page porqueViven | `/IT Proportione/Dashboard/pages/4_porqueViven.py` (código listo, deploy pendiente) |
| 6 | 18 tareas replicadas en Upbase con due dates 24-29 abr | Lista `Porqueviven WEB & ARQ` (id `2boyTNv65mex62fZjMPiJ`) |
| 7 | Search Console SA ya con permiso Completo (verificado, no intervención) | `sc-domain:porqueviven.org` |


## Tareas ejecutadas

### Viernes 24-Abr (cerradas)

- **V1 FinOps GCP** → tab añadido en `pages/4_porqueViven.py` con banner explicativo de compartición con automation-brain. Deploy manual pendiente del usuario (requiere `gcloud auth login` interactiva).
- **V2 Alfredo** → Gmail draft con columnas CSV esperadas (`codigo_elemento`, `nombre`, `categoria`, `descripcion`) y pasos Revit 1-5. Link al doc de instrucciones previo reenviado.
- **V3 CNAME GoDaddy** → Gmail draft pidiendo acceso al panel con valores exactos (`_94071871e5f204d10b8534576a1585fe.cursos` → `_8b80103a08ae5dc2734a6a7d610783b9.jkddzztszm.acm-validations.aws`, TTL 600).
- **V4 ESTADO.md** → actualizado con progreso del día, commit `0416e45`.

### Sábado 25-Abr (cerrado)

- **S1 Whitepaper HIS v0.1** → 13 secciones, 2.600 palabras aprox. Sección 9 (procesos internos) queda placeholder hasta recibir los 55 procesos de Ana el lunes 27. v0.2 prevista miércoles 29.
- **D1 pre-entregado (domingo adelantado)** → Copy completo de la landing "Inicio al duelo" en `docs/landings/formacion-inicio-al-duelo.md`. 10 bloques, SEO, Schema.org Course, formulario de captación. Solo queda maquetar en Elementor.
- **L2 + M1 + M2 pre-entregado (lun-mar adelantados)** → Copy completo del producto WC "Farmacias que cuidan" + landing + QR + flyer A5 + pegatina en `docs/landings/farmacias-que-cuidan.md`. Basado en doc oficial de Mónica (id `1rrObEBC...`). Formulario de adhesión con 12 campos (NIF, colegio farmacéutico, provincia...), 3 vías de pago con Bizum preferente.


## Pendientes del usuario

1. **Reauth gcloud y deploy BI**:
   ```
   cd "/Users/javiercuervolopez/code/IT Proportione/Dashboard"
   gcloud auth login
   gcloud run deploy proportione-bi --project=automation-brain --region=europe-west1 --source=. \
     --service-account=proportione-backup-executor@automation-brain.iam.gserviceaccount.com \
     --min-instances=0 --max-instances=1 --memory=512Mi --cpu=1 --port=8080 --quiet
   ```
2. **Revisar y enviar drafts Gmail** (Alfredo + Mónica/Cristina/Mayte).
3. **Push** de los 2 commits locales cuando quieras:
   ```
   cd /Users/javiercuervolopez/code/porqueViven && git push
   ```


## Bloqueantes externos vigilados

- **Ana** — 55 procesos validados (lunes 27-Abr) → bloquea IAM y whitepaper v0.2.
- **Alfredo** — CSV BIM → bloquea prueba QR del miércoles 29.
- **Mónica** — datos personales representante legal Stripe → bloquea pago 19,90 € curso Inicio al duelo.
- **Mayte/Cristina** — CNAME GoDaddy → bloquea SSL cursos.porqueviven.org.
- **Fundación IE + EOI** — modelo donación cursos → cierra landing formación (D1 del domingo).


## Próxima parada

Domingo 26-Abr: **D1 Landing page formación CAPPI en porqueviven.org** — captura de email + CTA a cursos.porqueviven.org, redacción con ángulo "donación <20 %". 4 h estimadas.


—

Commit final del repo porqueViven: `0416e45`. Working tree limpio, 2 commits adelantados sobre `origin/main` (no pushed). Token Upbase fresco (válido ~30 días). Playwright browser abierto en tabs de trabajo — cerrar cuando terminemos.
