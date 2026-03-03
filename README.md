# Landing Pages — Menú / Índice

Página de inicio tipo portafolio que centraliza el acceso a las **15 landing pages** del proyecto. Diseño editorial oscuro con grid de tarjetas, animaciones y cursor personalizado.

---

## Archivos

```
index.html   ← Estructura y contenido del menú
index.css    ← Todos los estilos, animaciones y responsive
```

Ambos archivos deben estar en la misma carpeta, al mismo nivel que `LandindPages/`.

```
📁 proyecto/
├── index.html
├── index.css
└── LandindPages/
    ├── page3/
    ├── page4/
    ├── page6/
    └── ...
```

---

## Cómo usar

1. Coloca `index.html` e `index.css` en la raíz del proyecto
2. Abre `index.html` en el navegador
3. Haz clic en cualquier tarjeta para abrir la landing correspondiente

No requiere servidor ni instalación. Funciona abriendo el archivo directamente en el navegador.

---

## Características del menú

**Grid de tarjetas**
15 tarjetas, una por landing page. Dos tarjetas son `featured` (doble ancho) para romper la monotonía del grid. Cada tarjeta muestra el número de página, título, descripción y tags de categoría.

**Colores por página**
Cada tarjeta tiene un gradiente único que representa visualmente la temática de esa landing (oscuros para tech, verdes para naturaleza, cálidos para diseño, etc.).

**Cursor personalizado**
En desktop aparece un cursor circular verde (`#c8f060`) con un anillo exterior con lag suave. Al hacer hover sobre una tarjeta cambia a naranja y se expande. En móvil se desactiva automáticamente.

**Animaciones**
Las tarjetas aparecen con un `fadeUp` escalonado al cargar la página. Las previews hacen zoom suave en hover. La flecha `↗` de cada tarjeta se revela solo en hover.

**Barra de filtros**
Botones de categoría en la parte superior (All, Design, Tech, Lifestyle, Editorial, Product). Actualmente son visuales — se pueden conectar a lógica de filtrado JS si se necesita.

---

## Responsive

| Breakpoint | Comportamiento |
|------------|----------------|
| `> 900px` | Grid multi-columna, tarjetas featured en doble ancho |
| `≤ 900px` | Featured vuelven a ancho simple, padding reducido |
| `≤ 600px` | Grid de 1 columna, header en vertical, cursor desactivado |

---

## Tecnologías

- HTML5 semántico
- CSS3 — Custom Properties, Grid, Flexbox, `@keyframes`, `clamp()`
- Google Fonts — [Syne](https://fonts.google.com/specimen/Syne) + [DM Sans](https://fonts.google.com/specimen/DM+Sans)
- JavaScript vanilla — solo para el cursor personalizado (animación con `requestAnimationFrame`)

---

## Personalización rápida

**Cambiar colores del tema** — editar las variables en `:root` en `index.css`:
```css
--accent: #c8f060;   /* verde lima — color principal */
--accent2: #ff6b35;  /* naranja — hover del cursor */
--bg: #0d0d0d;       /* fondo oscuro */
```

**Cambiar el gradiente de una tarjeta** — editar el `style` inline del `.card-preview-bg` en `index.html`:
```html
<div class="card-preview-bg" style="background: linear-gradient(...)">
```

**Agregar una página nueva** — duplicar un bloque `.card` en el HTML y actualizar el `href`, número, título y gradiente.

---

*Menú de portafolio — HTML & CSS — 2024*