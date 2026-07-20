# Boletín Vicedecanato de Investigación y Postgrado — Facultad de Humanidades USACH

Versión web del Boletín «Cuenta Pública 2024–2026 · Investigación», lista para publicar en GitHub Pages.

## Contenido de esta carpeta

```
boletin-fahu-web/
├── index.html            ← el boletín (página principal)
├── support.js            ← runtime que renderiza la página
├── image-slot.js         ← componente de imágenes arrastrables (marcos aún vacíos)
├── assets/
│   ├── logo-fahu.png     ← logotipo de la Facultad
│   ├── e_lineas.js       ← datos de líneas de investigación (punto 1.e)
│   └── img/              ← imágenes ya incrustadas (retrato de intro, captura del sitio)
└── .nojekyll             ← evita el procesamiento Jekyll de GitHub Pages
```

Todas las rutas son **relativas**, por lo que el sitio funciona al servirse desde cualquier subcarpeta de un repositorio.

## Cómo publicarlo en GitHub Pages

1. Sube el **contenido** de esta carpeta a la raíz del repositorio (o a `/docs`).
2. En el repositorio: **Settings → Pages** → *Deploy from a branch*, rama `main`, carpeta `/root` (o `/docs`).
3. En un par de minutos estará en `https://<usuario>.github.io/<repositorio>/`.

## Visualización robusta y caché

- **El contenido siempre se muestra.** El boletín anima las secciones al hacer scroll mediante JavaScript (que carga el motor de render desde un CDN). Si esa carga falla o va lenta en alguna red, una **red de seguridad en JavaScript puro** revela todo el contenido de todas formas: el boletín nunca queda en blanco.
- **Refresco de caché.** `index.html` incluye cabeceras `no-cache` y los scripts llevan una marca de versión (`?v=…`) que cambia en cada exportación, de modo que los navegadores no sirven una versión antigua desde la caché.
- **Conexión a internet:** la página carga tipografías (Google Fonts) y el motor de render desde CDN; GitHub Pages sirve el sitio online, así que funciona sin pasos extra.

## Otras notas

- **Versión impresa / PDF:** botón «Imprimir / PDF» (arriba a la derecha) o `Ctrl/Cmd + P`. La maquetación de impresión oculta la navegación y muestra los datos en tablas estáticas.
- **Imágenes:** las imágenes ya cargadas están **incrustadas** en `assets/img/`. Los marcos aún vacíos (fotografía de revistas y cierre de 1.c) se muestran como marcadores hasta que se incrusten las definitivas.
- **Actualizar:** cada vez que quieras sincronizar cambios, vuelve a exportar esta carpeta y súbela al repositorio (commit + push).
