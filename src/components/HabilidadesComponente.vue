<script setup>
import { ref } from 'vue';
const habilidades = ref([
    {
        id: 1, nombre: 'Lenguajes de Programación', habilidades: [
            //Se crea un objeto con id, nombre, nivel e icono
            { id: 1, nombre: 'JavaScript', nivel: 'Avanzado', icono: "/src/assets/javascript.svg" },
            { id: 2, nombre: 'Python', nivel: 'Intermedio', icono: "/src/assets/python.svg" },
            { id: 3, nombre: 'HTML/CSS', nivel: 'Avanzado', icono: "/src/assets/html-5.svg" },
            { id: 4, nombre: 'Java', nivel: 'Intermedio', icono: "/src/assets/Java.svg" },
            { id: 5, nombre: 'SQL', nivel: 'Intermedio', icono: "/src/assets/sql.svg" }
        ]
    },
    {
        id: 2, nombre: 'Frameworks y Librerías', habilidades: [
            { id: 1, nombre: 'React.js', nivel: 'Avanzado', icono: "/src/assets/react.svg" },
            { id: 2, nombre: 'Vue.js', nivel: 'Intermedio', icono: "/src/assets/vue.svg" },
            { id: 3, nombre: 'Node.js', nivel: 'Avanzado', icono: "/src/assets/node.svg" },
            { id: 4, nombre: 'Django', nivel: 'Intermedio', icono: "/src/assets/django.svg" },
            { id: 5, nombre: 'Bootstrap', nivel: 'Avanzado', icono: "/src/assets/bootstrap.svg" }
        ]
    },
    {
        id: 3, nombre: 'Herramientas y Software', habilidades: [
            { id: 1, nombre: 'Git', nivel: 'Avanzado', icono: "/src/assets/git.svg" },
            { id: 2, nombre: 'Docker', nivel: 'Intermedio', icono: "/src/assets/docker.svg" },
            { id: 3, nombre: 'Cypress', nivel: 'Intermedio', icono: "/src/assets/cypress.svg" },
            { id: 4, nombre: 'Figma', nivel: 'Intermedio', icono: "/src/assets/figma.svg" },
            { id: 5, nombre: 'Visual Studio Code', nivel: 'Avanzado', icono: "/src/assets/vscode.svg" }
        ]
    },
    {
        id: 4, nombre: 'Bases de Datos', habilidades: [
            { id: 1, nombre: 'MongoDB', nivel: 'Avanzado', icono: "/src/assets/mongodb.svg" },
            { id: 2, nombre: 'MySQL', nivel: 'Intermedio', icono: "/src/assets/mysql.svg" },
            { id: 3, nombre: 'PostgreSQL', nivel: 'Intermedio', icono: "/src/assets/postgresql.svg" }
        ]
    },
    {
        id: 5, nombre: 'Idiomas', habilidades: [
            { id: 1, nombre: 'Español', nivel: 'Nativo', icono: "/src/assets/español.svg" },
            { id: 2, nombre: 'Inglés', nivel: 'Avanzado (C1)', icono: "/src/assets/ingles.svg" }
        ]
    }
]);

</script>


<template>
    <div class="skills-contenedor">
        <div v-for="habilidad in habilidades" :key="habilidad.id" class="skills-categoria">
            <h3>{{ habilidad.nombre }}</h3>
            <ul class="skills">
                <li v-for="habilidad in habilidad.habilidades" :key="habilidad.id" class="skill">
                    <img :src="habilidad.icono" :alt="habilidad.nombre">
                    <span>{{ habilidad.nombre }}: {{ habilidad.nivel }}</span>
                </li>
            </ul>
        </div>
    </div>

</template>

<style scoped>
.skills-contenedor {
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    gap: 20px;
    padding: 20px;
    justify-content: center;
    background: linear-gradient(-45deg,#021526,#03346E,#6EACDA,#E2E2B6);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
}
@keyframes gradient{
    0%{
        background-position: 50% 0%;
    }
    50%{
        background-position: 50% 100%;
    }
    100%{
        background-position: 50% 0%;
    }
}

.skills-categoria {
    margin-bottom: 20px;
    
}

.skills-categoria h3 {
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5em;
    color: aliceblue;
    font-size: 1.5em;
    font-weight: bold;
}

.skills {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    background-color: rgba(241, 245, 243, 0.856);
    padding: 0.3em;
    border-radius: 8px;
    box-shadow: 0px 4px 12px rgba(2, 151, 151, 0.963);
    flex: 1 1 200px;
    max-width: 250px;
}

.skill:hover {
    background-color: rgba(2, 151, 151, 0.963);
}

.skill img {
    width: 35px;
    height: 35px;
}

.skill span {
    font-size: 1em;
    color: #333;
}

.skill:hover {
    font-size: 1.3em;
    transition: 2s ease;
}

@media (max-width: 768px) {
    .skills-categoria h3 {
        justify-content: center;
    }

    .skill {
        justify-content: center;
    }
}
</style>