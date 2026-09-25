# TP: HTML y CSS — Bloques 1, 2 y 3

Licenciatura en Sistemas de Información — Diseño UX-UI 2026

## Ejercicios resueltos

### Bloque 1 — Nivel Básico

Se resolvieron todos los ejercicios del Bloque 1, **excepto el Ejercicio 2**:

- **Ejercicio 1** — Estructura HTML básica
- **Ejercicio 3** — Tabla de datos (horario semanal)
- **Ejercicio 4** — Formulario simple
- **Ejercicio 5** — Primeros estilos CSS
- **Ejercicio 6** — Selectores CSS
- **Ejercicio 7** — Modelo de caja (Box Model)

### Bloque 2 — Nivel Intermedio

Se resolvieron todos los ejercicios del Bloque 2:

- **Ejercicio 8** — Flexbox: barra de navegación
- **Ejercicio 9** — Flexbox: galería de tarjetas
- **Ejercicio 10** — CSS Grid: layout de página
- **Ejercicio 11** — Pseudo-clases y pseudo-elementos
- **Ejercicio 12** — Posicionamiento
- **Ejercicio 13** — Formulario estilizado
- **Ejercicio 14** — Variables CSS y temas

### Bloque 3 — Nivel Medio/Avanzado

Se resolvieron todos los ejercicios del Bloque 3:

- **Ejercicio 15** — Diseño responsivo con Media Queries
- **Ejercicio 16** — Animaciones con @keyframes
- **Ejercicio 17** — Menú responsivo tipo "hamburguesa" (solo CSS)
- **Ejercicio 18** — Grid avanzado: galería tipo mosaico
- **Ejercicio 19** — Formulario multi-step con validación visual
- **Ejercicio 20** — Proyecto integrador: Landing Page completa

Cada ejercicio está en su propia carpeta, con `index.html` y `styles.css`
separados, tal como piden las instrucciones generales.

## Decisiones de diseño

- **Ejercicio 5** reutiliza el HTML del Ejercicio 1 (misma estructura e
  imagen) y le agrega una hoja de estilos propia, ya que la consigna pide
  aplicar CSS "a la página del Ejercicio 1".
- Se usó una paleta de color consistente en todos los ejercicios
  (`#2C3E50` como color primario, `#3E8E7E` como acento) para dar
  coherencia visual al conjunto, sin que esto sea un requisito explícito
  de la consigna.
- En el Ejercicio 3, la fila `rowspan="2"` en la columna del lunes
  representa una clase de Algoritmos que ocupa dos franjas horarias
  seguidas, y el `tfoot` usa `colspan="6"` para el total de horas.
- En el Ejercicio 6 se usaron tres tipos de selectores distintos:
  ID (`#intro`), clase (`.card`, `.destacado`) y descendiente
  (`.card h2`, `.card p`).
- En el Ejercicio 7 se aplicó `box-sizing: border-box` de forma global
  (`*`) para que `padding` y `border` no alteren el ancho definido en
  `.card`, logrando que las tres tarjetas midan exactamente lo mismo.
- En el Ejercicio 9, las "tarjetas de producto" se enmarcaron como una
  tienda de accesorios para programadores (teclado, mouse, auriculares,
  monitor, taza, cuaderno) para mantener la temática del TP; cada imagen
  es un SVG simple generado localmente.
- En el Ejercicio 12, el tooltip usa `position: relative` en
  `.tooltip-contenedor` como referencia para el `position: absolute` del
  `.tooltip`, y el botón "volver arriba" usa `position: fixed` con
  `z-index` más alto para quedar siempre por encima del contenido.
- En el Ejercicio 13 se retomó exactamente el HTML del formulario del
  Ejercicio 4, agregando solo estilos (bordes redondeados, `:focus`,
  `:hover`, `:active` y `transition`), sin modificar su estructura.
- En el Ejercicio 14, el "modo oscuro" se resuelve sin JavaScript: un
  checkbox oculto (`#modo-oscuro`) redefine las variables CSS de
  `.pagina` mediante el combinador de hermanos (`~`) cuando está
  marcado, siguiendo el mismo espíritu "solo CSS" que pide el
  Ejercicio 17 del Bloque 3.
- En el Ejercicio 15 se adaptó el layout exacto del Ejercicio 10, con
  enfoque **desktop-first**: se justificó esta elección porque el
  layout ya estaba pensado para escritorio, así que se parte de esos
  estilos y se van "recortando" con `max-width` a medida que se achica
  la pantalla, en dos breakpoints (768px y 480px).
- En el Ejercicio 16 se combinaron dos animaciones para cubrir ambas
  variantes de la consigna: un spinner en loop infinito y tarjetas con
  fade-in + slide-up que aparecen una sola vez, con `animation-delay`
  escalonado por tarjeta.
- En el Ejercicio 17, el menú hamburguesa reutiliza el truco del
  checkbox oculto (`input[type="checkbox"]` + combinador `~`) igual que
  el Ejercicio 14, pero aplicado a `max-height` para animar la apertura
  del menú en pantallas chicas.
- En el Ejercicio 18, el elemento `.grande` usa `grid-column: span 2` y
  `grid-row: span 2` sobre una base de `repeat(auto-fill, minmax(...))`
  con `grid-auto-flow: dense`, para que el resto de las imágenes rellene
  los huecos automáticamente.
- En el Ejercicio 19, la navegación entre pasos se resolvió con radio
  buttons ocultos (en vez de `:target`) porque no depende de que la URL
  cambie; la validación visual usa `:required:not(:placeholder-shown)`
  junto con `:valid`/`:invalid` para no mostrar los bordes en rojo antes
  de que la persona empiece a escribir.
- El Ejercicio 20 integra Flexbox (navbar, tarjetas) y Grid (sección de
  servicios) combinados, variables CSS heredadas de los ejercicios
  anteriores, dos media queries (900px y 600px), una animación de
  entrada (`@keyframes aparecer`, reutilizada del Ejercicio 16) y un
  carrusel de testimonios con `scroll-snap-type: x mandatory`. El CSS
  quedó dividido en secciones comentadas (variables, header, hero,
  servicios, testimonios, contacto, footer, media queries) según pide
  el criterio de organización.

## Pendiente

El Ejercicio 2 (listas y enlaces) no forma parte de esta entrega.
