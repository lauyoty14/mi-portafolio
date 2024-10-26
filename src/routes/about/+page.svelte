<script>
  // Puedes importar componentes adicionales si los necesitas
</script>

<svelte:head>
  <title>Sobre mí - Octavio Pastorive</title>
  <meta name="description" content="Conoce más sobre Octavio Pastorive, desarrollador fullstack con experiencia en SvelteKit, Django, NodeJS, y más." />
</svelte:head>

<main class="about-page">
  <h1>Sobre mí</h1>
  
  <section class="bio">
    <img src="/images/profile-photo.jpeg" alt="Octavio Pastorive" class="profile-photo">
    <div>
      <h2>Octavio Pastorive</h2>
      <p>Soy un desarrollador fullstack apasionado por crear soluciones web innovadoras y eficientes. Con un año de experiencia en el desarrollo web, me especializo en tecnologías como SvelteKit, Django y NodeJS.</p>
    </div>
  </section>

  <section class="experience">
    <h2>Experiencia Profesional</h2>
    <ul>
      <li>
        <h3>Desarrollador Fullstack Junior</h3>
        <p>Empresa MasConectados | enero 2023 - diciembre 2023</p>
        <ul>
          <li>Desarrollo de aplicaciones web utilizando SvelteKit y Django.</li>
          <li>Implementación de bases de datos con MySQL y MongoDB.</li>
          <li>Colaboración en equipos ágiles para entregar proyectos de alta calidad.</li>
        </ul>
      </li>
    </ul>
  </section>

  <section class="education">
    <h2>Educación</h2>
    <ul>
      <li>
        <h3>Licenciatura en Informática</h3>
        <p>Universidad Universidad Nacional de Quilmes | En curso</p>
      </li>
      <li>
        <h3>Tecnicatura en Programación</h3>
        <p>Escuela Secundaria Tecnica de la Universidad Nacional de Quilmes | Finalizado (Año de graduación 2023)</p>
      </li>
    </ul>
  </section>

  <section class="skills">
    <h2>Habilidades Técnicas</h2>
    <ul>
      <li>Frontend: SvelteKit</li>
      <li>Backend: Django, NodeJS, Express</li>
      <li>Bases de datos: MySQL, MongoDB</li>
      <li>Control de versiones: Git, GitHub</li>
      <li>Metodologías: Agile, Scrum</li>
    </ul>
  </section>

  <section class="interests">
    <h2>Intereses y Pasatiempos</h2>
    <p>Además de la programación, me apasiona el deporte, la musica y los videojuegos. Fiel creyente de la motivacion personal y fuertemente determinado a ser un desarrollador fullstack de alto nivel.</p>
  </section>
</main>

<style>
  .about-page {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;
  }

  h1 {
    font-size: 2.5rem;
    color: var(--primary-color);
    margin-bottom: 2rem;
  }

  h2 {
    font-size: 1.8rem;
    color: var(--accent-color);
    margin-top: 2rem;
    margin-bottom: 1rem;
  }

  .bio {
    display: flex;
    align-items: center;
    gap: 2rem;
    margin-bottom: 2rem;
  }

  .profile-photo {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    object-fit: cover;
  }

  section {
    margin-bottom: 2rem;
  }

  ul {
    list-style-type: none;
    padding-left: 0;
  }

  li {
    margin-bottom: 1rem;
  }

  .experience li, .education li {
    background-color: rgba(255, 255, 255, 0.1);
    padding: 1rem;
    border-radius: 8px;
  }

  .skills ul {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .skills li {
    background-color: var(--secondary-color);
    color: var(--text-color);
    padding: 0.5rem 1rem;
    border-radius: 20px;
    font-size: 0.9rem;
  }
</style>