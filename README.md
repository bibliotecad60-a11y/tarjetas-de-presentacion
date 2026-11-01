TARJETAS PRO — EDICIÓN WEB HTML
================================

CONTENIDO
- index.html: aplicación web principal.
- card-templates.js: colección de 30 plantillas.
- card-editor.js: edición de datos, estilos y orientación.
- card-storage.js: almacenamiento local de tarjetas.
- card-export.js: exportación PNG, PDF real (archivo) y compartir cuando el navegador lo admite.
- lib/pdf-lib.min.js: librería PDF (pdf-lib, licencia MIT en lib/pdf-lib.LICENSE.md), incluida para no depender de internet.
- usage-tracker.js: control local de descargas gratuitas (5 por defecto) y códigos de activación.
- qr-code.js: generador de códigos QR reales (vCard escaneable), sin conexión.
- manifest.webmanifest e iconos (icon-192.png, icon-512.png, icon-maskable-512.png): datos de la app para instalarla desde Chrome.
- fonts/: tipografías incluidas para trabajar sin depender de Google Fonts.

CÓMO ABRIR
1. Extrae todo el ZIP conservando la estructura de carpetas.
2. Abre index.html con Chrome, Edge o Firefox.
3. Para un uso más estable en Android, sirve esta carpeta desde un alojamiento web/servidor local y abre la dirección en Chrome.

GALERÍA
La galería permite buscar por nombre/categoría, filtrar por Corporativo, Moderno, Creativo, Tech y Vintage, y seleccionar cualquiera de las 30 tarjetas. Las miniaturas son vistas previas generadas con los colores y estilos de cada plantilla.

ORIENTACIÓN, PDF Y LÍMITE DE DESCARGAS
El editor permite orientación horizontal y vertical. El botón PDF descarga un archivo PDF del tamaño exacto de una tarjeta (3.5 x 2 pulgadas, o 2 x 3.5 en vertical). Si el navegador no puede generarlo, se abre el diálogo de impresión como respaldo ("Guardar como PDF").
Cada persona tiene 5 descargas gratuitas (PNG, PDF o compartir). Guardar y editar tarjetas no consume descargas. Al agotarse, se pide un código de activación. Para cambiar el número: MAX_FREE_USES en usage-tracker.js. Para entregar códigos: lista VALID_CODES en el mismo archivo.

IMPORTANTE — LIMITACIONES
- El QR es real y escaneable: codifica una vCard con nombre, empresa, cargo, teléfono, correo y sitio web. Si el contenido es largo, se omite la dirección para que el QR sea más pequeño y fácil de leer. Escanea siempre la tarjeta antes de imprimirla en cantidad.
- El límite y los códigos se controlan en el navegador de cada persona: frenan el uso normal, pero quien borre los datos del navegador o sepa de programación puede saltarlos. Para un control real hace falta un servidor. No valida compras.
- La exportación PNG usa SVG foreignObject. Si abres index.html directamente (file://), el PNG usa las fuentes del sistema en lugar de DejaVu; sirviendo la carpeta desde un servidor local o alojamiento web se incrustan las fuentes incluidas. Si tu navegador móvil no la admite, el PDF intentará usar el diálogo de impresión.
- Los datos guardados permanecen en el almacenamiento local del navegador/dispositivo. Haz respaldo antes de borrar datos del navegador o cambiar de dispositivo.

No se incluye APK ni código nativo Android: esta edición está preparada como sitio/app web HTML. No incluye service worker, así que no funciona sin conexión como app instalada.
