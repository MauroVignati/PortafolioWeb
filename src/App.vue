<script setup>
  import NavBar from './components/NavBar.vue';
  import DatosPersonales from './components/DatosPersonales.vue';
  import Educacion from './components/EducacionComponente.vue';
  import ExperienciaComponente from './components/ExperienciaComponente.vue';
  import ProyectosComponente from './components/ProyectosComponente.vue';
  import HabilidadesComponente from './components/HabilidadesComponente.vue';
  import InteresesComponente from './components/InteresesComponente.vue';
</script>

<template>
  <header id="top">
    <!--Barra de navegacion-->
    <NavBar />
    <!--Componentes Datos Personales-->
    <DatosPersonales />

  </header>
  <main>
    <!-- eñ estoñp css de section se encuentra en base.css-->
    <section id="educacion"><h2>Educacion - Cursos</h2>
    <Educacion />
    </section>
    <section id="experiencia"><h2>Experiencia</h2>
    <ExperienciaComponente />
    </section>
    <section id="proyectos"><h2>Proyectos</h2></section>
    <ProyectosComponente />
    <section id="habilidades">
      <h2>Habilidades</h2>
      <HabilidadesComponente />
    </section>
    <section id="intereses">
      <h2>Intereses</h2>
      <InteresesComponente />
    </section>
    <footer>
      <a href="#top">Subir</a>
      <p>® 2024 Vignati Mauro - Portafolio web</p>
    </footer>
  </main>
</template>

<style scoped>
  footer{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
    font-size: 1.3rem;
  }
</style>
