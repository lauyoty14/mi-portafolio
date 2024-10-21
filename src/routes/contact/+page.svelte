<section>
    <h2>Contacto</h2>
    <p>¿Quieres colaborar o tienes alguna pregunta? ¡Escríbeme!</p>
    <form>
      <label for="name">Nombre:</label>
      <input type="text" id="name" required />
      
      <label for="email">Email:</label>
      <input type="email" id="email" required />
      
      <label for="message">Mensaje:</label>
      <textarea id="message" required></textarea>
      
      <button type="submit">Enviar</button>
    </form>
  </section>
  
  <style>
    section {
      max-width: 600px;
      margin: 0 auto;
      padding: 2rem;
      background-color: rgba(255, 255, 255, 0.1);
      border-radius: 15px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    h2 {
      font-size: 2.5rem;
      color: var(--accent-color);
      text-align: center;
      margin-bottom: 1.5rem;
    }

    p {
      text-align: center;
      font-size: 1.1rem;
      margin-bottom: 2rem;
      color: var(--text-color);
    }

    form {
      display: flex;
      flex-direction: column;
    }

    label {
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
      color: var(--secondary-color);
    }

    input, textarea {
      padding: 0.8rem;
      margin-bottom: 1.5rem;
      border: none;
      border-radius: 8px;
      background-color: rgba(255, 255, 255, 0.2);
      color: var(--text-color);
      font-size: 1rem;
      transition: all 0.3s ease;
    }

    input:focus, textarea:focus {
      outline: none;
      box-shadow: 0 0 0 2px var(--accent-color);
    }

    textarea {
      min-height: 150px;
      resize: vertical;
    }

    button {
      padding: 1rem 2rem;
      background-color: var(--accent-color);
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 1.1rem;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    button:hover {
      background-color: var(--secondary-color);
      transform: translateY(-2px);
    }
  </style>