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

## Create a custom `README.md`

We strongly recommend overwriting this `README.md` with a custom one. We've provided a template inside the [`README-template.md`](./README-template.md) file in this starter code.

The template provides a guide for what to add. A custom `README` will help you explain your project and reflect on your learnings. Please feel free to edit our template as much as you like.

Once you've added your information to the template, delete this file and rename the `README-template.md` file to `README.md`. That will make it show up as your repository's README file.

## Submitting your solution

Submit your solution on the platform for the rest of the community to see. Follow our ["Complete guide to submitting solutions"](https://medium.com/frontend-mentor/a-complete-guide-to-submitting-solutions-on-frontend-mentor-ac6384162248) for tips on how to do this.

Remember, if you're looking for feedback on your solution, be sure to ask questions when submitting it. The more specific and detailed you are with your questions, the higher the chance you'll get valuable feedback from the community.

## Sharing your solution

There are multiple places you can share your solution:

1. Share your solution page in the **#finished-projects** channel of the [community](https://www.frontendmentor.io/community). 
2. Tweet [@frontendmentor](https://twitter.com/frontendmentor) and mention **@frontendmentor**, including the repo and live URLs in the tweet. We'd love to take a look at what you've built and help share it around.
3. Share your solution on other social channels like LinkedIn.
4. Blog about your experience building your project. Writing about your workflow, technical choices, and talking through your code is a brilliant way to reinforce what you've learned. Great platforms to write on are [dev.to](https://dev.to/), [Hashnode](https://hashnode.com/), and [CodeNewbie](https://community.codenewbie.org/).

We provide templates to help you share your solution once you've submitted it on the platform. Please do edit them and include specific questions when you're looking for feedback. 

The more specific you are with your questions the more likely it is that another member of the community will give you feedback.

## Got feedback for us?

We love receiving feedback! We're always looking to improve our challenges and our platform. So if you have anything you'd like to mention, please email hi@frontendmentor.io.

This challenge is completely free. Please share it with anyone who will find it useful for practice.

**Have fun building!** 🚀
