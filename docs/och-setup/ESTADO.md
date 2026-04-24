# OCH cursos.porqueviven.org — estado final 23-abr-2026 23:40h

## URLs

- Tenant OCH: https://cursos-porqueviven.onlinecoursehost.com
- Dominio custom solicitado: https://cursos.porqueviven.org (pendiente SSL ACM, DNS propagando)
- Curso 1 admin: https://cursos-porqueviven.onlinecoursehost.com/edit-courses/LcLD8K5KvHiJPFjxbMUX/edit
- Curso 2 admin: https://cursos-porqueviven.onlinecoursehost.com/edit-courses/BYm2VmRhZnhNssYw9kAK/edit

## Tareas completadas

| # | Tarea | Estado |
|---|-------|--------|
| 1 | Admin `proportione@porqueviven.org` (Website Admin) + support email | ✅ |
| 3 | Curso 1 **"Inicio al duelo"** (19,90€ donativo) + 4 lecciones con vídeos porqueViven | ✅ |
| 4 | Curso 2 **"Formación Básica de Voluntariado"** (gratis) + Lección Ricardo Martino | ✅ |
| 6 | 3 plantillas email en español (Welcome, Completion, Invited) con firma porqueViven | ✅ |
| 7 | Certificado participación en español con firma institucional CIF G86801099 | ✅ |
| 8 | QA + 53 capturas | ✅ |
| 9 | Custom CSS "Pagar → Donar" en Branding | ✅ |
| 10 | Logo cabecera blanco + portadas cursos | ✅ |
| 11 | Cursos renombrados según acta 17-Abr | ✅ |
| 12 | **Home Page** custom: header, 3 benefits, CTA, FAQ todo en porqueViven | ✅ |
| 13 | **Landing pages** completas: 6 features + long description + 6 FAQs por curso | ✅ |
| 14 | Más lecciones Curso 1 (4 lecciones con vídeos YouTube porqueViven) | ✅ |
| 15 | Author "Fundación porqueViven" + 2 categorías ("Duelo y pérdida", "Voluntariado porqueViven") | ✅ |

## Tareas con bloqueos externos

| # | Tarea | Bloqueo |
|---|-------|---------|
| 2 | Stripe OAuth | Representante legal requiere datos de Mónica (DNI, fecha nac., domicilio). User pidió no avanzar |
| 5 | SSL ACM cursos.porqueviven.org | DNS propagando. CNAME creado. Esperar propagación AWS |

## Setup completo

### Tenant OCH
- Academy "Cursos porqueViven" con lifetime AppSumo aplicado (1 código redimido, queda 1)
- Idioma español · Europe/Madrid · Moneda EUR cuando Stripe esté OAuth
- Onboarding completo

### Branding porqueViven
- Primary `#0C4DA2` · Accent `#770E75` · Footer `#2D2D2D` · Lato
- Logo horizontal porqueViven FUNDACIÓN en top menu, footer, login y OG image
- Favicon porqueViven SVG→PNG 256×256
- Custom CSS con reglas de sustitución "Pagar/Pay Now/Buy Now" → "Donar ahora / Confirmar donativo"

### Admin y accesos
- Owner login Google: javier.cuervo@proportione.com (readonly)
- **Admin invitado con rol Website Admin**: `proportione@porqueviven.org` (email reset enviado)
- Support email: `proportione@porqueviven.org`

### Redes sociales (en footer + share bar)
- Facebook, X, Instagram, YouTube, LinkedIn — todas apuntando a los perfiles oficiales porqueViven

### Curso 1 "Inicio al duelo" (19,90€ donativo)
- Estado: Draft
- Landing page completa: 6 features + long description (5 bloques) + 6 FAQs
- 4 lecciones con vídeos:
  - L1 "Bienvenida — Qué es porqueViven" (vídeo `2lvSH55uPrE`)
  - L2 "Comprender lo que vive una familia" (vídeo `k4cSkEM8N30`)
  - L3 "No estábamos solos — un testimonio" (vídeo `b3hNAroY59Y`)
  - L4 "Construir una red para cuidar" (vídeo `h2YwkXguXgs` + ejercicio reflexivo)
- Portada: `ninia_valores2-1.jpg` (de porqueviven.org)
- Autor: Fundación porqueViven · Categoría: Duelo y pérdida
- Certificado configurado

### Curso 2 "Formación Básica de Voluntariado" (gratis)
- Estado: Draft
- Landing page completa: 6 features + long description (5 bloques) + 6 FAQs
- Lección "Ensanchar la vida — bienvenida al voluntariado" con 3 vídeos Ricardo Martino: `B8jTo-7Smrw` + `PRYBypKDuIE` + `X90bgNrMyes`
- Portada: thumbnail YouTube B8jTo-7Smrw (Ricardo Martino)
- Autor: Fundación porqueViven · Categoría: Voluntariado porqueViven

### Home Page (Page Builder)
- Header: Pretitle "Fundación porqueViven" · Title "Acompañar también se aprende" · Subtitle + Button Sub Text
- Benefits: 3 items porqueViven (Humano antes que teórico · Corto y en español · Útil para la vida real)
- Call To Action: "Empezamos por lo esencial — Dos cursos, dos puertas de entrada"
- FAQ: 4 preguntas porqueViven (precios · formación previa · duración · certificado)
- Secciones template genéricas eliminadas: Testimonial, Highlighted Box, Newsletter

### Autorías y categorías
- **Author**: "Fundación porqueViven" — Cuidados Paliativos Pediátricos · Madrid, con descripción Ricardo Martino/CAPPI
- **Category 1**: "Duelo y pérdida" → Curso 1
- **Category 2**: "Voluntariado porqueViven" → Curso 2

### Email templates (español + firma porqueViven)
- Default Course Welcome: "Bienvenida al curso: {{courseTitle}}"
- Default Course Completion: "Has completado el curso: {{courseTitle}}"
- Manually Invited Student Welcome: "Te invitamos al curso: {{courseTitle}}"

### Certificado de participación
- Título: "Certificado de participación"
- Textos traducidos: Se entrega a · Por haber completado la formación · Emitido el · Válido hasta · ID de certificado
- Nota: "…impartida por la Fundación porqueViven. Se emite con fines de reconocimiento, no sustituye a una titulación oficial. CIF G86801099 · porqueviven.org"

### Dominio custom — BLOQUEADO por ubicación del DNS
- `cursos.porqueviven.org` solicitado en OCH (AWS ACM)
- **Issue encontrado 24-Abr 05:00h**: Los NS autoritativos de `porqueviven.org` son de **GoDaddy** (`ns51.domaincontrol.com`, `ns52.domaincontrol.com`), NO de SiteGround.
- El CNAME creado en SiteGround Zone Editor no tiene efecto porque GoDaddy es quien responde las consultas públicas.
- **Acción pendiente (usuario)**: añadir el CNAME en panel de GoDaddy DNS:
  - Tipo: `CNAME`
  - Host/Subdominio: `_94071871e5f204d10b8534576a1585fe.cursos`
  - Value: `_8b80103a08ae5dc2734a6a7d610783b9.jkddzztszm.acm-validations.aws`
  - TTL: 600s (el mínimo que GoDaddy permite)
- Tras propagar (~15-30 min), volver a `https://cursos-porqueviven.onlinecoursehost.com/admin/settings/request-custom-domain` y pulsar "Check Certificate". OCH entonces emite el CNAME tráfico que también hay que añadir en GoDaddy.

## Pendientes manuales usuario

1. **Stripe onboarding** (paso representante legal en el tab Stripe): requiere datos personales de Mónica (DNI, fecha nacimiento, domicilio). Desbloquea:
   - Precio 19,90€ en Curso 1
   - Moneda EUR en settings
2. **Dominio custom — CNAME en GoDaddy**: los NS de porqueviven.org son de GoDaddy (`ns51.domaincontrol.com`), no SiteGround. Entrar al panel DNS de GoDaddy y añadir:
   - Tipo CNAME · Host `_94071871e5f204d10b8534576a1585fe.cursos` · Value `_8b80103a08ae5dc2734a6a7d610783b9.jkddzztszm.acm-validations.aws` · TTL 600
   - Tras propagación, pulsar "Check Certificate" en OCH. Se emitirá el 2º CNAME tráfico para apuntar `cursos.porqueviven.org` a CloudFront.
3. **Email reset** en bandeja `proportione@porqueviven.org` para completar login como Website Admin
4. **Publish** cursos y Home cuando Mónica dé el OK (ahora están en Draft — por eso `/course/inicio-al-duelo` devuelve 404 a público, es comportamiento esperado)
5. **Para demostrar a Mónica**: entrar con javier.cuervo@proportione.com (owner) → /courses → Admin ve los 2 cursos. O compartir enlaces de la home pública: `https://cursos-porqueviven.onlinecoursehost.com/home`

## Capturas (9 en `~/code/porqueViven/docs/och-setup/captures/`)

1. `00-appsumo-codigos-disponibles.png`
2. `01-create-academy-filled.png`
3. `02-tenant-creado-lifetime.png`
4. `03-branding-colores-fuente.png`
5. `04-branding-con-logos.png`
6. `05-admin-cursos-listado.png`
7. `06-home-publica.png`
8. `07-cursos-publica.png`
9. `08-certificado-porqueviven.png`
10. `09-cursos-final-2-cursos.png` — **la imagen estrella para la reunión Mónica**: 2 cursos visibles en la plataforma con branding completo

## Decisiones tomadas en ruta

- **Industria onboarding**: "Non-Profit/NGO & Governmental" (vs "Personal development" de bizi) — más identitario de una fundación
- **Nombre del tenant**: "Cursos porqueViven" (consistente con dominio `cursos.porqueviven.org` y con `cursos.institutoteologia.org`)
- **Precio píldora duelo**: 19,90 € donativo (del 20€ acordado 27-Mar, ajustado a 19,90 por petición usuario)
- **SECPAL**: piloto gratis, contenido expandible cuando SECPAL confirme catálogo
- **CTA lenguaje**: "Donar ahora / Confirmar donativo" en vez de "Pagar" por naturaleza fundación
