<script>
  // @ts-nocheck
  import { onMount } from 'svelte';
  import { writable } from 'svelte/store';

  // Imagen actual visible
  let currentImage = 0;
  let currentIndex = 0;

  onMount(() => {
    const container = document.querySelector('.carousel-pc');
    const items = document.querySelectorAll('.gallery-pc-item');
    const nextBtn = document.querySelector('.carousel-pc-btn.next');
    const prevBtn = document.querySelector('.carousel-pc-btn.prev');

    if (!container || !items || !nextBtn || !prevBtn) {
      console.error('Uno o más elementos del DOM no se encontraron');
      return;
    }

    function updateCarousel() {
      const offset = -currentIndex * 100;
      container.style.transform = `translateX(${offset}%)`;
    }

    nextBtn.addEventListener('click', () => {
      currentIndex = (currentIndex + 1) % items.length;
      updateCarousel();
    });

    prevBtn.addEventListener('click', () => {
      currentIndex = (currentIndex - 1 + items.length) % items.length;
      updateCarousel();
    });

    updateCarousel();

    // Limpieza para evitar fugas de memoria
    return () => {
      nextBtn.removeEventListener('click', updateCarousel);
      prevBtn.removeEventListener('click', updateCarousel);
    };
  });

  function moveCarouselMobile(id, direction) {
    const carousel = document.getElementById(`carousel-${id}`);
    const scrollAmount = 220; // Ancho de una imagen más margen

    carousel.scrollBy({
      left: scrollAmount * direction,
      behavior: 'smooth',
    });
  }

  // Cambia la imagen actual según la dirección
  function moveCarousel(direction) {
    currentImage += direction;

    if (currentImage < 0) {
      currentImage = imagenesGestion.length - 1; // Volver al último
    } else if (currentImage >= imagenesGestion.length) {
      currentImage = 0; // Volver al primero
    }
  }

    const imagenes = [
      {
        src: "/images/pediloSimple/inicio.png",
        alt: "Pantalla de inicio",
        descripcion: "Pantalla de inicio con descripcion del proyecto"
      },
      {
        src: "/images/pediloSimple/ventajas.png",
        alt: "Ventajas del servicio",
        descripcion: "Ventajas del servicio de pedidos"
      },
      {
        src: "/images/pediloSimple/registro.png",
        alt: "Registro de usuarios",
        descripcion: "Formulario de registro para usuarios con autenticacion"
      },
    ];
  
    const imagenesAdmin = [
      {
        src: "/images/admin-canchas/inicio.png",
        alt: "Pantalla de inicio",
        descripcion: "Pantalla de inicio con resumen de reservas"
      },
      {
        src: "/images/admin-canchas/reservas.png",
        alt: "Reserva de cancha",
        descripcion: "Proceso de reserva de cancha paso a paso"
      },
      {
        src: "/images/admin-canchas/Contabilidad.png",
        alt: "administracion de contabilidad",
        descripcion: "Toda la administracion de la contabilidad del emprendimiento"
      },
      {
        src: "/images/admin-canchas/torneos.png",
        alt: "torneos",
        descripcion: "administracion de torneos"
      },
      {
        src: "/images/admin-canchas/Canchas.png",
        alt: "Administración de canchas",
        descripcion: "Interfaz de administración de canchas"
      },
      {
        src: "/images/admin-canchas/Contactos.png",
        alt: "contactos",
        descripcion: "agenda de clientes regulares"
      },
    ];
    const ImagenesGestionMobile = [
      {
        src: "/images/gestion-Emprendimiento/DasboardMobile-1.png",
        alt: "DashboardMobile 1",
        descripcion: "Version Mobile del dashboard",
      },
      {
        src: "/images/gestion-Emprendimiento/DashboardMobile-2.png",
        alt: "DashboardMobile 2",
        descripcion: "Version mobile del header",
      },
      {
        src: "/images/gestion-Emprendimiento/DashboardMobile-3.png",
        alt: "DashboardMobile 3",
        descripcion: "Version mobile del formulario agregar productos",
      },
      {
        src: "/images/gestion-Emprendimiento/DashboardMobile-4.png",
        alt: "DashboardMobile 4",
        descripcion: "Version mobile de la lista de productos",
      },
      {
        src: "/images/gestion-Emprendimiento/DashboardMobile-5.png",
        alt: "DashboardMobile 5",
        descripcion: "Version mobile de la lista de actividades recientes",
      },
      {
        src: "/images/gestion-Emprendimiento/DasboardMobile-grafico.png",
        alt: "DashboardMobile Grafico",
        descripcion: "Version mobile del grafico de stock y ventas",
      },
    ];
    const imagenesGestion = [
    {
      src: "/images/gestion-Emprendimiento/Dashboard-1.png",
      alt: "Dashboard 1",
      descripcion: "Primera vista del sistema",
    },
    {
        src: "/images/gestion-Emprendimiento/Dashboard-2.png",
        alt: "Dashboard 2",
        descripcion: "Agregar productos y lista de productos",
      },
      {
        src: "/images/gestion-Emprendimiento/Dashboard-3.png",
        alt: "Dashboard 3",
        descripcion: "Lista de actividades recientes",
      },
      {
        src: "/images/gestion-Emprendimiento/Dashboard-grafico.png",
        alt: "Dashboard 4",
        descripcion: "Grafico de stock y venta de cada producto",
      },
      {
        src: "/images/gestion-Emprendimiento/Productos-1.png",
        alt: "Productos 1",
        descripcion: "Tabla de productos modificable",
      },
      {
        src: "/images/gestion-Emprendimiento/Productos-2.png",
        alt: "Productos 2",
        descripcion: "Actividad reciente y Form de agregar producto",
      },
      {
        src: "/images/gestion-Emprendimiento/Interfaz.png",
        alt: "Interfaz",
        descripcion: "Interfaz para administrar las ventas realizadas en el momento",
      },
      {
        src: "/images/gestion-Emprendimiento/Gestion-ventas.png",
        alt: "Gestión de ventas",
        descripcion: "Gestion de todas las ventas realizadas y grafico de las ganancias",
      }
  ];
</script>

<section>
  <h2>Mis Proyectos</h2>
  <article>
    <h3>Sistema de Pedidos para Emprendimientos de Comida</h3>
    <p>Una aplicación para gestionar pedidos en restaurantes...</p>
    <div class="button-container">
      <a href="https://github.com/lauyoty14/pediloSimple-Frontend" class="button">Ver Repositorio Frontend</a>
      <a href="https://github.com/diazhernanluis/pediloSimple-Backend" class="button">Ver Repositorio Backend</a>
      <a href="#galeria-sistema-pedidos-mobile" class="button">Ver Galería Mobile</a>
    </div>

    <h4>Funcionalidades:</h4>
    <ul>
      <li>Gestión de pedidos en tiempo real</li>
      <li>Notificaciones a los usuarios sobre el estado del pedido</li>
      <li>Interfaz de usuario intuitiva y fácil de usar</li>
    </ul>

    <h4>Tecnologías:</h4>
    <div class="tech-icons">
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js" />
        <span>Node.js</span>
      </div>
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mongodb/mongodb-original-wordmark.svg" alt="Mongoose" />
        <span>Mongoose</span>
      </div>
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/svelte/svelte-original.svg" alt="SvelteKit" />
        <span>SvelteKit</span>
      </div>
    </div>

    <h4>Desafíos y Soluciones:</h4>
    <p>Desafío: Integrar un sistema de notificaciones en tiempo real.</p>
    <p>Solución: Implementé WebSockets para permitir la comunicación bidireccional entre el servidor y el cliente.</p>
  </article>

  <article>
    <h3>Sistema de administración de canchas</h3>
    <p>Un sistema para pedidos en emprendimientos de gastronomía</p>
    <div class="button-container">
      <a href="enlace-al-repo" class="button">Ver Repositorio</a>
      <a href="#galeria-sistema-administracion-mobile" class="button">Ver Galería Mobile</a>
    </div>

    <h4>Funcionalidades:</h4>
    <ul>
      <li>Gestión de reservas de canchas</li>
      <li>Interfaz de administración para usuarios y administradores</li>
      <li>Reportes de uso y estadísticas</li>
    </ul>

    <h4>Tecnologías:</h4>
    <div class="tech-icons">
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/svelte/svelte-original.svg" alt="SvelteKit" />
        <span>SvelteKit</span>
      </div>
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/djangorest/djangorest-original.svg" alt="Django" />
        <span>Django</span>
      </div>
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/postgresql/postgresql-original-wordmark.svg" alt="PostgreSQL" />
        <span>MySQL</span>
      </div>
    </div>

    <h4>Desafíos y Soluciones:</h4>
    <p>Desafío: Asegurar la disponibilidad de canchas en tiempo real.</p>
    <p>Solución: Implementé un sistema de reservas que actualiza la disponibilidad automáticamente.</p>
  </article>

  <article>
    <h3>Sistema de Gestión de Emprendimientos</h3>
    <p>Un sistema integral para gestionar stock, ventas y un carrito de compras en tiempo real.</p>
    <div class="button-container">
      <a href="#galeria-gestion-emprendimientos-pc" class="button">Ver Galería PC</a>
      <a href="#galeria-gestion-emprendimientos-mobile" class="button">Ver Galería Mobile</a>
    </div>

    <h4>Funcionalidades:</h4>
    <ul>
      <li>Gestión de stock con alertas para productos bajos en inventario</li>
      <li>Carrito de compras con cálculo automático de totales</li>
      <li>Historial de ventas detallado con gráficos de desempeño</li>
      <li>Gráficos del stock y ventas de cada producto</li>
      <li>Lista de actividades realizadas en el sistema</li>
    </ul>

    <h4>Tecnologías:</h4>
    <div class="tech-icons">
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/svelte/svelte-original.svg" alt="SvelteKit" />
        <span>SvelteKit</span>
      </div>
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/django/django-plain.svg" alt="Django" />
        <span>Django</span>
      </div>
      <div class="tech-icon">
        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/azuresqldatabase/azuresqldatabase-original.svg" alt="MySQL" />
        <span>MySQL</span>
      </div>
    </div>

    <h4>Desafíos y Soluciones:</h4>
    <p>Desafío: Implementar un carrito de compras que sincronice datos en tiempo real.</p>
    <p>Solución: Usé variables reactivas y funcionalidades que se recargan con cada cambio.</p>
  </article>
</section>

<section id="galeria-gestion-emprendimientos-pc" class="gallery-pc">
  <h3>Capturas de Pantalla: Sistema de Gestión de Emprendimientos (Versión PC)</h3>
  <div class="gallery-container-pc">
    <button class="carousel-pc-btn prev" on:click={() => moveCarousel(-1)}>❮</button>
    <div class="carousel-pc">
      {#each imagenesGestion.filter(img => !img.alt.includes('Mobile')) as imagen, index}
        <div class="gallery-pc-item {index === currentImage ? 'visible' : 'hidden'}">
          <img src={imagen.src} alt={imagen.alt}>
          <h4>{imagen.alt}</h4>
          <p>{imagen.descripcion}</p>
        </div>
      {/each}
    </div>
    <button class="carousel-pc-btn next" on:click={() => moveCarousel(1)}>❯</button>
  </div>
</section>

<!-- Galería Mobile: Sistema de Pedidos -->
<section id="galeria-sistema-pedidos-mobile" class="gallery-mobile">
  <h3>Capturas de Pantalla: Sistema de Pedidos (Versión Mobile)</h3>
  <div class="gallery-container">
    <button class="carousel-btn prev" on:click={() => moveCarouselMobile('pedidos', -1)}>❮</button>
    <div class="carousel" id="carousel-pedidos">
      {#each imagenes as imagen}
        <div class="gallery-item">
          <img src={imagen.src} alt={imagen.alt}>
          <h4>{imagen.alt}</h4>
          <p>{imagen.descripcion}</p>
        </div>
      {/each}
    </div>
    <button class="carousel-btn next" on:click={() => moveCarouselMobile('pedidos', 1)}>❯</button>
  </div>
</section>

<section id="galeria-sistema-administracion-mobile" class="gallery-mobile">
  <h3>Capturas de Pantalla: Sistema de Administración (Versión Mobile)</h3>
  <div class="gallery-container">
    <button class="carousel-btn prev" on:click={() => moveCarouselMobile('administracion', -1)}>❮</button>
    <div class="carousel" id="carousel-administracion">
      {#each imagenesAdmin as imagen}
        <div class="gallery-item">
          <img src={imagen.src} alt={imagen.alt}>
          <h4>{imagen.alt}</h4>
          <p>{imagen.descripcion}</p>
        </div>
      {/each}
    </div>
    <button class="carousel-btn next" on:click={() => moveCarouselMobile('administracion', 1)}>❯</button>
  </div>
</section>

<section id="galeria-gestion-emprendimientos-mobile" class="gallery-mobile">
  <h3>Capturas de Pantalla: Sistema de Gestión de Emprendimientos (Versión Mobile)</h3>
  <div class="gallery-container">
    <button class="carousel-btn prev" on:click={() => moveCarouselMobile('emprendimientos', -1)}>❮</button>
    <div class="carousel" id="carousel-emprendimientos">
      {#each ImagenesGestionMobile.filter(img => img.alt.includes('Mobile')) as imagen}
        <div class="gallery-item">
          <img src={imagen.src} alt={imagen.alt}>
          <h4>{imagen.alt}</h4>
          <p>{imagen.descripcion}</p>
        </div>
      {/each}
    </div>
    <button class="carousel-btn next" on:click={() => moveCarouselMobile('emprendimientos', 1)}>❯</button>
  </div>
</section>

<style>
  section {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;
  }

  h2 {
    font-size: 2.5rem;
    color: var(--primary-color);
    text-align: center;
    margin-bottom: 2rem;
  }

  article {
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    padding: 1.5rem;
    margin-bottom: 2rem;
    transition: transform 0.3s ease;
  }

  article:hover {
    transform: translateY(-5px);
  }

  h3 {
    font-size: 1.8rem;
    color: var(--accent-color);
    margin-bottom: 1rem;
  }

  p {
    margin-bottom: 0.5rem;
    line-height: 1.6;
  }

  a {
    display: inline-block;
    margin-top: 1rem;
    padding: 0.5rem 1rem;
    background-color: var(--secondary-color);
    color: white;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
  }

  a:hover {
    background-color: var(--primary-color);
  }
  
  /* Configuración del contenedor del carrusel */
  .gallery-container {
    position: relative; /* Necesario para botones absolutos */
    display: flex;
    flex-direction: column; /* Alinea el título y el carrusel en una columna */
    gap: 1rem;
    overflow: hidden;
    max-width: 100%; /* Asegura que no exceda el ancho del contenedor */
    padding: 1rem;
    box-sizing: border-box; /* Incluye padding en el cálculo de tamaño */
    justify-content: center;
    align-items: center; /* Centra verticalmente las imágenes */
  }

  /* Configuración del carrusel */
  .carousel {
    display: flex;
    overflow-x: auto;
    scroll-snap-type: x mandatory;
    gap: 1rem;
    max-width: 100%;
    box-sizing: border-box;
    justify-content: flex-start; /* Cambiaremos dinámicamente a center si hay pocos elementos */
  }

  .carousel::-webkit-scrollbar {
    display: none; /* Oculta la barra de desplazamiento */
  }

  .carousel img {
    width: 200px;
    height: auto;
    border-radius: 5px;
    margin: 0 auto;
    scroll-snap-align: center;
    transition: transform 0.3s ease;
  }

  /* Asegura que el título, texto y el botón no expandan el carrusel */
  .gallery-item {
    max-width: 200px;
    text-align: center;
  }

  .gallery-item h4 {
    margin: 0.5rem 0 0.2rem;
    font-size: 1rem;
    font-weight: bold;
    color: #fff;
  }

  .gallery-item p {
    font-size: 0.9rem;
    color: #ddd;
  }

  /* Botones de navegación */
  .carousel-btn {
    background-color: rgba(0, 0, 0, 0.5);
    border: none;
    color: white;
    font-size: 2rem;
    cursor: pointer;
    padding: 0.5rem 1rem;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    z-index: 10;
  }

  .carousel-btn.prev {
    left: 0.5rem;
  }

  .carousel-btn.next {
    right: 0.5rem;
  }

  /* Configuración de la galería para PC */
  .gallery-container-pc {
    position: relative;
    width: 100%;
    max-width: 800px; /* Ajusta el tamaño máximo del carrusel */
    margin: auto;
    overflow: hidden; /* Oculta los elementos fuera del contenedor */
    background-color: #f9f9f9;
  }

  .carousel-pc {
    display: flex;
    transition: transform 0.5s ease-in-out; /* Para animar el desplazamiento */
    width: 100%; /* Asegura que no exceda el tamaño del contenedor */
  }

  .gallery-pc-item {
    flex: 0 0 100%; /* Mantiene el tamaño del contenedor para el carrusel */
    height: 100%; /* Asegura que ocupe todo el espacio vertical disponible */
    display: block; /* Habilitamos flexbox */
    justify-content: center; /* Centra horizontalmente */
    align-items: center; /* Centra verticalmente */
    overflow: hidden; /* Oculta contenido desbordante */
    text-align: center;
  }

  .gallery-pc-item img {
    max-width: 100%; /* Escala la imagen para no desbordar horizontalmente */
    max-height: 100%; /* Escala la imagen para no desbordar verticalmente */
    object-fit: contain; /* Mantiene las proporciones de la imagen */
  }

  .gallery-pc-item h4 {
    margin: 0.5rem 0 0.2rem;
    font-size: 1rem;
    font-weight: bold;
    color: #000000;
  }

  .gallery-pc-item p {
    font-size: 0.9rem;
    color: #000000;
  }

  .carousel-pc-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    z-index: 10;
  }

  .carousel-pc-btn.prev {
    left: 10px;
  }

  .carousel-pc-btn.next {
    right: 10px;
  }

  .tech-icon {
    background-color: rgba(255, 255, 255, 0.8); /* Fondo blanco con opacidad */
    border-radius: 8px; /* Bordes redondeados */
    padding: 0.5rem; /* Espaciado interno */
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2); /* Sombra para dar profundidad */
    text-align: center; /* Centra el texto */
  }
  
  .tech-icons {
    display: flex;
    gap: 1.5rem;
    margin-bottom: 1rem;
  }

  .tech-icon img {
    width: 40px; /* Ajusta el tamaño según sea necesario */
    height: auto;
  }

  .tech-icon span {
    display: block; /* Hace que el texto esté en una nueva línea */
    margin-top: 0.5rem; /* Espaciado entre la imagen y el texto */
    font-size: 0.9rem; /* Tamaño de fuente del texto */
    color: black; /* Color del texto */
  }
</style>
