# JD Repair - Página Web

## Descripción General

Este repositorio contiene el proyecto de una página web estática profesional para **JD Repair**, una empresa ficticia dedicada a servicios y repuestos John Deere. El desarrollo de este sitio es parte de la **Actividad 2, 3 y 4 del III Corte** de la materia Computación III, siguiendo los lineamientos académicos para la creación de sitios web modernos, accesibles y visualmente atractivos.

---

## Índice

- [Estructura del Proyecto](#estructura-del-proyecto)
- [Requisitos de la Actividad](#requisitos-de-la-actividad)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Explicación del Código](#explicación-del-código)
  - [HTML](#html)
  - [CSS](#css)
  - [Animaciones y Librerías](#animaciones-y-librerías)
- [Diseño Responsivo](#diseño-responsivo)
- [Cómo Ejecutar el Proyecto](#cómo-ejecutar-el-proyecto)

---

## Estructura del Proyecto

```
proyecto_jd_repair/
│
├── index.html
├── about.html
├── services.html
├── parts.html
├── contact.html
│
├── css/
│   └── style.css
│
└── assets/
    └── images/
        ├── logo-jd-placeholder.png
        ├── hero-bg-jd.jpg
        ├── about-team.jpg
        ├── about-workshop.jpg
        ├── map-placeholder.png
        ├── service-engine.jpg
        ├── service-transmission.jpg
        ├── service-hydraulics.jpg.jpg
        ├── service-maintenance.jpg
        ├── parts-engine-components.jpg
        ├── parts-filters.jpg
        ├── parts-oils.jpg
        └── parts-general.jpg
```

---

## Requisitos de la Actividad

### III CORTE "ACTIVIDAD 2" - **Estructura básica y Contenido Estático**

- **Sobre nosotros:** Historia y valores de la empresa.
- **Servicios:** Detalle de los servicios ofrecidos.
- **Experiencia/Trabajos realizados:** Trayectoria y logros.
- **Testimonios de clientes:** Opiniones reales o ficticias.
- **Contacto:** Formulario y datos de contacto.

**Investigación previa:**  
- HTML básico: etiquetas, estructura, imágenes, enlaces.
- Organización de archivos y carpetas.

---

### III CORTE "ACTIVIDAD 3" - **Estilo y diseño con CSS**

- Aplicación de estilos personalizados.
- Diseño visualmente agradable y profesional.
- Inspiración en páginas web reales.
- Investigación sobre CSS, selectores, box model, colores y fuentes.

---

### III CORTE "ACTIVIDAD 4" - **Diseño responsivo**

- Uso de media queries para adaptar el diseño a diferentes dispositivos.
- Experiencia de usuario óptima en móviles, tablets y escritorio.

---

## Tecnologías Utilizadas

- **HTML5:** Estructura semántica y accesible.
- **CSS3:** Estilos modernos, gradientes, sombras, tipografía Montserrat.
- **Font Awesome:** Iconografía profesional.
- **[AOS.js](https://michalsnik.github.io/aos/):** Animaciones al hacer scroll.
- **[Swiper.js](https://swiperjs.com/):** Slider de testimonios.
- **Google Fonts:** Fuente Montserrat para una apariencia moderna.

---

## Explicación del Código

### HTML

Cada página (`index.html`, `about.html`, `services.html`, `parts.html`, `contact.html`) sigue una estructura clara y semántica:

- `<header>`: Barra de navegación sticky con logo y menú.
- `<section>`: Diferentes bloques para hero, servicios, repuestos, equipo, testimonios, contacto, etc.
- `<footer>`: Información legal, enlaces rápidos y redes sociales.

**Ejemplo de estructura básica:**
```html
<header class="header">
  <nav class="navbar">
    <div class="logo">
      <a href="index.html"><img src="assets/images/logo-jd-placeholder.png" alt="JD Repair Logo"></a>
    </div>
    <ul class="nav-menu">
      <li><a href="index.html" class="active"><i class="fas fa-home"></i> Inicio</a></li>
      <!-- ...otros enlaces... -->
    </ul>
  </nav>
</header>
```

### CSS

- **Reset y fuentes:** Uso de `box-sizing: border-box` y fuente Montserrat importada de Google Fonts.
- **Colores y gradientes:** Paleta basada en los colores de John Deere (verde y amarillo).
- **Sombras y bordes:** Para dar profundidad y modernidad.
- **Botones y tarjetas:** Microinteracciones, transiciones y efectos hover.
- **Separadores visuales:** `.section-divider` para dividir secciones de forma elegante.
- **Responsive:** Media queries para adaptar el diseño a cualquier pantalla.

**Ejemplo de gradiente y tipografía:**
```css
body {
  font-family: 'Montserrat', 'Segoe UI', Arial, sans-serif;
  background: linear-gradient(135deg, #f7f7f7 0%, #e6f5d6 100%);
  color: #222;
}
```

### Animaciones y Librerías

- **AOS.js:**  
  Permite animar la aparición de secciones y tarjetas al hacer scroll, mejorando la experiencia visual.
  ```html
  <section class="features" data-aos="fade-up">
    <!-- contenido -->
  </section>
  ```
  ```js
  <script>
    AOS.init({ duration: 900, once: true });
  </script>
  ```

- **Swiper.js:**  
  Slider profesional para testimonios, adaptable y táctil.
  ```html
  <div class="swiper testimonials-swiper">
    <div class="swiper-wrapper">
      <div class="swiper-slide testimonial">...</div>
      <!-- más slides -->
    </div>
    <div class="swiper-pagination"></div>
  </div>
  ```
  ```js
  <script>
    const swiper = new Swiper('.testimonials-swiper', {
      loop: true,
      autoplay: { delay: 5000, disableOnInteraction: false },
      pagination: { el: '.swiper-pagination', clickable: true },
      slidesPerView: 1,
      spaceBetween: 30,
      breakpoints: {
        700: { slidesPerView: 2 },
        1000: { slidesPerView: 3 }
      }
    });
  </script>
  ```

---

## Diseño Responsivo

El sitio utiliza **media queries** para asegurar que todos los elementos se adapten perfectamente a pantallas de escritorio, tablets y móviles.  
Las tarjetas, menús y formularios cambian de tamaño y disposición para garantizar la mejor experiencia de usuario en cualquier dispositivo.

**Ejemplo:**
```css
@media (max-width: 900px) {
  .features, .services-grid, .parts-grid {
    flex-direction: column;
    align-items: center;
  }
}
```

---

## Cómo Ejecutar el Proyecto

1. **Descarga o clona este repositorio.**
2. Abre la carpeta `proyecto_jd_repair` en tu editor favorito (Visual Studio Code recomendado).
3. Abre `index.html` en tu navegador.
4. Navega entre las páginas usando el menú superior.

**No se requiere servidor web ni instalación adicional. Todo funciona de manera local.**

---

¡Este proyecto demuestra el dominio de HTML, CSS, organización de archivos, diseño responsivo y el uso de librerías modernas para crear una web profesional y atractiva!
