<script>
  const projects = [
    {
      title: 'Sistema de Pedidos para Emprendimientos de Comida',
      description: 'Una aplicación para gestionar pedidos en restaurantes y emprendimientos gastronómicos.',
      technologies: ['NodeJS', 'Mongoose', 'MySQL'],
      image: './images/pediloSimple/inicioPC.png',
      link: '/projects/sistema-pedidos'
    },
    {
      title: 'Sistema de Administración de Canchas de Fútbol',
      description: 'Un sistema para la gestión de reservas y administración de canchas de fútbol.',
      technologies: ['SvelteKit', 'Django', 'MySQL'],
      image: './images/admin-canchas/inicioPC.png',
      link: '/projects/admin-canchas'
    }
  ];
</script>

<section class="project-highlights" id="project-highlights">
  <h2>Proyectos Destacados</h2>
  <div class="project-grid">
    {#each projects as project}
      <div class="project-card">
        <img src={project.image} alt={project.title} class="project-image">
        <div class="project-info">
          <h3>{project.title}</h3>
          <p>{project.description}</p>
          <div class="technologies">
            {#each project.technologies as tech}
              <span class="tech-tag">{tech}</span>
            {/each}
          </div>
        </div>
      </div>
    {/each}
  </div>
  <div class="cta">
    <a href="/projects" class="all-projects-link">Ver todos los proyectos</a>
  </div>
</section>

<style>
  .project-highlights {
    padding: 4rem 0;
  }

  h2 {
    font-size: 2.5rem;
    margin-bottom: 2rem;
    text-align: center;
  }

  .project-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
  }

  .project-card {
    border: 1px solid #e9ecef;
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.3s ease;
    background-color: rgba(255, 255, 255, 0.1);
  }

  .project-card:hover {
    transform: translateY(-5px);
  }

  .project-image {
    width: 100%;
    height: 300px;  
    object-fit: contain;  
  }

  .project-info {
    padding: 1.5rem;
  }

  h3 {
    font-size: 1.5rem;
    margin-bottom: 1rem;
  }

  .technologies {
    margin: 1rem 0;
  }

  .tech-tag {
    display: inline-block;
    background-color: var(--accent-color);
    color: var(--background-color);
    padding: 0.3rem 0.6rem;
    border-radius: 4px;
    font-size: 0.8rem;
    margin-right: 0.5rem;
    margin-bottom: 0.5rem;
  }

  .cta {
    text-align: center;
    margin-top: 2rem;
  }

  .all-projects-link {
    display: inline-block;
    padding: 0.8rem 1.5rem;
    background-color: var(--secondary-color);
    color: white;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
    transition: background-color 0.3s ease;
  }

  .all-projects-link:hover {
    background-color: var(--primary-color);
  }
</style>
