# QA Report — Ferretería Lali y Sara

**Slug:** `ferreteria-lali-y-sara`
**URL de despliegue:** https://clavijero.github.io/lali-y-sara/
**Fecha auditoría:** 2026-05-30

## VEREDICTO: APTO PARA DESPLIEGUE

El sitio supera todos los bloques críticos del checklist.

---

## Correcciones aplicadas durante el QA

1. **Meta description reducida de 167 a 158 caracteres** (`index.html`, línea 7) — dentro del rango 120–160.
2. **Botones de contacto — desbordamiento en móvil estrecho** (`css/style.css`) — media query `@media (max-width: 479px)` que apila los botones "Llamar" / "Ver en Google Maps" a ancho completo en viewports de 320–400 px.

## Correcciones aplicadas por el orquestador (post-QA)

3. **Imagen rota sustituida** — `photo-1607582544043-6a3e3c4d9a2b` (HTTP 404) reemplazada por `photo-1581244277943-fe4a9c777189` (verificada 200) en la galería ("Herramientas eléctricas en exposición"). Las 7 imágenes Unsplash devuelven ahora HTTP 200.
4. **URLs absolutas reconciliadas con el repo real** — canonical, og:url, JSON-LD `url` y README actualizados de `…/ferreteria-lali-y-sara/` a `…/lali-y-sara/` (el repositorio de despliegue es `clavijero/lali-y-sara`).

---

## Resultados por bloque

**Integridad de plantilla — PASA**
- Cero tokens `{{...}}` ni comentarios `[[...]]` sin sustituir.
- Sin `src=""`, `href="#"` huérfanos ni atributos vacíos significativos.

**Técnico / GitHub Pages — PASA**
- Rutas relativas correctas: `css/style.css`, `js/main.js` sin `/` inicial.
- Hero: `loading="eager"` + `fetchpriority="high"`. Galería: `loading="lazy"` con `width`/`height`.
- Iframe con `title`, `referrerpolicy` y `loading="lazy"`.
- Sin `fetch()`, sin frameworks JS, sin dependencias de build.
- Google Fonts con doble `preconnect` y `display=swap`.

**SEO / GEO — PASA**
- Un único `<h1>`.
- Meta description: 158 caracteres.
- `canonical`, OG y Twitter coherentes con el slug de despliegue `lali-y-sara`.
- JSON-LD válido, `@type: HardwareStore`, **sin `openingHours`**, **sin `sameAs`**, sin campos vacíos.
- Coordenadas (41.4446, -5.7311), dirección (C. Corrales, 54, 49190 Morales del Vino) y teléfono (+34980574048) coinciden con la ficha.
- CID Maps `14745082989007771555` correcto en `hasMap` y enlace "Ver en Google Maps".
- `aggregateRating`: 4.6 / 37 reseñas (verificado).

**Coherencia con datos verificados — PASA**
- Solo el teléfono 980 574 048 (descartado el 980 570 153 de Páginas Amarillas / "Almacén Domingo").
- Sin horarios en ninguna sección ni en el JSON-LD (decisión cliente).
- Sin email, web externa ni redes sociales (decisión cliente).
- Las 4 reseñas reales presentes con atribuciones correctas.

**Accesibilidad / móvil — PASA**
- Todas las imágenes con `alt` descriptivo y variado.
- Touch targets ≥ 44px.
- Menú hamburger con `aria-expanded`, cierre con Escape, foco devuelto al botón.
- Contraste hero y `.btn-hero-secondary` correctos.

---

## Pendientes para decisión humana

- **P1 — Contraste de estrellas en testimonios (menor):** `.estrellas`/`.estrellas-inline` usan `--accent` (#44617A) sobre `--secondary` (#2B2F36), ratio ~2.1:1 (umbral WCAG UI 3:1). Llevan `aria-label`, por lo que el valor numérico adyacente en blanco cubre la información. Opción de subir a un tono más claro (ej. #7BACC4) si se desea cumplir 3:1.
- **P3 — Coordenadas trianguladas:** lat/lng 41.4446, -5.7311 son una aproximación desde callejero (el CID sí está confirmado). El enlace "Ver en Google Maps" usa el CID (pin exacto); el iframe usa coordenadas (zona correcta). Conviene confirmar visualmente que el marcador cae sobre el local.

*P2 (validación de imágenes en vivo) resuelto: ver corrección 3.*
