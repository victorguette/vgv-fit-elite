# VGV-FIT ELITE 1.0 — Plantilla Elementor para gimnasios y entrenadores

Plantilla web completa e importable para **Elementor gratuito** + tema
Hello, de VGV Technology. Una página de aterrizaje (landing) para un
gimnasio o entrenador personal: encabezado con menú, portada,
características, entrenador profesional, servicios, app móvil, reto,
planes y precios, resultados, preguntas frecuentes y contacto.

**Versión publicada: VGV-FIT ELITE 1.0, Kit v7** (16 de noviembre de
2026). El Kit v7 es idéntico al v6 salvo un ajuste: en la sección
«Entrenador profesional» el texto va alineado arriba, junto a la parte
superior de la foto, en escritorio.

## Qué trae

- **1 página, 161 elementos**, solo widgets nativos gratuitos de
  Elementor (sin Elementor Pro, sin shortcodes, sin plugins
  adicionales).
- **11 secciones** con anclas: inicio, entrenador, entrenamientos, app,
  promo, planes, resultados, preguntas y contacto.
- **14 espacios de imagen** (13 fotos WebP; el logo se usa en 2 sitios)
  que se descargan solos a la Biblioteca de medios al importar el Kit.
- **36 animaciones de entrada** que se disparan una sola vez al hacer
  scroll (32 `fadeInUp` + 4 `fadeIn`, 3 lentas en las fotos grandes).
- **Colores y fuentes globales**: Anton para títulos, Inter para textos;
  naranja `#F97316` sobre negros `#101010` / `#080808` / `#1B1B1B`.
- **Responsive**: en tableta y celular las filas pasan a una sola
  columna.
- **Editable con clics**: cada foto, texto, precio, botón y enlace se
  edita en el editor de Elementor, sin código.

## Requisitos

- WordPress 7.1.4 o superior (probado en 7.1.4).
- Plugin **Elementor gratuito** 4.4.x instalado y activado. No hace falta
  Elementor Pro.
- Tema **Hello Elementor** activo.
- Conexión a internet al momento de importar: las fotos se descargan
  solas desde el repositorio público de fotos durante la importación.

## Instalación

1. Descarga el archivo **`VGV-FIT-ELITE-Kit.zip`** desde la
   [**Release**](../../releases) de este repositorio. No lo descomprimas.
2. En el panel de WordPress, ve a **Elementor > Herramientas** (*Tools*)
   > pestaña **Plantillas de sitios web** (*Website Templates*).
3. En la tarjeta **Aplicar una plantilla de sitio web** (*Apply a
   Website Template*), pulsa **Import** y sube el archivo ZIP.
4. Deja marcadas **Content** y **Settings & configurations**.
   **Templates** pide Pro: es normal, no hace falta para esta plantilla.
5. Pulsa **Import and apply**. Verás el mensaje *«Your website template
   is now live on your site!»*. La página se llama **VGV-FIT ELITE**.
6. Después de importar, a mano: pon la página como portada (**Ajustes >
   Lectura** > «Una página estática» > Portada: VGV-FIT ELITE) y
   regenera el CSS (**Elementor > Herramientas > General > Regenerate
   CSS & Data**).

El procedimiento completo, con capturas y solución de problemas, está en
[`docs/MANUAL-INSTALACION.md`](docs/MANUAL-INSTALACION.md).

## Estructura del repositorio

```
├── README.md                  Este archivo
├── kit-elementor/             Archivos del Kit descomprimidos (byte-idénticos al ZIP)
│   ├── manifest.json          Manifiesto del Kit (v2.0, exportado con Elementor 4.4.1)
│   ├── site-settings.json     Colores y tipografías globales
│   ├── global-classes.json    Clases globales (vacío: no se usan)
│   ├── content/page/5.json    La página «VGV-FIT ELITE» (161 elementos)
│   ├── taxonomies/            Taxonomía por defecto de la exportación
│   ├── wp-content/            Archivos WXR por defecto de la exportación
│   ├── 02-Landing-VGV-FIT-ELITE-respaldo.json   Respaldo (solo respaldo)
│   └── LEELO.md               Qué es cada archivo y por qué no editarlos a mano
├── assets/
│   ├── images/                Mapa de imágenes + nota (los 13 WebP se suben por separado)
│   └── css/                   Nota: no hay CSS personalizado (todo vive en el JSON)
├── docs/                      Manual, guía de personalización y licencias (Markdown + nota de los PDF)
└── evidencias/                Informes de verificación + lista de capturas (las JPG se suben por separado)
```

## Las fotos y el CDN

El formato de Kit de Elementor no lleva las fotos dentro: al importar,
las imágenes se descargan desde las URL guardadas en la página. Las 13
fotos WebP viven en el repositorio público
[`victorguette/vgv-fotos-elite`](https://github.com/victorguette/vgv-fotos-elite)
y se sirven por jsDelivr CDN:

`https://cdn.jsdelivr.net/gh/victorguette/vgv-fotos-elite@main/`

El mapa completo —qué archivo va en cada espacio, medidas, URL del CDN
y SHA-256— está en
[`assets/images/MAPA-IMAGENES.md`](assets/images/MAPA-IMAGENES.md). En
las pruebas de importación, los 14 archivos descargados coincidieron
por SHA-256 con los originales: 14/14.

## Estado y límites honestos

- El Kit se probó importándolo en **dos instalaciones limpias**
  (WordPress 7.1.4 + Hello, Elementor 4.4.1 y 4.4.0) con resultados
  idénticos, y **por la interfaz** en un WordPress Playground limpio,
  con revisión visual en pantalla. Ver
  [`evidencias/EVIDENCIA.md`](evidencias/EVIDENCIA.md).
- **Pendiente:** la prueba de importación en el staging Hostinger de
  Victor (hosting real, MySQL, español). Esa es la prueba final.
- La consola del navegador no se revisó (sin acceso a DevTools en el
  navegador de prueba) y el frontend móvil se verificó solo con la vista
  previa «Mobile Portrait» del editor, no en una ventana real de 390 px.
- **Licencias:** las 8 fotos originales fueron generadas con Muse Image
  (Meta) y sus derechos de reventa comercial están **sin verificar**. El
  camino seguro antes de vender la plantilla es regenerarlas con una
  herramienta de permiso comercial claro. Ver
  [`docs/LICENCIAS.md`](docs/LICENCIAS.md) (resumen de investigación; no
  es asesoramiento legal).

## Contenido de demostración

Los textos entre corchetes, los precios ($19.99 / $29.99 / $39.99), el
número de WhatsApp, el correo y las redes son contenido de demostración
marcado «EDITABLE»: deben reemplazarse por los reales antes de publicar.
La guía de personalización ([`docs/GUIA-PERSONALIZACION.md`](docs/GUIA-PERSONALIZACION.md))
explica dónde está cada uno.
