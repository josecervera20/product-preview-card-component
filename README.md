# Frontend Mentor - Solución para Product preview card component

Esta es una solución al [desafío del componente de tarjeta de vista previa de producto en Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor desafíos te ayudan a mejorar tus habilidades de codificación construyendo proyectos realistas.

## Tabla de Contenidos 📋

- [Resumen 📝](#resumen-📝)
  - [El desafío](#el-desafío)
  - [Captura de pantalla 📸](#captura-de-pantalla-📸)
  - [Enlace 🔗](#enlace-🔗)
- [Mi Proceso 🚀](#mi-proceso-🚀)
  - [Construido con 🏗️](#construido-con-🏗️)
  - [Lo que aprendí 🧠](#lo-que-aprendí-🧠)
  - [Desarrollo Continuo 📈](#desarrollo-continuo-📈)
  - [Recursos Útiles 📚](#recursos-útiles-📚)
- [Autor 🧑‍💻](#autor-🧑‍💻)
- [Agradecimientos 🙌](#agradecimientos-🙌)

## Resumen 📝

### El desafío

Los usuarios deberían poder:

- Ver el diseño óptimo según el tamaño de la pantalla de su dispositivo.
- Ver los estados de hover para elementos interactivos.

### Captura de pantalla 📸

![Captura de pantalla de la solución de Product preview card component](./design/desktop-design.jpg)

### Enlace 🔗

- URL de la Solución (Repositorio): [https://github.com/josecervera20/product-preview-card-component](https://github.com/josecervera20/product-preview-card-component)

## Mi Proceso 🚀

### Construido con 🏗️

- Marcado semántico HTML5
- Propiedades personalizadas de CSS (Variables CSS)
- **CSS Grid** (para la maquetación principal del componente y la alineación de elementos internos)
- Flujo de trabajo mobile-first
- **Google Fonts: Montserrat** (pesos 500, 700) y **Fraunces** (peso 700)

### Lo que aprendí 🧠

Durante este proyecto, consolidé y profundicé en varias áreas clave del desarrollo frontend:

- **Maquetación responsiva con CSS Grid:** Utilicé CSS Grid para estructurar el contenedor principal (`.main`), permitiendo un layout fluido que se transforma de una columna (móvil) a dos columnas (escritorio) de forma eficiente. Esto fue crucial para posicionar la imagen y el bloque de texto de lado a lado, así como para la alineación interna de elementos como el botón.

  ```css
  /* Maquetación móvil */
  .main {
    display: grid;
    grid-template-columns: 1fr;
  }

  /* Maquetación escritorio */
  @media (min-width: 667px) {
    .main {
      grid-template-columns: 1fr 1fr;
    }
  }

  /* Alineación de elementos internos (ej. el botón) */
  .main__cta {
    display: grid;
    grid-auto-flow: column;
    grid-auto-columns: max-content;
    justify-content: center;
    gap: 1em;
  }
  ```

- **Manejo de imágenes de fondo responsivas:** Implementé las imágenes del producto utilizando `background-image` y `background-size: cover` en un `div` (`.main__bg`), cambiando la fuente de la imagen con media queries para optimizar la carga y visualización en diferentes dispositivos.

  ```css
  .main__bg {
    background-image: url("../images/image-product-mobile.jpg");
  }

  @media (min-width: 667px) {
    .main__bg {
      background-image: url("../images/image-product-desktop.jpg");
    }
  }
  ```

- **Implementación de estados interactivos (`:hover`):** Añadí un efecto de transición suave y un cambio de color al pasar el ratón (`:hover`) al botón "Add to Cart", mejorando la experiencia del usuario.

  ```css
  .main__cta {
    transition: background-color 0.3s ease;
  }

  .main__cta:hover {
    background-color: hsl(158, 36%, 20%);
    cursor: pointer;
  }
  ```

- **Uso de pseudo-elementos (`::before`):** Utilicé `::before` para insertar el icono del carrito en el botón de forma eficiente, controlando su apariencia con CSS.

### Desarrollo Continuo 📈

En futuros proyectos, me gustaría seguir profundizando en:

- **Accesibilidad (ARIA attributes y semántica avanzada):** Asegurarme de que todos los elementos interactivos y gráficos (como la imagen de fondo de producto) tengan la información adecuada para lectores de pantalla.
- **Optimización de rendimiento:** Explorar técnicas más avanzadas para la optimización de imágenes (ej. `srcset` con `sizes` en HTML para `<img>` tags, o formatos de imagen modernos como WebP) y la carga de fuentes.
- **Transiciones y animaciones más complejas:** Experimentar con transiciones más sofisticadas o animaciones CSS para elementos UI.

### Recursos Útiles 📚

- [Frontend Mentor](https://www.frontendmentor.io/) - Una plataforma excelente para desafíos de codificación.
- [The Markdown Guide](https://www.markdownguide.org/) - Una referencia útil para la sintaxis de Markdown.
- [MDN Web Docs](https://developer.mozilla.org/es/docs/Web) - Siempre una fuente invaluable para entender propiedades CSS y el funcionamiento de HTML.
- [CSS-Tricks: A Complete Guide to CSS Grid](https://www.google.com/search?q=https://css-tricks.com/snippets/css/a-complete-guide-to-css-grid/) - Un recurso fundamental para entender y aplicar CSS Grid.

## Autor 🧑‍💻

- GitHub - [@josecervera20](https://github.com/josecervera20)

## Agradecimientos 🙌

Agradezco a la comunidad de Frontend Mentor por proporcionar desafíos tan valiosos que me permiten mejorar mis habilidades y construir proyectos realistas. También a los recursos en línea como MDN y guías de CSS por ser fuentes invaluables durante el desarrollo.
