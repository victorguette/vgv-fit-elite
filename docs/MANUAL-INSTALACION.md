# VGV-FIT ELITE 1.0 — Manual de instalación (Kit v7, probado 16 nov 2026)

Kit importable para Elementor gratuito + tema Hello.
Procedimiento probado el 16 de noviembre de 2026.

> Versión en Markdown del documento `Manual-Instalacion.pdf` (6 páginas,
> con capturas). El contenido es el mismo. Las versiones PDF se suben por
> separado a este repositorio (ver `NOTA.md` en esta carpeta).

## Qué contiene este paquete

- **VGV-FIT-ELITE-Kit.zip** — el único archivo que debes importar. No lo
  descomprimas.
- **02-Landing-VGV-FIT-ELITE-respaldo.json** — respaldo de la página,
  solo por si hace falta. No es el método de importación.
- **Fotos/** — las 13 fotos WebP + el mapa que dice dónde va cada una.
- **Guia-Personalizacion.pdf** — cómo cambiar textos, fotos, precios y
  enlaces.
- **Licencias.pdf** — qué debes saber sobre las fotos de IA antes de
  vender la plantilla.
- **Evidencia/** — informe de verificación y capturas de las pruebas de
  importación.

## Antes de empezar (requisitos)

- WordPress 7.1.4 o superior (probado en 7.1.4).
- Plugin **Elementor gratuito** 4.4.x instalado y activado. **No hace
  falta Elementor Pro.**
- Tema **Hello Elementor** activo.
- Conexión a internet al momento de importar: las fotos se descargan
  solas desde el repositorio público de fotos durante la importación.

> **Las capturas están en inglés.** La prueba se hizo en un WordPress en
> inglés, por eso las capturas muestran los textos en inglés (*Tools,
> Website Templates, Apply a Website Template*). En tu sitio en español
> verás las mismas pantallas con los textos traducidos: *Herramientas,
> Plantillas de sitios web, Aplicar una plantilla de sitio web*. Los
> pasos son los mismos. La barra oscura flotante de algunas capturas es
> de WordPress Playground (el entorno de prueba), no de la plantilla.

## Paso 1 — Abre la pantalla de plantillas de sitio web

1. Entra al panel de WordPress (*Escritorio*).
2. En el menú de la izquierda, haz clic en **Elementor** y luego en
   **Herramientas** (*Tools*).
3. Arriba, haz clic en la pestaña **Plantillas de sitios web**
   (*Website Templates*).
4. Verás dos tarjetas. En la segunda, **Aplicar una plantilla de sitio
   web** (*Apply a Website Template*), haz clic en el botón **Import**.

## Paso 2 — Sube el archivo del Kit

1. Se abre la pantalla **Import a website template** (Importar una
   plantilla de sitio web).
2. Haz clic en la zona **Click to upload or drag and drop** y elige el
   archivo **VGV-FIT-ELITE-Kit.zip** de este paquete. También puedes
   arrastrarlo a esa zona.
3. Espera a que el archivo se cargue. No cierres la ventana.

## Paso 3 — Elige qué partes aplicar

1. Verás la pantalla **Select which parts you want to apply** (Elige qué
   partes quieres aplicar).
2. Deja marcadas **Content** (Contenido) y **Settings & configurations**
   (Ajustes y configuraciones): ya vienen marcadas.
3. **Templates** aparece sin marcar y con el botón **Upgrade**: eso es
   normal, es la parte Pro. **No hace falta** para esta plantilla: la
   página, las fotos y los estilos vienen en Content y Settings.
4. Haz clic en **Import and apply** (Importar y aplicar), abajo a la
   derecha.

El aviso de «versión anterior» también es normal: el Kit se exportó con
Elementor 4.4.1 e importa bien en 4.4.0 y 4.4.1.

## Paso 4 — Confirma que la importación terminó bien

Al terminar verás el mensaje de éxito (en inglés: *«Your website
template is now live on your site!»*; en español verás el texto
equivalente) y el resumen de lo importado: **Content: 1 Page | 1
Taxonomy**, **Templates: No templates imported** (normal, es la parte
Pro), **Site settings** con colores, fuentes y ajustes, y **Plugins: No
plugins imported** (la plantilla no necesita ningún plugin).

1. Haz clic en **Close** (Cerrar) para salir.
2. Ve a **Páginas** en el menú de WordPress: verás la página **VGV-FIT
   ELITE** publicada. Ábrela para verla.

## Paso 5 — Después de importar (3 pasos a mano)

**1. Poner la página como portada.** La importación crea la página pero
no la pone como inicio: si abres tu dominio verás la portada del blog.
Ve a **Ajustes > Lectura**, en «Tu página de inicio muestra» elige **Una
página estática**, en «Página de inicio» elige **VGV-FIT ELITE** y pulsa
**Guardar cambios**.

**2. Regenerar el CSS.** Ve a **Elementor > Herramientas**, pestaña
**General**, y pulsa el botón **Regenerate CSS & Data** (Regenerar CSS y
datos). Esto obliga a Elementor a reconstruir los estilos de la página
importada.

**3. Revisar la página.** Abre la página y desplázate por las 11
secciones: encabezado, portada, características, entrenador, servicios,
app, reto, precios, resultados, preguntas y contacto. Las fotos deben
verse todas; si alguna se ve como un cuadro gris, lee «Si algo no se ve
bien» abajo.

> **El menú y el logo ya vienen en la página.** El menú (Inicio,
> Entrenamientos, Planes, Resultados, Contacto) son botones dentro de la
> propia página, con enlaces a las secciones: **no necesitas crear un
> menú de WordPress** para que funcione. El logo también es una imagen
> dentro de la página (encabezado y pie): para cambiarlo, haz clic en la
> imagen en el editor y elige otra (ver la Guía de personalización). El
> logo de *Personalizar > Identidad del sitio* no afecta a esta página,
> porque usa la plantilla «Lienzo de Elementor».

## Si algo no se ve bien

- **Una foto se ve como cuadro gris o no carga:** casi siempre es que la
  descarga falló durante la importación (sin internet en ese momento, o
  el repositorio de fotos no estaba accesible). Vuelve a importar el
  Kit: Elementor reutiliza las fotos ya descargadas y completa las que
  falten. También puedes subir la foto a mano: clic en la imagen >
  *Choose Image* > elige el archivo de la carpeta Fotos/ de este
  paquete.
- **La página se ve sin estilos (todo blanco, sin colores):** regenera
  el CSS (Paso 5, punto 2) y recarga la página con Ctrl+F5.
- **Aparece el aviso de «versión anterior de Elementor»:** es normal y
  no impide nada. El Kit se exportó con Elementor 4.4.1 y se probó
  importando en 4.4.0 y 4.4.1.
- **«Templates» pide Pro:** es normal. La plantilla no usa plantillas de
  tema (encabezado/pie globales de Elementor Pro): el encabezado y el
  pie son secciones de la propia página.
- **El formulario de contacto:** la plantilla gratuita no trae widget de
  formulario (es de Pro). La sección de contacto lo explica en la propia
  página: instala un plugin gratuito de formularios (por ejemplo Contact
  Form 7 o WPForms Lite), crea tu formulario y agrega un widget de
  Shortcode en esa tarjeta con el shortcode. Mientras tanto, los botones
  de WhatsApp y correo funcionan.

## Qué se probó (y qué falta)

Este Kit se probó antes de entregarse: se importó el mismo archivo ZIP
en **dos instalaciones limpias** (WordPress 7.1.4 + Hello, con Elementor
4.4.1 y con 4.4.0) y los resultados fueron idénticos: 161 elementos, 36
animaciones, 14/14 fotos descargadas y verificadas byte a byte, colores
y fuentes globales, y página editable. Además se importó **por la
interfaz** en un WordPress Playground limpio y se revisó la página en
pantalla: filas de 4 y 3 columnas correctas, precios visibles, fotos
completas y paneles del editor funcionando. Las capturas y el informe
están en la carpeta **Evidencia/**.

Lo que **no** se pudo verificar en la prueba: la consola del navegador
(el navegador de prueba no tenía DevTools), el frontend móvil en una
ventana real de 390 px (se verificó con la vista previa móvil del
editor), y la importación en tu hosting real (Hostinger, MySQL,
español). **La prueba en tu staging es la prueba final:** si algo se ve
distinto allí, avísame con una captura y lo revisamos.

Antes de publicar, edita los textos marcados «EDITABLE» (WhatsApp,
correo, precios, biografía del entrenador, testimonios y políticas). La
Guía de personalización explica dónde está cada uno.
