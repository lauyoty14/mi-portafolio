<script>
  import Hero from '../components/Hero.svelte';
  import About from '../components/About.svelte';
  import Skills from '../components/Skills.svelte';
  import ProjectHighlights from '../components/ProjectHighlights.svelte';
  import Contact from '../components/Contact.svelte';
</script>

<svelte:head>
  <title>Octavio Pastorive - Desarrollador Fullstack</title>
  <meta name="description" content="Portafolio de Octavio Pastorive, desarrollador fullstack con experiencia en SvelteKit, Django, NodeJS, Mongoose y MySQL." />
</svelte:head>

<main>
  <Hero />
  <About />
  <Skills />
  <ProjectHighlights />
  <Contact />
</main>

<style>
  main {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
  }

  @media (max-width: 768px) {
    main {
      padding: 1rem;
    }
  }
</style>
