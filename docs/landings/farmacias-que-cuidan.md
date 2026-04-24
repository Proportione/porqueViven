# Producto + Landing: Farmacias que cuidan — porqueviven.org

Fuente: doc compartido por Mónica (ID `1rrObEBCO4bpOX6D2KdVsnvI53Y5gy_U1`).
Objetivo: canal de captación para las 22.000 farmacias de España (donativo 100 €/año al CAPPI) con QR impreso en folletos que Cristina distribuye vía colegios farmacéuticos y mayoristas.
Preferencia de pago Mónica: **Bizum / transferencia** para eliminar comisiones Stripe. Stripe como fallback.

Estado: BORRADOR v0.1 para lunes 27 (skeleton WC) + martes 28 (landing + QR + formulario persona jurídica).

---

## 1 · Producto WooCommerce

| Campo | Valor |
|-------|-------|
| Nombre | Farmacias que cuidan — donativo anual CAPPI |
| Slug | `farmacias-que-cuidan-100e` |
| Tipo | Producto simple |
| Precio | 100,00 € (fijo, no modificable por el usuario) |
| Categoría | Donativos colaboradores |
| Etiqueta | farmacias, CAPPI, anual, jurídico |
| SKU | DON-FARM-100 |
| Visibilidad catálogo | Oculto en búsqueda general (solo accesible desde la landing + QR) |
| Imagen destacada | Pegatina "Farmacia que cuida" (vista 1:1) |
| Imagen galería | 2ª: render CAPPI; 3ª: niño acompañado |
| Descripción corta | Tu farmacia se suma a la red nacional que acompaña a niños con enfermedades graves. Donativo anual de 100 € al CAPPI de la Fundación porqueViven. |
| Descripción larga | Ver bloque "Descripción larga del producto" más abajo. |
| Campos custom (metadata) | - `tipo_donante`: farmacia / colegio farmacéutico / mayorista<br>- `nif`: NIF o CIF (required)<br>- `nombre_comercial`: (required)<br>- `colegio_oficial`: en qué colegio está colegiada<br>- `num_colegiado`: número de farmacéutico colegiado (opcional)<br>- `provincia`: dropdown |
| Métodos de pago habilitados | Bizum (preferente, destacado primero) → transferencia → Stripe (último) |
| Post-compra | Pantalla con: código QR/enlace para la pegatina descargable, acceso a material, agradecimiento firmado Mónica. Email automático con certificado fiscal (Holded) en 7 días. |

### 1.1 · Descripción larga del producto (pegar en WC)

**La farmacia como espacio de cuidado**

Cada día, miles de personas pasan por su farmacia en momentos vinculados a la salud, al cuidado, a la vulnerabilidad. Es uno de los espacios de mayor confianza en el barrio.

Ese entorno convierte a las farmacias en un canal único para conectar con la misión de la Fundación porqueViven y con el proyecto **CAPPI — Centro de Atención Paliativa Pediátrica Integral**, primer centro en España especializado en el cuidado de niños con enfermedades graves o incurables y sus familias.

**Qué incluye tu adhesión**

- Formar parte de la **red nacional "Farmacias que cuidan"**, con tu farmacia identificada en porqueviven.org.
- **Kit físico**: pegatina identificativa para el escaparate + tarjetas informativas para clientes.
- **Apoyo en comunicación**: materiales listos para RRSS, dossier para el equipo de la farmacia, nota de prensa local si la pides.
- **Certificado fiscal** de donación a entidad sin ánimo de lucro (deducción del 80 % sobre los primeros 250 € en España, Ley 49/2002).
- **Informe anual de impacto**: a qué familias ha llegado tu aportación.

**Cómo se usa el dinero**

El 100 % del donativo se destina al CAPPI: atención domiciliaria gratuita, equipo multidisciplinar (medicina, enfermería, psicología, trabajo social, voluntariado), acompañamiento durante y después de la enfermedad. Sin intermediarios, sin comisiones de gestión sobre esta aportación.

**Paga como prefieras**

Bizum o transferencia a la cuenta de la Fundación (preferente, sin comisiones). Si lo prefieres, también hay tarjeta.

---

## 2 · Landing page

Destino: `https://porqueviven.org/farmacias-que-cuidan/`
Tono: institucional-cálido, orientado a farmacéutico/a titular que quiere tomar una decisión en 2 minutos tras escanear el QR del folleto.
Schema: Organization + DonateAction + Place (para localización de farmacias adheridas).

### 2.1 · Estructura visual

1. Hero (claim + CTA primario + pegatina de ejemplo)
2. Qué es Farmacias que cuidan
3. Cómo funciona (3 pasos)
4. Dos niveles de participación
5. Qué incluye tu adhesión
6. Qué aporta a tu farmacia
7. Testimonio (Rocío, farmacéutica piloto)
8. FAQ
9. Formulario de adhesión (CTA largo)
10. Mapa de farmacias ya adheridas (progresivo)

### 2.2 · Copy por bloque

#### Bloque 1 — Hero

**H1:** Farmacias que cuidan.
**H2 (sub):** Tu farmacia, en la red nacional que acompaña a niños con enfermedades graves y a sus familias.

**Bullets sobre CTA:**
- Adhesión anual: 100 € al CAPPI
- Kit físico + apoyo en comunicación
- Certificado fiscal (deducción del 80 %)
- Bizum, transferencia o tarjeta

**CTA primario:** _Adherir mi farmacia_ → ancla a #adherir
**CTA secundario:** _Me interesa, que me llamen_ → ancla al formulario de interés

**Visual hero:** pegatina "Farmacia que cuida" sobre mockup de escaparate + logo porqueViven Fundación. Alt: "Pegatina identificativa del programa Farmacias que cuidan de la Fundación porqueViven".

#### Bloque 2 — Qué es

**H2:** Qué es Farmacias que cuidan

**P:** Un programa que crea una **red nacional de farmacias comprometidas** con el cuidado de niños y familias que atraviesan una enfermedad grave. Las farmacias adheridas colaboran con el desarrollo del CAPPI, primer centro español especializado en cuidados paliativos pediátricos integrales, impulsado por la Fundación porqueViven.

**P:** No es un programa de marketing. Es una red discreta que identifica a tu farmacia como un espacio que entiende el cuidado —todo el cuidado, también el de las familias que no tienen cura a la vista.

#### Bloque 3 — Cómo funciona

**H2:** En 3 pasos

**Grid 3 columnas con iconos:**

| Paso | Título | Descripción |
|------|--------|-------------|
| 1 | Te adhieres | Rellenas el formulario en 90 segundos y haces el donativo anual de 100 € por Bizum, transferencia o tarjeta. |
| 2 | Recibes el kit | Pegatina identificativa para el escaparate, tarjetas informativas para tus clientes, y materiales de comunicación. |
| 3 | Acompañas | Tu farmacia aparece en el mapa nacional, recibe el informe anual de impacto, y ofrece a sus clientes una vía sencilla de ayudar. |

#### Bloque 4 — Dos niveles de participación

**H2:** Dos formas de estar

**Card 1: Compromiso de la farmacia**
- Aportación anual de 100 € al CAPPI.
- Formar parte de la red nacional.
- Visibilizar tu compromiso con el cuidado.

**Card 2: Participación de los clientes (opcional)**
- Opción de **redondeo en caja** hacia el CAPPI.
- Tarjetas informativas junto al mostrador.
- Acceso al proyecto del CAPPI con un QR en tu vitrina.

#### Bloque 5 — Qué incluye tu adhesión

**H2:** Qué te llevas

**Grid de 4 elementos:**

| Icono | Título | Descripción |
|-------|--------|-------------|
| 🏷️ | Pegatina identificativa | Para el escaparate. Diseño sobrio, reconocible a nivel nacional. |
| 📄 | Tarjetas informativas | Para tu mostrador, con un QR al proyecto CAPPI. |
| 📣 | Apoyo en comunicación | RRSS preparadas, dossier para tu equipo, nota de prensa local. |
| 🧾 | Certificado fiscal | Automático, en enero. Deducción del 80 % (Ley 49/2002). |

#### Bloque 6 — Qué aporta a tu farmacia

**H2:** Por qué adherirte

**Lista:**
- Formar parte de un proyecto de **alto impacto social** medible.
- Reforzar el compromiso de tu farmacia con la comunidad.
- Ofrecer a tus clientes una forma sencilla y creíble de ayudar.
- Diferenciarte como farmacia comprometida en un sector competitivo.

#### Bloque 7 — Testimonio

> "Cuando la Fundación me explicó el proyecto del CAPPI y cómo podíamos conectarlo con la farmacia de barrio, vi clarísimo que teníamos que estar. Mis clientes me preguntan por la pegatina, y me permite hablar de algo importante con gente a la que ya conozco."
>
> — Rocío, farmacéutica · Madrid · farmacia piloto de la red

(Nota: usar cita real de Rocío tras la reunión. Si aún no está grabada, sustituir por texto institucional.)

#### Bloque 8 — FAQ

**H2:** Preguntas frecuentes

**Acordeón (7 items):**

**¿Cuánto cuesta?**
100 € al año, como donativo íntegro al CAPPI. Sin comisiones para la farmacia.

**¿Tengo que recaudar yo de mis clientes?**
No. El donativo lo aporta la farmacia. Si además quieres ofrecer redondeo a tus clientes, te damos el material; si no, tu adhesión ya está cubierta.

**¿Qué formas de pago aceptáis?**
Bizum (preferente), transferencia bancaria o tarjeta. Si haces Bizum o transferencia, el 100 % llega sin comisiones.

**¿Me podéis emitir factura en lugar de certificado de donación?**
Las adhesiones se registran como donación a entidad sin ánimo de lucro. El certificado fiscal permite la deducción aplicable a personas jurídicas según la Ley 49/2002 (35 % con límite 10 % base imponible). Si tu asesor necesita un formato concreto, escríbenos.

**¿La pegatina es obligatoria?**
No. Te la enviamos por si quieres ponerla. Algunas farmacias prefieren tenerla dentro, otras en escaparate, otras no ponerla. Es tuya.

**¿Puedo renovar al año siguiente?**
Sí. En el décimo mes te avisamos y te facilitamos la renovación con un clic. Si quieres automatizar (domiciliación), también.

**¿Puedo hacer una aportación mayor?**
Por supuesto. Contacta con nosotros en [info@porqueviven.org](mailto:info@porqueviven.org) y te explicamos las opciones de colaboración estructural (patrocinio anual, proyectos concretos, nominación de salas del CAPPI).

#### Bloque 9 — Formulario de adhesión

**H2 (anclado en #adherir):** Sumar tu farmacia

**Texto corto:** 90 segundos. 100 €. Kit en casa en una semana.

**Formulario:**
- **Nombre comercial de la farmacia** (text, required)
- **NIF/CIF** (text, required, validación formato)
- **Colegio oficial** (dropdown — listado de colegios oficiales de farmacéuticos de España)
- **Nº colegiado** (text, opcional)
- **Provincia** (dropdown)
- **Dirección postal de envío del kit** (text, required)
- **Email de contacto** (email, required)
- **Teléfono** (tel, required)
- **Persona de contacto** (text, required)
- **¿Cómo te llegó Farmacias que cuidan?** (dropdown: folleto en farmacia, colegio farmacéutico, mayorista de medicamentos, RRSS, otros)
- **Método de pago** (radio: Bizum / Transferencia / Tarjeta) — selección por defecto: Bizum
- ☐ He leído y acepto la [política de privacidad](https://porqueviven.org/politica-de-privacidad/)
- ☐ Autorizo a porqueViven a incluir mi farmacia en el mapa nacional de farmacias adheridas (opcional)
- **Botón:** Adherirme · 100 €

**Tras envío:**
- **Si Bizum:** pantalla con número `13336` (oficial porqueViven) + botón "Ya lo he hecho" con email auto-confirm.
- **Si transferencia:** pantalla con IBAN `ES90 0049 1421 6025 1002 8397` + concepto sugerido `FARMACIAS-CUIDAN-<NIF>` + botón "Ya lo he enviado".
- **Si tarjeta:** checkout Stripe estándar.

#### Bloque 10 — Mapa de farmacias adheridas

**H2:** Farmacias que ya están en la red

**Widget:** mapa de España (Leaflet + OpenStreetMap) con pins de cada farmacia adherida que haya dado su consentimiento. Contador dinámico arriba: "X farmacias cuidando en Y provincias".

(Inicialmente estará vacío o con la farmacia piloto de Rocío. Crecerá con cada adhesión.)

---

## 3 · QR + folleto (entregable físico)

### 3.1 · QR code

- **URL destino:** `https://porqueviven.org/farmacias-que-cuidan/?utm_source=folleto&utm_medium=qr&utm_campaign=farmacias_cuidan_2026`
- **Formato:** PNG transparente 800×800 px + SVG vectorial
- **Colores:** cuadros #0C4DA2 (azul porqueViven), fondo blanco
- **Logo en centro:** logo compacto porqueViven (30 % del área central, sin romper legibilidad)
- **Nivel de corrección:** H (alto, para imprenta con posibles pliegues)
- **Test offline antes de imprimir:** lector de tres móviles distintos desde 20 cm de distancia

### 3.2 · Flyer / folleto

A5, una cara.

**Estructura:**
- Arriba: logo porqueViven FUNDACIÓN (a la izquierda)
- H1: "Tu farmacia, en la red que cuida."
- Subtítulo 2-3 líneas
- 3 iconos con sus 3 pasos
- Línea separadora
- QR grande (40 mm × 40 mm mínimo) con leyenda "Escanea y adhiérete en 90 segundos"
- URL acortada legible: `porqueviven.org/farmacias-que-cuidan`
- Pie: "Fundación porqueViven · CIF G86801099 · porqueviven.org"

Ver archivo de diseño pendiente en `docs/landings/assets/flyer-farmacias.md`.

### 3.3 · Pegatina

Circular Ø 80 mm.

**Diseño:**
- Fondo azul porqueViven (#0C4DA2)
- Texto blanco en dos líneas: "FARMACIA" (pequeño arriba) · "QUE CUIDA" (grande)
- Mini-logo porqueViven abajo
- Borde blanco fino

---

## 4 · Integraciones técnicas

| Componente | Integración | Notas |
|-----------|-------------|-------|
| Formulario de adhesión | HubSpot (mismo endpoint que las donaciones actuales) | Nueva lista: "Farmacias colaboradoras". Crear campo custom "NIF" si no existe. |
| Bizum | Captación manual (pantalla con `13336`) + reconciliación con extracto bancario | Plantear automatización con API bancaria más adelante. |
| Transferencia | IBAN mostrado + email auto-confirm al marcar "Ya lo he enviado" | Conciliación manual semanal. |
| Tarjeta | Stripe Connected Account existente | Producto WC como fallback, no preferente. |
| Certificado fiscal | Holded — generación automática en enero | Pendiente acuerdo #10 del acta (consulta Jara). |
| Mapa | Leaflet + JSON con geocodings de farmacias adheridas | Dato cargado desde API interna (nuevo endpoint `/wp-json/porqueviven/v1/farmacias-mapa`). |

---

## 5 · Check-list de entrega

### Lunes 27-Abr (L2 skeleton)
- [ ] Producto WC creado en estado Draft con SKU DON-FARM-100.
- [ ] Categoría "Donativos colaboradores" creada.
- [ ] Slug del producto confirmado.
- [ ] Campos custom (NIF, colegio, etc.) definidos en el perfil del producto o en el formulario externo.

### Martes 28-Abr (M1 landing + M2 QR)
- [ ] Página `/farmacias-que-cuidan/` creada con Elementor usando este copy.
- [ ] Todos los enlaces, iconos y colores aplicados (azul #0C4DA2, acento #770E75, Lato).
- [ ] Formulario de adhesión funcional con los 12 campos.
- [ ] Ruta Bizum / transferencia / tarjeta probada en los 3 escenarios.
- [ ] QR generado, probado en 3 móviles, exportado PNG + SVG.
- [ ] Flyer A5 maquetado (Cristina + Mayte).
- [ ] Pegatina Ø80 mm maquetada.
- [ ] Test de envío completo con NIF de prueba.

### Pendiente externo
- [ ] Listado oficial de Colegios de Farmacéuticos (¿desde DataCoF o scraping web?).
- [ ] Mocks del flyer + pegatina validados por Mónica antes de imprenta.
- [ ] Cita real de Rocío o texto institucional de sustitución.

---

## 6 · Copy adicional (pegatina digital post-compra)

Tras completar el donativo, el farmacéutico llega a una pantalla de "Gracias" con:

**H1:** Bienvenida a la red, [Nombre de la farmacia].

**P:** Tu donativo ha sido registrado. En los próximos 5-7 días laborables recibirás en [dirección] tu kit con la pegatina identificativa y las tarjetas informativas para tus clientes.

**Bloque destacado:**
- Descargar la versión digital de la pegatina (para RRSS): [botón]
- Descargar el certificado fiscal provisional: [botón] (el definitivo llegará en enero por Holded)
- Añadir tu farmacia al mapa nacional: [botón, si no se marcó en el formulario]

**Firma Mónica:**

> Gracias por sumaros. Sé que en una farmacia los días son intensos, y que dedicar 90 segundos a esto es un gesto concreto. Cada 100 € pagan unas horas de psicóloga que acompaña a una familia en casa. Nos vemos en el mapa.
>
> — Mónica Cantón, directora de la Fundación porqueViven
