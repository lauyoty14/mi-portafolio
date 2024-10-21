<section>
    <h2>Mis Proyectos</h2>
    <article>
      <h3>Sistema de Pedidos para Emprendimientos de Comida</h3>
      <p>Una aplicación para gestionar pedidos en restaurantes...</p>
      <div class="button-container">
        <a href="https://github.com/lauyoty14/pediloSimple-Frontend" class="button">Ver Repositorio Frontend</a>
        <a href="https://github.com/diazhernanluis/pediloSimple-Backend" class="button">Ver Repositorio Backend</a>
        <a href="#galeria-sistema-pedidos" class="button">Ver Galería</a>
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
      <h3>Sistema de administracion de canchas</h3>
      <p>Un sistema para pedidos en emprendimientos de gastronomia</p>
      <div class="button-container">
        <a href="enlace-al-repo" class="button">Ver Repositorio</a>
        <a href="#galeria-sistema-administracion" class="button">Ver Galería</a>
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
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/djangorest/djangorest-original.svg" alt ="Django"/>
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
</section>

<section id="galeria-sistema-pedidos" class="gallery">
  <h3>Capturas de Pantalla: Sistema de Pedidos para Emprendimientos de Comida</h3>
  <div class="gallery-container">
    {#each imagenes as imagen}
      <div class="gallery-item">
        <img src={imagen.src} alt={imagen.alt}>
        <p>{imagen.descripcion}</p>
      </div>
    {/each}
  </div>
</section>

<section id="galeria-sistema-administracion" class="gallery">
  <h3>Capturas de Pantalla: Sistema de Administración de Canchas de Fútbol</h3>
  <div class="gallery-container">
    {#each imagenesAdmin as imagen}
      <div class="gallery-item">
        <img src={imagen.src} alt={imagen.alt}>
        <p>{imagen.descripcion}</p>
      </div>
    {/each}
  </div>
</section>

<script>
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
</script>

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

  .gallery {
    margin-top: 3rem;
    padding: 1rem;
    background-color: rgba(0, 0, 0, 0.05);
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  }

  .gallery h3 {
    text-align: center;
    margin-bottom: 1.5rem;
    font-size: 2rem;
    color: var(--primary-color);
  }

  .gallery-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1.5rem;
  }

  .gallery-item {
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 10px;
    padding: 1rem;
    text-align: center;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .gallery-item:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
  }

  .gallery-item img {
    max-width: 100%;
    height: auto;
    border-radius: 5px;
    margin-bottom: 0.5rem;
    object-fit: cover;
    transition: transform 0.3s ease;
  }

  .gallery-item img:hover {
    transform: scale(1.1);
  }

  .gallery-item p {
    font-size: 0.9rem;
    color: var(--text-color);
    margin-top: 0.5rem;
  }

  .button-container {
    margin-top: 1rem;
  }

  .button {
    display: inline-block;
    margin-right: 1rem;
    padding: 0.5rem 1rem;
    background-color: var(--secondary-color);
    color: white;
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s ease;
  }

  .button:hover {
    background-color: var(--primary-color);
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
