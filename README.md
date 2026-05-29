# Ferretería Lali y Sara — Web

Sitio estático para Ferretería Lali y Sara (Morales del Vino, Zamora).
Desplegado en GitHub Pages. Sin dependencias, sin build.

## Despliegue inicial

    git init
    git add .
    git commit -m "init: web Ferretería Lali y Sara"
    git remote add origin https://github.com/clavijero/lali-y-sara.git
    git push -u origin main

Activar en GitHub: Settings → Pages → Branch: main → / (root) → Save.
URL: https://clavijero.github.io/lali-y-sara/

## Actualizar contenido

Editar `index.html` o `css/style.css` directamente y hacer `git push`.
No se necesita ningún build ni servidor local. Funciona abriendo `index.html` con `file://`.

## Tematización

La paleta y las fuentes están en el bloque `:root` al inicio de `css/style.css`.
Cambiar solo esas variables modifica todo el sitio.
