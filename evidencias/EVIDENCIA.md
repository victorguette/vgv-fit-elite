# EVIDENCIA DE PRUEBAS — VGV-FIT ELITE 1.0 (Kit v7)

Fecha de las pruebas: 16 de noviembre de 2026.
Kit probado: `VGV-FIT-ELITE-Kit.zip` (13.354 bytes, SHA-256
`2d48168f997a2f045179310ab37fc27664a6b331ca00090c3252769f240ac119`).

## Qué cambió respecto al Kit v6

Un solo ajuste, pedido por Victor: en la sección «Entrenador
profesional», la columna de texto quedaba flotando a media altura junto
a la foto alta de la entrenadora (la fila usaba alineación vertical
centrada). Ahora el texto empieza arriba, alineado con la parte
superior de la foto, en escritorio; en tableta y celular el
comportamiento no cambió. El cambio son exactamente 3 ajustes en un
solo contenedor de la página; la foto no se tocó (se muestra completa,
sin ningún recorte aplicado por la plantilla). Todo lo demás es
idéntico al Kit v6, verificado por comparación directa de los datos
importados.

## 1. Importación en dos instalaciones limpias (nivel de datos)

El MISMO archivo ZIP se importó en dos instalaciones limpias de
WordPress 7.1.4 + tema Hello 3.5.2: una con Elementor 4.4.1 y otra con
Elementor 4.4.0 (la versión exacta del staging de Victor). En ambas,
los datos de la página importada fueron idénticos:

- 161 elementos; 36 animaciones exactas (32 fadeInUp + 4 fadeIn, 3
  lentas); 10 tipos de widget, todos gratuitos; 15 enlaces; colores y
  fuentes globales (Anton/Inter); plantilla de página
  `elementor_canvas`; página editable en el editor.
- Imágenes: 14/14 espacios descargados a la Biblioteca de medios, 0
  marcadores de posición, y los 14 archivos coinciden byte a byte
  (SHA-256) con los WebP originales.
- La fila del entrenador quedó con alineación superior en escritorio y
  centrada en tableta/móvil, confirmado en el CSS generado; los anchos
  de fila y las fotos de servicios del Kit v6 quedaron intactos.

Detalle completo: `VERIFICATION-REPORT.md` (en esta carpeta).

## 2. Importación por la interfaz + revisión visual (navegador)

En un WordPress Playground limpio (WordPress 7.1.4 + Elementor gratuito
4.4.1 + Hello), se importó el Kit v7 por la interfaz: Elementor > Tools
> Website Templates > «Apply a Website Template», con Content + Settings
marcados (Templates quedó bloqueado por Pro, como se esperaba). Mensaje
final: «Your website template is now live on your site!».

En el frontend, a 1919 px de ancho, se verificó con capturas:

- La sección del entrenador quedó alineada arriba: el texto empieza a
  unos 10 px de la parte superior de la foto, sin el espacio negro que
  antes quedaba encima del texto. La foto se ve completa de la cabeza a
  las piernas (el encuadre original de la foto termina a media pierna;
  Elementor no recorta nada).
- Sin regresiones: encabezado en una sola fila, características y
  servicios en filas de 4, precios visibles, pie de página en 3
  columnas.
- En la vista previa «Mobile Portrait» del editor, la sección del
  entrenador se apila limpio: texto arriba y foto debajo, a ancho
  completo.

Capturas en esta carpeta (archivos JPG originales, sin recortar):

- `00-pantalla-plantillas-sitio-web.jpg` — Elementor > Tools, pestaña
  «Website Templates»: tarjetas «Export this website» y «Apply a Website
  Template» con el botón Import. (Captura de la revisión del Kit v6; la
  pantalla y el procedimiento son los mismos en v7.)
- `01-encabezado-hero.jpg` — encabezado en una sola fila (logo, menú de
  5 botones y botón ACCEDER A MI CUENTA) + portada con su foto.
  (Revisión v6; sin cambios en v7.)
- `02-fila-caracteristicas.jpg` — las 4 características en una sola
  fila. (Revisión v6; sin cambios en v7.)
- `03-servicios-4-columnas.jpg` — las 4 tarjetas de servicios en una
  sola fila, con sus fotos llenando el ancho de cada tarjeta.
  (Revisión v6; sin cambios en v7.)
- `04-precios.jpg` — las 3 tarjetas de precios visibles en una fila
  (BÁSICO $19.99, PREMIUM $29.99 «MÁS POPULAR», ELITE $39.99).
  (Revisión v6; sin cambios en v7.)
- `05-pie-pagina.jpg` — pie de página en 3 columnas en una sola fila.
  (Revisión v6; sin cambios en v7.)
- `06-movil-vista-previa-editor.jpg` — vista previa «Mobile Portrait»
  del editor: el diseño se apila limpio, menú en columna.
  (Revisión v6; sin cambios en v7.)
- `07-importacion-partes.jpg` — pantalla «Select which parts you want to
  apply»: Content y Settings & configurations marcados, Templates con
  «Upgrade» (Pro). (Revisión v6; la pantalla es la misma en v7.)
- `08-importacion-exito.jpg` — mensaje final de importación correcta.
  (Revisión v6; el mismo mensaje se vio al importar v7.)
- `09-panel-edit-image.jpg` — editor: panel «Edit Image» abierto al
  hacer clic en la foto principal (prueba de que las imágenes son
  editables). (Revisión v6; sin cambios en v7.)
- `10-entrenador-alineado-arriba.jpg` — REVISIÓN V7: sección
  «Entrenador profesional» en escritorio: el texto empieza arriba,
  alineado con la parte superior de la foto.
- `11-entrenador-foto-inferior-servicios.jpg` — REVISIÓN V7: parte
  inferior de la foto de la entrenadora y comienzo de la sección
  «Nuestros servicios».
- `12-entrenador-movil-vista-previa.jpg` — REVISIÓN V7: vista previa
  «Mobile Portrait» del editor: la sección del entrenador apilada, con
  el texto en una sola columna.
- `13-entrenador-movil-foto.jpg` — REVISIÓN V7: vista previa móvil del
  editor: la foto de la entrenadora a ancho completo y, debajo, la
  sección de servicios apilada.

La barra oscura flotante que se ve en la parte inferior de algunas
capturas es de WordPress Playground (el entorno de prueba), no de la
plantilla.

## 3. Límites honestos — lo que NO se verificó

- La consola del navegador NO se revisó (el navegador de la prueba no
  tenía acceso a DevTools). No se vio ningún síntoma de error, pero no
  se puede afirmar que no haya errores de consola.
- El frontend móvil NO se probó en una ventana real de 390 px (el
  navegador de la prueba no permitía redimensionar). La vista móvil se
  verificó solo con la vista previa «Mobile Portrait» del editor.
- Las pruebas corrieron en WordPress Playground (SQLite, inglés), no en
  el hosting real de Victor (Hostinger, MySQL, español). La prueba de
  importación en su staging sigue pendiente de su lado y es la prueba
  final.
- Las animaciones se verificaron a nivel de datos y de marcado/CSS, y su
  disparo al hacer scroll se observó en el navegador; la velocidad exacta
  en un teléfono real no se midió.
