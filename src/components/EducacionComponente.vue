
<script setup>
    import { ref } from 'vue';
    const educacion = ref([
    {fecha: '2024', title: 'Técnicatura Universitaria en Programacion', descripcion: 'Incumbencias Profesionales: Operación y programación de computadoras, desarrollo de programas en distintos lenguajes, análisis y control de sistemas informáticos.', enlace:'https://www.youtube.com/'},
    {fecha: '2023', title: 'Desarrollador Full Stack', descripcion: 'Trabajé en XYZ Tech, donde diseñé y desarrollé aplicaciones web completas utilizando tecnologías como Node.js, React y MongoDB.', enlace:'http:www.direccion.com'},
    {fecha: '2022', title: 'Internship en Desarrollo Web', descripcion: 'Realicé una pasantía en ABC Solutions, contribuyendo en la creación de interfaces de usuario y optimización de sitios web.', enlace:'http:www.direccion.com'},
    {fecha: '2021', title: 'Proyecto Personal - Aplicación de Gestión de Tareas', descripcion: 'Desarrollé una aplicación para la gestión de tareas diarias usando HTML, CSS y JavaScript, implementando funcionalidades como listas de tareas y recordatorios.', enlace:'http:www.direccion.com'},
    {fecha: '2020', title: 'Curso de Introducción a la Programación', descripcion: 'Completé un curso en línea sobre fundamentos de programación, donde aprendí lenguajes como Python y Java.', enlace:'http:www.direccion.com'}
]);

</script>

<template>
    <ul class="timeline">
        <li class="timeline-event" v-for="(item, index) in educacion" :key="index">
            
            <label class="timeline-event-icon mov"></label>
            <div class="timeline-event-copy">
                <p class="timeline-event-thumbnail mov">{{ item.fecha }}</p>
                <h3>{{ item.title }}</h3>
                <p>{{ item.descripcion }}</p>
                <a class="enlace" :href="item.enlace" target="_blank">Saber más</a>
            </div>
        </li>
    </ul>
    
</template>

<style scoped>


/* Fonts */
@import url(https://fonts.googleapis.com/css?family=Open+Sans:300,700);
body {
  font-family: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  font-size: 1em;
  font-weight: 300;
  line-height: 1.5;
  letter-spacing: 0.05em;
}

/* Layout */
* {
  box-sizing: border-box;
}

/* Styling */
.timeline {
  margin: 4em auto;
  position: relative;
  max-width: 46em;
} 
.timeline::before {
    background-color: white;
    content: '';
    margin-left: -1px;
    position: absolute;
    top: 0;
    left: 2em;
    width: 2px;
    height: 100%;
}

.timeline-event {
    position: relative;
}



.timeline-event:hover .timeline-event-icon {
    transform: rotate(-45deg); /* Efecto de rotación */
    background-color: rgb(168, 50, 121); /* Cambio de color de fondo */
}

.timeline-event:hover .timeline-event-thumbnail {
    box-shadow: inset 40em 0 0 0 rgb(168, 50, 121); /* Cambio de sombra interna */
}



.timeline-event-copy {
  padding: 2em;
  position: relative;
  top: -1.875em;
  left: 4em;
  width: 80%;
} 
h3 {
    font-size: 1.75em;
}
  
h4 {
    font-size: 1.2em;
    margin-bottom: 1.2em;
}
  
  
p:not(.timeline-event-thumbnail) {
    padding-bottom: 1.2em;
}


.timeline-event-icon {
  transition: transform 0.3s ease-in, background-color 1s ease-out;
  rotate: 45deg;
  background-color: white;
  outline: 10px solid black;
  display: block;
  margin: 0.5em 0.5em 0.5em -0.5em;
  position: absolute;
  top: 0;
  left: 2em;
  width: 1em;
  height: 1em;
}

.timeline-event-thumbnail {
  transition: box-shadow 0.5s ease-in 0.1s;
  color: black;
  font-size: 0.75em;
  background-color: white;
  box-shadow: inset 0 0 0 0em #ef795a;
  display: inline-block;
  margin-bottom: 1.2em;
  padding: 0.25em 1em 0.2em 1em;
}
</style>