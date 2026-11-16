# Nota — no hay archivo CSS personalizado

Esta plantilla **no tiene ningún archivo CSS personalizado**. No se
inventó ninguno para esta carpeta: todo el estilo vive dentro de los
archivos JSON del Kit, en los ajustes de Elementor.

## Dónde vive cada estilo

- **Colores y tipografías globales**: `../kit-elementor/site-settings.json`
  (secciones `system_colors`, `custom_colors` y `system_typography`).
  Se aplican al importar el Kit con Content + Settings y se editan en
  el editor de Elementor en Ajustes del sitio > Colores globales y
  Fuentes globales.
- **Estilos de cada elemento** (fondos, bordes, rellenos, anchos,
  alineación, animaciones): en los `settings` de cada uno de los 161
  elementos de `../kit-elementor/content/page/5.json`.
- **Sin clases globales**: `../kit-elementor/global-classes.json` está
  vacío; la plantilla no usa clases globales.
- **Sin CSS personalizado por elemento**: ningún elemento usa la opción
  de CSS personalizado (que además exige Elementor Pro). Todo se logra
  con los controles nativos gratuitos.

## Colores globales (exactos, de `site-settings.json`)

### Colores del sistema

| ID | Título | Color |
|---|---|---|
| `primary` | Primary | `#F97316` |
| `secondary` | Secondary | `#101010` |
| `text` | Text | `#FFFFFF` |
| `accent` | Accent | `#EA580C` |

### Colores personalizados

| ID | Título | Color |
|---|---|---|
| `c_deep` | Negro profundo | `#080808` |
| `c_card` | Negro tarjeta | `#1B1B1B` |
| `c_grey` | Gris secundario | `#B3B3B3` |
| `c_border` | Borde | `#2A2A2A` |

## Tipografías globales (exactas, de `site-settings.json`)

| ID | Título | Fuente | Peso | Tamaño | Interlineado | Otros |
|---|---|---|---|---|---|---|
| `primary` | Primary | Anton | 400 | 48 px | 1.15 em | — |
| `secondary` | Secondary | Anton | 400 | 28 px | 1.2 em | — |
| `text` | Text | Inter | 400 | 17 px | 1.7 em | — |
| `accent` | Accent | Inter | 600 | 15 px | — | Mayúsculas, espaciado 2 px |

Fuentes genéricas por defecto: `Inter, sans-serif`. No hay tipografías
personalizadas (`custom_typography` está vacío).
