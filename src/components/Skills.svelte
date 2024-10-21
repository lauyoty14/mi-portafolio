<script lang="ts">
  const skills = [
    { name: 'SvelteKit', level: 90 },
    { name: 'Django', level: 85 },
    { name: 'NodeJS', level: 80 },
    { name: 'Mongoose', level: 75 },
    { name: 'MySQL', level: 85 }
  ];
  // Animación de carga
  import { onMount } from 'svelte';

  onMount(() => {
    const skillLevels = document.querySelectorAll('.skill-level');
    skillLevels.forEach((level: Element, index) => {
      const skillLevel = skills[index].level;
      // Usar setTimeout para permitir que el DOM se renderice antes de aplicar el ancho
      setTimeout(() => {
        (level as HTMLElement).style.width = `${skillLevel}%`;
      }, 0);
    });
  });
</script>

<section class="skills">
  <h2>Mis Habilidades</h2>
  <div class="skill-list">
    {#each skills as skill}
      <div class="skill" title="{skill.name}: Nivel {skill.level}">
        <span class="skill-name"><i class="fa fa-svelte"></i> {skill.name}</span>
        <div class="skill-bar">
          <div class="skill-level" style="width: 0%;" data-level="{skill.level > 80 ? 'high' : skill.level > 50 ? 'medium' : 'low'}"></div>
        </div>
      </div>
    {/each}
  </div>
</section>

<style>
  .skills {
    padding: 4rem 0;
    background-color: rgba(0, 0, 0, 0.7);
    border-radius: 10px; /* Bordes redondeados */
  }

  h2 {
    font-size: 2.5rem;
    margin-bottom: 2rem;
    text-align: center;
    color: white; /* Color del texto */
  }

  .skill-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    max-width: 600px;
    margin: 0 auto;
  }

  .skill {
    display: flex;
    align-items: center;
    background-color: rgba(255, 255, 255, 0.1); /* Fondo semitransparente */
    padding: 1rem;
    border-radius: 5px; /* Bordes redondeados */
    transition: transform 0.3s ease; /* Transición para el hover */
  }

  .skill:hover {
    transform: scale(1.05); /* Aumentar ligeramente al pasar el mouse */
  }

  .skill-name {
    flex: 0 0 100px;
    font-weight: bold;
    color: white; /* Color del texto */
  }

  .skill-bar {
    flex: 1;
    height: 20px;
    background-color: #e9ecef;
    border-radius: 10px;
    overflow: hidden;
  }

  .skill-level {
    height: 100%;
    background-color: var(--primary-color);
    transition: width 0.5s ease; /* Transición */
  }

  .skill-level[data-level="high"] {
    background-color: green; /* Alto */
  }

  .skill-level[data-level="medium"] {
    background-color: yellow; /* Medio */
  }

  .skill-level[data-level="low"] {
    background-color: red; /* Bajo */
  }
</style>
