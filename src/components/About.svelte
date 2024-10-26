<section class="about">
  <h2>Sobre mí</h2>
  <div class="content">
    <img src="/images/profile-photo.jpeg" alt="Octavio Pastorive" class="profile-photo">
    <div class="text">
      <p>Soy un desarrollador fullstack con mas de 1 año de experiencia. Me apasiona crear soluciones web innovadoras y eficientes utilizando las últimas tecnologías.</p>
      <p>Mi enfoque se centra en desarrollar aplicaciones web robustas y escalables, siempre buscando aprender y mejorar mis habilidades.</p>
      <a href="/about" class="read-more">Leer más sobre mí</a>
    </div>
  </div>
</section>

<style>
  .about {
    padding: 4rem 1rem; /* Ajustar el padding para móviles */
  }

  h2 {
    font-size: 2.5rem;
    margin-bottom: 2rem;
    text-align: center;
  }

  .content {
    flex-direction: column; /* Cambiar a columna en móviles */
    align-items: center; /* Centrar contenido */
    gap: 2rem;
  }

  .profile-photo {
    width: 150px; /* Ajustar tamaño de la imagen */
    height: 150px; /* Ajustar tamaño de la imagen */
    border-radius: 50%;
    object-fit: cover;
  }

  .text {
    flex: 1;
  }

  p {
    margin-bottom: 1rem;
    line-height: 1.6;
  }

  .read-more {
    display: inline-block;
    margin-top: 1rem;
    color: #0077b6;
    text-decoration: none;
    font-weight: bold;
  }
</style>
