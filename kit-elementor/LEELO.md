# Kit Elementor — VGV-FIT ELITE 1.0 (Kit v7)

Esta carpeta contiene los archivos del Kit **descomprimidos**, tal como los
exportó el propio Elementor, para que puedan revisarse directamente desde
GitHub. Son byte-idénticos a las entradas del archivo
`VGV-FIT-ELITE-Kit.zip` publicado en la Release de este repositorio
(SHA-256 del ZIP: `2d48168f997a2f045179310ab37fc27664a6b331ca00090c3252769f240ac119`).

## El ZIP de la Release es el método de importación

Para instalar la plantilla, importa el archivo `VGV-FIT-ELITE-Kit.zip`
desde la Release (sin descomprimirlo): Elementor > Herramientas >
«Plantillas de sitios web» > «Aplicar una plantilla de sitio web».
El procedimiento completo está en `docs/MANUAL-INSTALACION.md`.

**No edites estos archivos a mano ni intentes reempaquetarlos**: el
formato del Kit (incluido `manifest.json`) lo genera el propio Elementor
y no está documentado para fabricarse a mano. Cualquier cambio de diseño
debe hacerse en el editor de Elementor y volver a exportarse.

## Contenido

| Archivo | Qué es |
|---|---|
| `manifest.json` | Manifiesto del Kit (versión 2.0, exportado con Elementor 4.4.1). |
| `site-settings.json` | Ajustes del sitio: colores globales, tipografías globales y ajustes del tema. |
| `global-classes.json` | Clases globales (vacío: la plantilla no usa clases globales). |
| `content/page/5.json` | La página «VGV-FIT ELITE»: 161 elementos, solo widgets gratuitos. |
| `taxonomies/category.json` | Taxonomía por defecto incluida en la exportación. |
| `wp-content/*.xml` | Archivos WXR por defecto de la exportación (sin contenido propio). |
| `02-Landing-VGV-FIT-ELITE-respaldo.json` | Respaldo de la página en formato de plantilla JSON (161 elementos). Solo respaldo: el método de importación es el Kit ZIP. Los 14 espacios de imagen apuntan a las URL permanentes del CDN (ver `../assets/images/MAPA-IMAGENES.md`). |

## Datos verificados del Kit

- 161 elementos; 36 animaciones de entrada (32 `fadeInUp` + 4 `fadeIn`,
  3 lentas); 10 tipos de widget, todos gratuitos; 15 enlaces.
- Plantilla de página `elementor_canvas`; colores y fuentes globales
  (Anton/Inter); página editable en el editor.
- Los 14 espacios de imagen llevan URL del CDN con `id` vacío: al
  importar, Elementor descarga las fotos a la Biblioteca de medios. El
  Kit no lleva binarios dentro (así funciona el formato de Kit de
  Elementor). Las fotos descargadas se verificaron byte a byte (SHA-256)
  contra los archivos originales en dos instalaciones limpias.
- La sección «Entrenador profesional» lleva la alineación superior en
  escritorio (ajuste v7) y centrada en tableta/móvil.
- Sin shortcodes ni rutas del plugin VGV-FIT: la plantilla funciona
  sola, con Elementor gratuito.
