<script>
  let name = '';
  let email = '';
  let message = '';

  function handleSubmit() {
    // Aquí puedes agregar la lógica para enviar el formulario
    console.log('Formulario enviado', { name, email, message });
    // Resetear los campos después del envío
    name = '';
    email = '';
    message = '';
  }
</script>

<section class="contact">
  <h2>Contáctame</h2>
  <form action="https://formspree.io/f/xanynwbv" method="POST">
    <div class="form-group">
      <label for="name">Nombre</label>
      <input type="text" id="name" name="name" required>
    </div>
    <div class="form-group">
      <label for="email">Email</label>
      <input type="email" id="email" name="email" required>
    </div>
    <div class="form-group">
      <label for="message">Mensaje</label>
      <textarea id="message" name="message" required></textarea>
    </div>
    <button type="submit">Enviar mensaje</button>
  </form>
  
  <div class="social-links">
    <h3>Conéctame en:</h3>
    <ul>
      <li><a href="https://www.linkedin.com/in/octavio-nicolas-pastorive-644796306/" target="_blank"><i class="fab fa-linkedin"></i> LinkedIn</a></li>
      <li><a href="mailto:nicolas.octavio.pastorive@gmail.com"><i class="fas fa-envelope"></i> Gmail</a></li>
      <li><a href="https://github.com/lauyoty14" target="_blank"><i class="fab fa-github"></i> GitHub</a></li>
    </ul>
  </div>
</section>

<style>
  .contact {
    padding: 4rem 1rem; /* Ajustar el padding para móviles */
  }

  h2 {
    font-size: 2.5rem;
    margin-bottom: 2rem;
    text-align: center;
  }

  form {
    display: flex;
    flex-direction: column; /* Cambiar a columna en móviles */
  }

  .form-group {
    margin-bottom: 1rem; /* Espaciado entre grupos de formulario */
  }

  label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
  }

  input,
  textarea {
    width: 100%;
    padding: 0.8rem;
    border-radius: 4px;
    background-color: rgba(255, 255, 255, 0.1);
    color: var(--text-color);
    border: 1px solid var(--accent-color);
  }

  textarea {
    height: 150px;
  }

  button {
    display: block;
    width: 100%;
    padding: 1rem;
    background-color: var(--secondary-color);
    color: white;
    border: none;
    border-radius: 4px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  button:hover {
    background-color: var(--primary-color);
  }

  .social-links {
    text-align: center;
    margin-top: 2rem;
  }

  .social-links ul {
    list-style-type: none;
    padding: 0;
  }

  .social-links li {
    margin: 0.5rem 0;
  }

  .social-links a {
    color: var(--accent-color);
    text-decoration: none;
  }

  .social-links a:hover {
    text-decoration: underline;
  }

  .social-links i {
    margin-right: 0.5rem; /* Espacio entre el ícono y el texto */
  }
</style>
