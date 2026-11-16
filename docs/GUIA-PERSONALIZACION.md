# VGV-FIT ELITE 1.0 — Guía de personalización (Kit v7)

Cómo cambiar fotos, textos, precios, enlaces y colores.
Todo se edita con clics en el editor de Elementor, sin código.

> Versión en Markdown del documento `Guia-Personalizacion.pdf` (4
> páginas). El contenido es el mismo. Las versiones PDF se suben por
> separado a este repositorio (ver `NOTA.md` en esta carpeta).

## 1. Las fotos: 14 espacios, 13 archivos

La página tiene 14 espacios de imagen. El logo se usa en 2 sitios, por
eso son 13 archivos. Para reemplazar una foto, usa una imagen con las
**mismas medidas** (o la misma proporción) de la tabla: así no se
deforma nada.

| # | Espacio | Archivo | Medidas (px) |
|---|---|---|---|
| 1 | Encabezado — logo | logo-horizontal-600x200.webp | 600 × 200 |
| 2 | Portada — foto principal | hero-principal-1600x1200.webp | 1600 × 1200 |
| 3 | Entrenador — foto | entrenador-900x1200.webp | 900 × 1200 |
| 4–7 | Servicios — 4 tarjetas | servicio-\*.webp (4 archivos) | 800 × 600 c/u |
| 8–9 | App — 2 teléfonos | mockup-movil-\*.webp (2 archivos) | 900 × 1600 c/u |
| 10 | Reto Elite — dominadas | promo-dominadas-1600x600.webp | 1600 × 600 |
| 11–13 | Resultados — 3 testimonios | resultado-\*.webp (3 archivos) | 800 × 800 c/u |
| 14 | Pie de página — logo | logo-horizontal-600x200.webp | 600 × 200 |

El mapa completo con URL del CDN y SHA-256 de cada archivo está en
`../assets/images/MAPA-IMAGENES.md`.

### Cómo reemplazar una foto

1. Abre la página con **Editar con Elementor**.
2. Haz **clic en la foto** que quieres cambiar. Se abre su panel a la
   izquierda (en inglés: *Edit Image*; en las tarjetas de servicios, el
   panel de la caja de imagen).
3. Pulsa **Choose Image** (Elegir imagen), sube la nueva foto o elígela
   de la Biblioteca de medios y confirma.
4. Pulsa **Actualizar** (*Update*) arriba a la derecha. No hace falta
   tocar ningún otro ajuste.

### Notas sobre las fotos

- El logo tiene **fondo transparente**. Si lo reemplazas, usa un PNG o
  WebP con fondo transparente para que se vea bien sobre el fondo negro.
  Cambia los 2 logos (encabezado y pie) para que coincidan.
- Los 2 mockups de teléfono dicen «MOCKUP DEMO»: reemplázalos con
  **capturas reales de la app** antes de publicar.
- Las fotos de servicios llenan el ancho de su tarjeta. Si tu foto es
  de otra proporción, se verá recortada o con espacios: respeta
  800 × 600.
- La foto de la entrenadora es vertical (900 × 1200) y más alta que el
  texto vecino: es el diseño aprobado. Si prefieres otra proporción,
  cambia la foto por una con la misma proporción vertical.

## 2. Textos, botones y enlaces

### Cómo cambiar un texto

1. En el editor, haz clic en el título o el párrafo. Se abre su panel.
2. Escribe el texto nuevo en el campo del panel (o haz clic directamente
   sobre el texto en la página y escribe).
3. Pulsa **Actualizar**.

### Textos que debes cambiar antes de publicar (dicen «EDITABLE» o van entre corchetes)

- **Biografía del entrenador** y nombre, formación y experiencia
  (sección «Entrenador profesional»).
- **Testimonios**: nombres y textos de los 3 clientes (sección
  «Resultados»).
- **Respuestas de preguntas frecuentes** (sección «Preguntas
  frecuentes»).
- **Precios y funciones de los planes**: Básico $19.99, Premium $29.99,
  Elite $39.99 son precios de demostración.
- **WhatsApp, correo e Instagram** en Contacto y en el pie de página
  (ver abajo).
- **Política de privacidad y Términos y condiciones** en el pie de
  página, y el año y nombre comercial del copyright («© 2026 VGV
  Technology»).

### Cómo cambiar un enlace de un botón

1. Haz clic en el botón. En su panel, busca el campo **Enlace**
   (*Link*).
2. Escribe la dirección nueva y pulsa **Actualizar**.

### Enlaces que trae la plantilla

- **Menú y botones de sección:** enlaces internos a las secciones de la
  misma página: #inicio, #entrenamientos, #planes, #resultados,
  #contacto. Funcionan sin tocar nada.
- **Escribir por WhatsApp:** https://wa.me/573000000000 con un mensaje
  predefinido. **Cambia el número** por el real (código de país +
  número, sin «+» ni espacios).
- **Enviar correo:** mailto:correo@ejemplo.com. **Cambia el correo** por
  el real.
- **ACCEDER A MI CUENTA:** hoy enlaza a #contacto (es un marcador de
  posición: la plantilla no trae sistema de cuentas). Apúntalo a la
  dirección real de acceso de tu app o tu sistema cuando la tengas.
- **Iconos de redes** (Instagram, Facebook, YouTube, TikTok) en Contacto
  y en el pie: haz clic en el widget de iconos sociales y edita cada
  enlace con la dirección real de cada red. El texto «Instagram:
  @tu_cuenta» también debe cambiarse.

## 3. Colores y fuentes globales

Toda la página usa los colores y fuentes globales del Kit: si los
cambias en un solo sitio, cambian en toda la página. En el editor, abre
**Ajustes del sitio** (el icono de engranaje / *Site Settings*, arriba a
la izquierda) y entra en **Colores globales** y **Fuentes globales**.

| Color | Código | Dónde se usa |
|---|---|---|
| Principal (naranja) | #F97316 | Botones, acentos, iconos |
| Secundario (negro) | #101010 | Fondos de sección |
| Texto | #FFFFFF | Títulos y párrafos |
| Acento (naranja oscuro) | #EA580C | Detalles y hover |
| Fondo profundo | #080808 | Fondo general |
| Tarjeta | #1B1B1B | Fondo de tarjetas |
| Gris | #B3B3B3 | Textos secundarios |
| Borde | #2A2A2A | Bordes de tarjetas |

Fuentes: **Anton** para títulos y **Inter** para textos y botones. Si
cambias una fuente global, revisa que los títulos largos sigan cabiendo
en su espacio.

Los valores exactos (incluidos tamaños e interlineados) están en
`../assets/css/NOTA.md` y en `../kit-elementor/site-settings.json`.

## 4. Planes y precios

Las 3 tarjetas de «Planes y precios» son contenedores con títulos,
listas y botones (no es el widget de tabla de precios de Pro: todo es
editable con Elementor gratuito). Para cambiar un precio, haz clic en el
número ($19.99, $29.99 o $39.99) y escribe el nuevo. Para cambiar las
funciones, haz clic en la lista de cada tarjeta. El sello «MÁS POPULAR»
y el borde naranja de la tarjeta Premium se editan igual: clic en el
elemento y cambia el texto o el estilo. Los botones «ELEGIR PLAN» hoy
enlazan a #contacto: apúntalos a tu página de pago o registro cuando la
tengas.

## 5. Cómo se ve en celular y tableta

La página es responsive: en tableta y celular las filas pasan a una
sola columna, el menú se apila botón por botón y las fotos ocupan el
ancho completo. Esto se verificó con la vista previa «Mobile Portrait»
del editor (captura en la carpeta Evidencia). Para revisarlo tú: en el
editor, usa los iconos de **escritorio / tableta / móvil** de la barra
superior y desplázate por la página. Si editas algo en vista móvil, el
cambio solo afecta a esa vista: no rompe la vista de escritorio.

## 6. Animaciones

36 elementos tienen animación de entrada (32 *fadeInUp* y 4 *fadeIn*, 3
de ellas lentas en las fotos grandes). Cada animación se dispara **una
sola vez** cuando el elemento entra en pantalla al hacer scroll: no se
repiten. Si una animación te molesta, selecciónala en el editor, abre la
pestaña **Avanzado** y en **Motion Effects / Entrance Animation** elige
«None» (Ninguna). No quites las animaciones de las 3 tarjetas de precios
sin probar: llevan la animación del contenedor y sin ella se ven igual,
pero el cambio debe revisarse en pantalla.

## 7. Lista de revisión antes de publicar

- Número de WhatsApp real y correo real en Contacto, pie de página y
  botones.
- Precios y funciones de los planes reales; botones ELEGIR PLAN
  apuntando a donde deben ir.
- Biografía, nombre y datos del entrenador reales; testimonios reales
  con permiso de los clientes.
- Respuestas de preguntas frecuentes escritas; políticas de privacidad y
  términos enlazados o escritos.
- Logo propio en encabezado y pie (si aplica); mockups de teléfono
  reemplazados por capturas reales.
- Revisar la página en celular (vista previa móvil del editor) y en
  escritorio después de cada cambio grande.
- Si vas a **vender** esta plantilla a terceros, lee antes
  **Licencias.pdf**: las fotos de IA que trae tienen condiciones que
  debes conocer.
