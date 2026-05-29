# Prompt — Web llave en mano: Ferretería Lali y Sara (Morales del Vino, Zamora)

---

## CONTEXTO DEL PROYECTO

Vas a construir un sitio web estático de una sola página para una ferretería de proximidad en un pueblo de Zamora. El sitio se desplegará en **GitHub Pages** usando HTML, CSS y JS puros — sin frameworks, sin build tools, sin npm. El resultado debe funcionar abriendo `index.html` directamente, sin servidor. `git push` y listo.

El negocio es una ferretería de barrio con muy buena valoración (4.6/5), conocida por su amplio surtido y, sobre todo, por el asesoramiento personal: el cliente entra, cuenta qué quiere hacer y sale con el material y la solución. El diseño debe transmitir eso: un escaparate cuidado, ordenado, con el producto y el trato cercano al frente.

---

## DATOS DEL NEGOCIO

```
NOMBRE:          Ferretería Lali y Sara
TIPO:            Ferretería / Comercio local (Schema: HardwareStore)
LOCALIDAD:       Morales del Vino, Zamora
DIRECCIÓN:       C. Corrales, 54, 49190 Morales del Vino, Zamora
TELÉFONO:        980 574 048  (incluir CTA de llamada con tel:+34980574048)
HORARIOS:        NO PUBLICAR — el cliente ha confirmado que NO debe aparecer ningún horario.
                 → Omitir la sección de horario por completo.
                 → Excluir openingHours / openingHoursSpecification del JSON-LD.
                 → NO añadir ningún texto alternativo del tipo "consultar horario".
EMAIL:           No disponible — omitir (sin email).
WEB EXTERNA:     No disponible — omitir.
REDES SOCIALES:  Ninguna — omitir iconos de redes y cualquier enlace social. Sin "sameAs".
ESPECIALIDADES:
  - Herramientas manuales y eléctricas
  - Materiales de construcción
  - Fontanería
  - Electricidad
  - Jardinería
  - Bricolaje general
  - Asesoramiento personalizado sobre materiales y técnicas
  - Entrega a domicilio y entrega el mismo día (mencionadas en dos fuentes)
  - Pago con tarjeta (crédito y débito) y pago móvil NFC
RESEÑAS REALES (usar como copy de testimonios, literales):
  - "Voy desde que era un enano, aquí puedes encontrar cualquier cosa que necesites. Tienen
     de todo. Incluso si no tienes claro qué necesitas le cuentas qué quieres hacer y te
     ayuda." — Rubén HC (Google)
  - "Muy buen trato, amables y cualquier duda te la resuelven muy bien sobre qué materiales
     utilizar. Muy aconsejable." — Héctor (Google)
  - "La mejor de los alrededores, buena atención, calidad precio, muchísimo material."
     — Cliente verificado (Google)
  - "La dueña, además de saber orientar al cliente a la perfección, es especialmente
     agradable. Tiene muchísima variedad de productos y bastante bien en cuanto a
     precio/calidad." — Cliente verificado (Google)
VALORACIÓN:      4.6 / 5 · 37 reseñas en Google (usar en aggregateRating)
FOTOS:           No disponibles — usar Unsplash (ver sección fotos)
GOOGLE MAPS URL: https://maps.google.com/?cid=14745082989007771555
MAPS CID:        14745082989007771555
COORDENADAS:     41.4446, -5.7311  (trianguladas desde callejero; usar el CID para el iframe)
COLOR/ESTÉTICA:  "Escaparate cuidado" — claro, ordenado, producto al frente, asesoramiento personal
```

> Nota interna (no publicar): Páginas Amarillas registra la misma dirección como "Almacén
> Domingo" con otro teléfono (980 570 153). NO usar ese nombre ni ese teléfono. Usar
> únicamente "Ferretería Lali y Sara" y el teléfono 980 574 048.

---

## ESTRUCTURA DE ARCHIVOS

```
/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js      (solo para el menú hamburger móvil y el header sticky — mínimo)
└── README.md
```

Sin páginas adicionales. Todo en una sola página con scroll suave entre secciones.

---

## SECCIONES (en este orden)

1. **Hero** — `<h1>` con "Ferretería Lali y Sara", tagline `"Todo lo que tu casa, tu obra o tu huerto necesitan — en Morales del Vino"`. Dos botones CTA: `"Ver qué ofrecemos"` (scroll anchor a #servicios) y `"Llamar 980 574 048"` (`tel:+34980574048`). Fondo: foto hero de ferretería (Unsplash). Overlay oscuro ~55% para garantizar legibilidad. Los botones deben ser visibles sin scroll en 375px.

2. **Sobre nosotros** — Párrafo corto y cálido. Idea central: una ferretería de proximidad en el corazón de Morales del Vino donde encuentras de todo y, si no sabes qué necesitas, te lo cuentan y te ayudan a resolverlo. Mencionar el amplio surtido (herramientas, construcción, fontanería, electricidad, jardinería) y el asesoramiento personal como seña de identidad. Tono cercano, local, de confianza de toda la vida, sin corporativo. Apoyarse en las reseñas reales que destacan el trato y la variedad.

3. **Nuestros servicios** — Grid con 6 servicios. Sin precios (no disponibles). Símbolo Unicode del set del preset por servicio (`◈ ✦ ❖ ◇ ⬡ ✓`). Servicios:
   - **Herramientas** — Manuales y eléctricas para cada trabajo, de la marca de confianza al recambio que buscabas.
   - **Materiales de construcción** — Lo que necesitas para tu obra o reforma, con consejo sobre qué usar en cada caso.
   - **Fontanería** — Tubería, griferías, juntas y accesorios para arreglar el grifo o montarlo de cero.
   - **Electricidad** — Cables, mecanismos, bombillas y pequeño material eléctrico para tu instalación.
   - **Jardinería y huerto** — Herramienta de campo, riego y todo lo que pide tu jardín o tu huerta.
   - **Asesoramiento personal** — Cuéntanos qué quieres hacer y te orientamos sobre los materiales y la técnica.

   Debajo del grid, una franja de **facilidades** en texto breve (no como servicios principales): "Entrega a domicilio y en el mismo día · Pago con tarjeta y móvil (NFC)".

4. **Galería** — 6 fotos de Unsplash (ver sección fotos). Grid 2 col en móvil, 3 col en desktop. Con `loading="lazy"`.

5. **Lo que dicen nuestros clientes** — Las 4 reseñas reales. Diseño de citas con comillas tipográficas grandes en el fondo, 5 estrellas ★★★★★ y el nombre/atribución real ("Rubén HC", "Héctor", "Cliente verificado"). Mostrar también la valoración global "4.6 / 5 · 37 reseñas en Google".

6. **Cómo llegar** — Dirección completa: `C. Corrales, 54, 49190 Morales del Vino, Zamora`. Botón de llamada (`tel:+34980574048`) y enlace al pin de Google Maps. Iframe del mapa embebido. **NO incluir horario ni mensaje sobre horario.** Texto de contacto: `"Estamos en C. Corrales, 54, en Morales del Vino. Acércate o llámanos al 980 574 048 y te ayudamos con lo que necesites."`

7. **Footer** — `© 2026 Ferretería Lali y Sara · C. Corrales, 54, 49190 Morales del Vino, Zamora · Tel. 980 574 048`. Sin iconos de redes sociales.

---

## REQUISITOS TÉCNICOS

### Mobile first
- CSS base desde 320px, breakpoints en 768px y 1024px.
- Touch targets mínimo 44×44px.
- Fuente base 17px en móvil.
- Botones del hero visibles sin scroll en 375px de alto.
- Menú hamburger colapsable en móvil (JS mínimo, sin librerías).

### Rendimiento
- Sin JS frameworks ni jQuery.
- Un único archivo CSS, sin preprocesador.
- Imágenes con `loading="lazy"` (excepto hero: `loading="eager"`).
- Google Fonts con `<link rel="preconnect">` y `display=swap`.
- Animaciones solo con `transform` y `opacity`.

### GitHub Pages
- Rutas relativas en todo (sin `/` inicial): `css/style.css`, no `/css/style.css`.
- Sin `fetch()` ni APIs externas con clave.
- Iframe de Maps con `referrerpolicy="no-referrer-when-downgrade"` y `loading="lazy"`.
- Funciona con `file://` sin servidor.

---

## SEO Y GEO — TODOS LOS CAMPOS OBLIGATORIOS

### `<head>`:

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ferretería Lali y Sara — Ferretería en Morales del Vino, Zamora</title>
<meta name="description" content="Ferretería Lali y Sara, tu ferretería de proximidad en Morales del Vino (Zamora). Herramientas, construcción, fontanería, electricidad y jardinería con asesoramiento personal.">
<meta name="keywords" content="ferretería Morales del Vino, ferretería Zamora, Lali y Sara, herramientas Morales del Vino, materiales de construcción Zamora, fontanería electricidad jardinería">
<link rel="canonical" href="https://clavijero.github.io/ferreteria-lali-y-sara/">

<meta property="og:title" content="Ferretería Lali y Sara — Morales del Vino, Zamora">
<meta property="og:description" content="Ferretería de proximidad en Morales del Vino: herramientas, construcción, fontanería, electricidad y jardinería con asesoramiento personal.">
<meta property="og:type" content="website">
<meta property="og:url" content="https://clavijero.github.io/ferreteria-lali-y-sara/">
<meta property="og:image" content="https://images.unsplash.com/photo-1581235720704-06d3acfcb36f?w=1200&q=80">
<meta property="og:locale" content="es_ES">

<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Ferretería Lali y Sara — Morales del Vino">
<meta name="twitter:description" content="Tu ferretería de proximidad en Morales del Vino, Zamora. Surtido amplio y asesoramiento personal.">
<meta name="twitter:image" content="https://images.unsplash.com/photo-1581235720704-06d3acfcb36f?w=1200&q=80">
```

### JSON-LD (justo antes de `</body>`):

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "HardwareStore",
  "name": "Ferretería Lali y Sara",
  "description": "Ferretería de proximidad en Morales del Vino (Zamora) especializada en herramientas, materiales de construcción, fontanería, electricidad y jardinería, con asesoramiento personal y amplio surtido.",
  "url": "https://clavijero.github.io/ferreteria-lali-y-sara/",
  "telephone": "+34980574048",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "C. Corrales, 54",
    "addressLocality": "Morales del Vino",
    "addressRegion": "Zamora",
    "postalCode": "49190",
    "addressCountry": "ES"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": 41.4446,
    "longitude": -5.7311
  },
  "hasMap": "https://maps.google.com/?cid=14745082989007771555",
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.6",
    "reviewCount": "37",
    "bestRating": "5"
  },
  "image": "https://images.unsplash.com/photo-1581235720704-06d3acfcb36f?w=1200&q=80",
  "priceRange": "€€",
  "currenciesAccepted": "EUR",
  "paymentAccepted": "Efectivo, Tarjeta de crédito, Tarjeta de débito, Pago móvil NFC"
}
</script>
```

> IMPORTANTE: el JSON-LD NO debe contener `openingHours`, `openingHoursSpecification` ni
> `sameAs` (decisión del cliente: sin horario publicado y sin web/redes).

### Headings:
- Un único `<h1>`: "Ferretería Lali y Sara"
- `<h2>`: "Sobre nosotros", "Nuestros servicios", "Galería", "Lo que dicen nuestros clientes", "Dónde estamos"
- `<h3>`: cada servicio individual

### Alt de imágenes:
- Hero: `alt="Interior de Ferretería Lali y Sara, ferretería de proximidad en Morales del Vino, Zamora"`
- Galería: descriptivos y variados — `alt="Estanterías con herramientas en la ferretería"`, `alt="Material de fontanería y tuberías"`, `alt="Herramientas eléctricas en exposición"`, `alt="Tornillería y pequeño material ordenado"`, `alt="Sección de electricidad y mecanismos"`, `alt="Herramienta de jardinería y huerto"`.

---

## DISEÑO Y ESTÉTICA

### Dirección visual: "Escaparate cuidado"
Comercio local claro y ordenado, con el producto y el asesoramiento personal al frente. Fiable y cercano, nada estridente. Azul sobrio de confianza como acento, sobre fondos cálidos templados. Las reseñas hablan de variedad y de buen trato — el diseño debe transmitir orden, surtido y proximidad.

### Paleta — pegar tal cual en `:root`:

```css
:root {
  --bg:          #FAF8F5;
  --bg-alt:      #EFEAE3;
  --accent:      #44617A;
  --accent-dark: #354C61;
  --secondary:   #2B2F36;
  --text:        #18191B;
  --text-soft:   #4A4F55;
  --line:        #E2DBD0;
  --dark:        #18191B;
  --font-head:   'Fraunces', Georgia, serif;
  --font-body:   'Nunito Sans', system-ui, sans-serif;
}
```

### Tipografía (Google Fonts — usar esta combinación):
- Headings: **Fraunces** (weight 400 y 600) — carácter, cálida, no genérica.
- Body: **Nunito Sans** (weight 400 y 600) — legible, neutra y amable.

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:wght@400;600&family=Nunito+Sans:wght@400;600&display=swap" rel="stylesheet">
```

### Detalles de calidad:
- `scroll-behavior: smooth` en `html`.
- Línea decorativa fina (`border-bottom: 2px solid var(--accent); width: 60px`) bajo cada `<h2>`.
- Iconos de servicio con símbolos Unicode del set `◈ ✦ ❖ ◇ ⬡ ✓` en color `var(--accent)`.
- Cards de servicios: hover con `transform: translateY(-4px)` y `transition: 0.25s ease`.
- Header sticky con cambio de `background` al hacer scroll (JS mínimo: toggle de clase `.scrolled`).
- Sección de testimonios sobre fondo oscuro `var(--secondary)` con texto claro.
- Separación generosa entre secciones: `padding: 5rem 1.5rem` en móvil.
- Comillas tipográficas grandes (`"`) en color tenue como fondo decorativo en testimonios.

### Lo que NO hacer:
- Sin fondo blanco puro `#FFFFFF`.
- Sin estética "ferretería de gran superficie" agresiva (rojos/amarillos chillones, ofertas).
- Sin botones `border-radius: 50px` fosforitos.
- Sin sombras grandes tipo Material Design.
- Sin Inter, Roboto, Arial ni Montserrat.
- Sin iconos de redes sociales ni enlaces externos de contacto.
- Sin mostrar ningún horario ni mensaje sobre horario.

---

## FOTOS — UNSPLASH

Términos de búsqueda de respaldo: `hardware-store`, `local-store`. Solo interiores de tienda / producto de ferretería, nada de personas recortadas ni stock corporativo.

```
HERO (loading="eager"):
https://images.unsplash.com/photo-1581235720704-06d3acfcb36f?w=1400&q=80

GALERÍA (loading="lazy"):
https://images.unsplash.com/photo-1530124566582-a618bc2615dc?w=800&q=80
https://images.unsplash.com/photo-1572981779307-38b8cabb2407?w=800&q=80
https://images.unsplash.com/photo-1607582544043-6a3e3c4d9a2b?w=800&q=80
https://images.unsplash.com/photo-1504148455328-c376907d081c?w=800&q=80
https://images.unsplash.com/photo-1426927308491-6380b6a9936f?w=800&q=80
https://images.unsplash.com/photo-1416879595882-3373a0480b5b?w=800&q=80
```

Si alguna URL falla en el momento de construir, buscar reemplazo en `https://unsplash.com/s/photos/hardware-store` — solo interiores y producto, no de personas recortadas.

---

## README.md A GENERAR

```markdown
# Ferretería Lali y Sara — Web

Sitio estático para Ferretería Lali y Sara (Morales del Vino, Zamora).
Desplegado en GitHub Pages. Sin dependencias, sin build.

## Despliegue inicial

git init
git add .
git commit -m "init: web Ferretería Lali y Sara"
git remote add origin https://github.com/clavijero/ferreteria-lali-y-sara.git
git push -u origin main

Activar en GitHub: Settings → Pages → Branch: main → / (root) → Save.
URL: https://clavijero.github.io/ferreteria-lali-y-sara/

## Actualizar contenido

Editar index.html o css/style.css directamente y hacer git push.
No se necesita ningún build ni servidor local.
```

---

## CHECKLIST ANTES DE ENTREGAR

- [ ] Funciona abriendo `index.html` con `file://` sin servidor.
- [ ] Rutas relativas en todo — sin `/` inicial.
- [ ] Un único `<h1>` con "Ferretería Lali y Sara".
- [ ] `<meta name="description">` entre 120 y 160 caracteres.
- [ ] JSON-LD tipo `HardwareStore` completo, sin campos vacíos ni placeholders.
- [ ] JSON-LD SIN `openingHours` y SIN `sameAs` (decisión del cliente).
- [ ] `aggregateRating` con `ratingValue` 4.6 y `reviewCount` 37.
- [ ] Coordenadas `41.4446, -5.7311` en el JSON-LD.
- [ ] `telephone` "+34980574048" en el JSON-LD y CTA `tel:+34980574048` en hero y contacto.
- [ ] Iframe de Google Maps con `referrerpolicy` y `loading="lazy"`.
- [ ] Enlace real al pin: `https://maps.google.com/?cid=14745082989007771555`
- [ ] Las 4 reseñas reales con su atribución (Rubén HC, Héctor, Cliente verificado).
- [ ] Todas las imágenes con `alt` descriptivo.
- [ ] Botones del hero visibles sin scroll en viewport de 375×667px.
- [ ] Contraste texto/fondo ≥ 4.5:1 en todos los bloques (especialmente hero con overlay).
- [ ] Google Fonts con `preconnect` y `display=swap`.
- [ ] NINGÚN horario ni mensaje sobre horario en toda la web.
- [ ] Sin email, sin web externa, sin redes sociales ni sus iconos.
- [ ] README.md con instrucciones de despliegue.
```
