<script>
    import { onMount } from 'svelte';
  </script>
  
  <header>
    <h1>Octavio Pastorive - Fullstack Developer</h1>
    <nav>
      <a href="/">Inicio</a>
      <a href="/about">Sobre mí</a>
      <a href="/projects">Proyectos</a>
      <a href="/contact">Contacto</a>
    </nav>
  </header>
  
  <style>
    header {
      background-color: rgba(0, 0, 0, 0.7);
      color: var(--text-color);
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    h1 {
      margin: 0;
      font-size: 1.5rem;
    }

    nav {
      display: flex;
      gap: 1rem;
    }

    a {
      color: var(--text-color);
      text-decoration: none;
      padding: 0.5rem;
      border-radius: 4px;
      transition: background-color 0.3s ease;
    }

    a:hover {
      background-color: var(--primary-color);
    }

    @media (max-width: 600px) {
        nav {
            flex-direction: column; /* Cambia la dirección a columna en pantallas pequeñas */
            gap: 0.5rem; /* Reduce el espacio entre los enlaces */
        }
    }
  </style>
