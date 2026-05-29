# Ficha de negocio — Ferretería Lali y Sara

SLUG_PROPUESTO:  ferreteria-lali-y-sara
TIPO:            Ferretería / Comercio local
PRESET_SUGERIDO: 7 — Comercio / Tienda local (Schema: HardwareStore)
CONFIANZA:       media  — dirección, teléfono y CID verificados en dos fuentes independientes;
                          coordenadas trianguladas pero no extraídas de Google Maps directamente;
                          reseñas textuales confirmadas.

## Identidad
NOMBRE:          Ferretería Lali y Sara
DESCRIPCIÓN:     Ferretería de proximidad en Morales del Vino (Zamora) especializada en
                 herramientas, materiales de construcción, fontanería, electricidad y
                 jardinería. Asesoramiento personal y amplio surtido de producto.

## Ubicación
DIRECCIÓN:       C. Corrales, 54
CP:              49190
LOCALIDAD:       Morales del Vino
PROVINCIA:       Zamora
COORDENADAS:     41.4446, -5.7311  (trianguladas desde callejero; pendiente confirmación exacta)
MAPS_CID:        14745082989007771555
MAPS_URL:        https://maps.google.com/?cid=14745082989007771555

## Contacto
TELÉFONO:        980 574 048
EMAIL:           NO DISPONIBLE — sin email (confirmado por cliente)
WEB:             NO DISPONIBLE — sin web (confirmado por cliente)
REDES:           NINGUNA — sin redes sociales (confirmado por cliente) → omitir iconos de redes

## Horarios
HORARIOS:        NO PUBLICAR — horario sin confirmar (decisión cliente)
                 → Omitir sección de horario en la web y excluir openingHours del JSON-LD.
                 → No mostrar franjas horarias; no añadir mensaje de "consultar horario".

## Reseñas (literales, reales)
VALORACIÓN:      4.6 / 5 · 37 reseñas en Google
- "Voy desde que era un enano, aquí puedes encontrar cualquier cosa que necesites. Tienen de
  todo. Incluso si no tienes claro que necesitas le cuentas que quieres hacer y te ayuda."
  — Rubén HC (5/5, Google)
- "Muy buen trato, amables i cualquier duda te la resuelve muy bien sobre qué materiales
  utilizar. Muy aconsejable." — Héctor (5/5, Google)
- "La mejor de los alrededores, buena atención, calidad precio, muchísimo material"
  — Cliente verificado (Google)
- "La dueña, además de saber orientar al cliente a la perfección, es especialmente agradable.
  Tiene muchísima variedad de productos y bastante bien en cuanto a precio/calidad."
  — Cliente verificado (Google)

## Servicios / especialidades
- Herramientas manuales y eléctricas
- Materiales de construcción
- Fontanería
- Electricidad
- Jardinería
- Bricolaje general
- Asesoramiento personalizado sobre materiales y técnicas
- Entrega a domicilio (mencionada en dos fuentes, sin confirmar área de cobertura)
- Entrega el mismo día (mencionada en dos fuentes)
- Pago con tarjeta (crédito y débito) y pago móvil NFC

## Fotos
FOTOS_PROPIAS:   NO DISPONIBLES → usar Unsplash
UNSPLASH_TERMS:  "hardware-store", "local-store"

## Fuentes consultadas
- https://papeleriatecnicacano.es/ferreteria-lali-y-sara/
- https://comprarenzamora.com/negocios/ferreteria-lali-y-sara/
- https://morales-del-vino.callejero.net/calle-corrales.html
- https://www.paginasamarillas.es/f/morales-del-vino/almacen-domingo_144208345_000000001.html
- https://morales-del-vino.infoisinfo.es/busqueda/ferreteria

## Notas para el constructor
1. HORARIO: No publicar. El cliente ha confirmado que no debe aparecer ningún horario en la web.
   Excluir el campo openingHours del JSON-LD LocalBusiness. No añadir ningún texto alternativo
   sobre el horario.

2. CONTACTO ONLINE: El negocio no dispone de web, email ni redes sociales (confirmado por
   cliente). La web mostrará únicamente teléfono (980 574 048) y dirección postal. Omitir
   todos los botones de enlace externo e iconos de redes sociales.

3. COORDENADAS: Lat 41.4446 / Long -5.7311 son coordenadas trianguladas a partir del
   callejero de la calle, no extraídas directamente de Google Maps (la pasarela de
   consentimiento de Google bloqueó el acceso directo). El CID sí está confirmado en dos
   fuentes independientes. Usar el CID para el iframe; verificar coordenadas exactas con
   el cliente o revisando el pin en Google Maps.

4. NOMBRE LEGAL vs. COMERCIAL: Páginas Amarillas registra la misma dirección (C. Corrales 54)
   bajo el nombre "Almacén Domingo" con un teléfono diferente (980 570 153). Puede ser un
   negocio anterior en ese local, o una segunda actividad. No incluir ese teléfono; usar
   solo 980 574 048, confirmado en las dos fuentes principales.

5. SCHEMA: Usar HardwareStore como @type en el JSON-LD. No incluir openingHours ni sameAs
   (sin redes ni web externa). aggregateRating: 4.6/5 con 37 reseñas.

6. VALORACIÓN: Usar 4.6/5 (37 reseñas). Actualizar si el cliente confirma dato más reciente.
