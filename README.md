# NFT preview card component — Solución Frontend Mentor

Este repositorio contiene mi implementación de la tarjeta de vista previa NFT del reto de Frontend Mentor.

Enlaces
- Página de la solución en Frontend Mentor: https://www.frontendmentor.io/solutions/nft-preview-card-component-O8ZcjBWPTA
- Demo desplegado en Vercel: https://nft-preview-card-component-delta-five.vercel.app/

Descripción breve
-----------------
Componente responsive (HTML + CSS) que reproduce el diseño del reto: tarjeta con imagen principal, título, descripción, fila de precio/tiempo y sección del creador con avatar. Está construida con un enfoque mobile-first y variables CSS (`:root`) para tokens de color y tipografía.

Características implementadas
-----------------------------
- Variables CSS en `:root` basadas en el `style-guide.md` (colores primarios y neutrales, tamaños y tipografías).
- Fuente `Outfit` integrada (actualmente mediante `@import` en `styles/styles.css`).
- Layout mobile-first y responsivo; puntos de diseño considerados: 375px (móvil) y 1440px (desktop).
- Tarjeta (`.card`) estilizada con: fondo, borde sutil, sombra moderna, esquinas redondeadas y efecto de elevación en hover.
- Interacción de la imagen: overlay de color cian y aparición del icono central (`.eye-icon`) al hacer hover.
- Fila de precio y tiempo con íconos (`icon-ethereum.svg`, `icon-clock.svg`) y separación correcta.
- Sección del creador: avatar circular con borde blanco y texto secundario de menor tamaño (variable `--small-font-size`).
- Ajustes tipográficos (base en 18px) y utilidades para contrastes y accesibilidad visual.
- Ajustes de espaciado: márgenes y `gap` para que el título `Equilibrium #3429` tenga la misma separación superior/inferior con respecto a la imagen.

Archivos clave
-------------
- `index.html` — marcado de la tarjeta y referencia a los estilos.
- `styles/styles.css` — variables de diseño, reglas del componente y utilidades.
- `style-guide.md` — especificaciones del desafío (paleta de color, pesos tipográficos, tamaños de diseño).
- `images/` — todos los assets usados en la tarjeta (imagen principal, avatar, iconos, favicon).

Cómo ejecutar localmente
------------------------
Abrir `index.html` directamente funciona, pero para servir archivos estáticos de forma simple:

```bash
# desde la raíz del proyecto
python3 -m http.server 8000

# Abrir en el navegador:
http://localhost:8000
```

O usando `live-server`, `http-server` u otras utilidades similares.

Decisiones de implementación
---------------------------
- Uso de variables CSS: centralizan los tokens de color y tipografía para facilitar ajustes posteriores.
- Import de la tipografía: `@import` en el CSS por simplicidad; para producción recomiendo moverlo a un `<link rel="stylesheet">` en el `<head>` de `index.html` para mejor rendimiento.
- Sombra y borde de la tarjeta: se añadieron variables `--card-border` y `--card-shadow` para conseguir un aspecto moderno y reutilizable.
- Accesibilidad: se cuidó la relación de color para texto sobre el fondo de la tarjeta; no obstante es recomendable ejecutar una auditoría (Lighthouse / axe) para comprobar contraste y foco de teclado.

Problemas y aprendizajes
------------------------
- Afinar el espaciado vertical entre la imagen y el título requirió ajustar el `margin-bottom` del `h4` para que la separación superior e inferior fuese consistente con el `gap` del contenedor.
- Trabajar con imágenes y overlays llevó a usar pseudo-elementos (`::before`) y animaciones de opacidad para mantener el HTML limpio.

Mejoras pendientes (opcional)
-----------------------------
- Mover la carga de la fuente a un `<link>` en `index.html`.
- Añadir estilos de foco (keyboard) para la interactividad (ej. al tabular hasta el icono de vista).
- Añadir un pequeño script para abrir una vista modal con la imagen al hacer clic en el icono de vista.
- Añadir pruebas visuales o snapshots para validar cambios de estilo.

Licencia y créditos
-------------------
Este proyecto es la solución de un reto público de Frontend Mentor. Los recursos de imagen y los iconos provienen de la carpeta `images/` incluida en el reto.

Contacto / Demo
----------------
- Frontend Mentor solution: https://www.frontendmentor.io/solutions/nft-preview-card-component-O8ZcjBWPTA
- Demo en Vercel: https://nft-preview-card-component-delta-five.vercel.app/

- Mi usuario en Frontend Mentor: `@cristianbarreiro`
- Mi usuario en GitHub: `@cristianbarreiro`

Si quieres, puedo:
- añadir capturas (`preview.jpg`) y colocarlas en el README,
- cambiar `@import` por una etiqueta `<link>` en `index.html` y actualizarlo aquí,
- o preparar el deploy en GitHub Pages además de la versión en Vercel.

---

Gracias — dime si quieres que traduzca este README al inglés o que lo haga más corto para la descripción del repositorio.
- [Vercel](https://vercel.com/)
- [Netlify](https://www.netlify.com/)

You can host your site using one of these solutions or any of our other trusted providers. [Read more about our recommended and trusted hosts](https://medium.com/frontend-mentor/frontend-mentor-trusted-hosting-providers-bf000dfebe).

