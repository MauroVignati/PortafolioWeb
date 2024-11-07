<script setup>
import proyecto1 from '/src/assets/RestoApp.png';
import proyecto2 from '/src/assets/e-learning.png';
import proyecto3 from '/src/assets/blogPersonal.png';
import proyecto4 from '/src/assets/inventario.png';

import { ref } from 'vue';
var misProyectos = ref([]);
misProyectos.value = ([
    {
        id: 1,
        src: proyecto1,
        titulo: "'Aplicación de Reservas para Restaurantes(2023)'",
        descripcion: "Creé una aplicación móvil con Flutter que permite a los usuario reservar mesas en restaurantes locales",
        proyectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/user/RestoApp"
    },
    {
        id: 2,
        src: proyecto2,
        titulo: 'Plataforma de E-Learning(2022)',
        descripcion: 'Diseñe y desarrolle una plataforma de educación en línea utilizando Django y React',
        proyectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/user/e-learning"
    },
    {
        id: 3,
        src: proyecto3,
        titulo: 'Blog Personal con CMS(2022)',
        descripcion: 'Construí un blog personal con un sistema de gestión de contenido(CMS) utilizando WordPress',
        proyectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/user/blogPersonal"
    },
    {
        id: 4,
        src: proyecto4,
        titulo: 'Inventario(2021)',
        descripcion: 'Desarrollé una aplicación de inventario para una pequeña empresa utilizando Java y MySQL',
        proyectoLink: "https://www.google.com.ar",
        githubLink: "https://github.com/user/inventario"
    },
    
])
</script>

<template>
    <div class="galeria">
        <li class="proyecto" v-for="proyecto in misProyectos" :key="proyecto.id">
            <img :src="proyecto.src" :alt="proyecto.titulo">
            <div class="poryecto-info">
                <h3>{{proyecto.titulo}}</h3>
                <p>{{proyecto.descripcion}}</p>
                <div class="proyecto-links">
                    <a :href="proyecto.proyectoLink" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">Ver      Proyecto</a>
                    <a :href="proyecto.githubLink" class="github-link" target="_blank" rel="noopener noreferrer">Ver Código en GitHub</a>
                </div>
            </div>
        </li>

    </div>
</template>

<style scoped>
/* .galeria{
    width: 100%;
    height: 100vh;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    background-image: url('/src/assets/fondo-proyectos.png');
    background-size: cover;
    background-position: center;
    background-position: no-repeat;

} */
/* Estilos fondo animado de Css de la galería
   La clase 'galeria'es el contenedor principal de la galeria de proyectos*/
.galeria{
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    padding: 20px;
    justify-content: center;
    background: linear-gradient(-45deg,#021526,#03346E,#6EACDA,#E2E2B6);
    background-size: 400% 400%;
    animation: gradient 15s ease infinite;
}

/*Define una animacion llamada 'gradient' para cambiar la posicion del fondo*/
@keyframes gradient{
    0%{
        background-position: 0% 50%;
    }
    50%{
        background-position: 100% 50%;
    }
    100%{
        background-position: 0% 50%;
    }
}
/* La clase 'proyecto' es el contenedor individual de cada proyecto */
.proyecto {
    /* Utiliza flexbox para organizar el contenido del proyecto en una columna */
    display: flex;
    /* Establece la dirección de los elementos en columna */
    flex-direction: column;
    /* Agrega un padding de 5px alrededor del proyecto */
    padding: 5px;
    /* Aplica un borde de 2px sólido y color gris claro (#ddd) alrededor del proyecto */
    border: 2px solid #ddd;
    /* Redondea las esquinas del contenedor */
    border-radius: 8px;
    /* Oculta cualquier contenido que se desborde del contenedor */
    overflow: hidden;
    /* Establece un color de fondo claro para el proyecto */
    background-color: #f9f9f9;
    /* Define el ancho máximo del proyecto en 222px */
    max-width: 222px;
    /* Hace que el contenedor se ajuste flexiblemente ocupando al menos 300px de ancho */
    flex: 1 1 300px;
    color: #333;
}

/* Estilo para las imágenes dentro del contenedor 'proyecto' */
.proyecto img {
    /* Hace que la imagen ocupe el 100% del ancho del contenedor */
    width: 100%;
    /* Mantiene la relación de aspecto de la imagen */
    height: auto;
    /* Asegura que la imagen se muestre como un bloque, sin espacio en línea alrededor */
    display: block;
}

/* La clase 'proyecto-info' contiene la información del proyecto */
.proyecto-info {
    display: flex;
    flex-direction: column;
    /* Agrega un padding de 15px alrededor de la información */
    padding: 15px;
    /* Centra el texto dentro del contenedor */
    text-align: center;
}

/* Estilo para los títulos de los proyectos */
.poryecto-info h3 {
    /* Establece un margen superior e inferior de 10px */
    margin: 10px 0;
    /* Define el tamaño de la fuente a 1.3em (relativo al tamaño de fuente del contenedor) */
    font-size: 1rem;
    /* Aplica un color gris oscuro (#333) al texto */
    color: #333;
    text-align: center;
    font-variant: small-caps;
    font-weight:500; 
    height: 55px;  
}

/* Estilo para los párrafos de los proyectos */
.poryecto-info p {
    /* Establece un margen superior e inferior de 10px */
    margin: 10px 0;
    /* Define el tamaño de la fuente a 1em (igual al tamaño de fuente base) */
    font-size: 1em;
    /* Aplica un color gris (#666) al texto */
    color: #666;
    text-align: center;
    margin-top: 10px;
    height: 100px;

}


/* La clase 'proyecto-links' organiza los enlaces y botones del proyecto */
.proyecto-links {
    /* Utiliza flexbox para organizar los enlaces en una columna */
    display: flex;
    /* Establece la dirección de los elementos en columna */
    flex-direction: column;
    /* Establece un espacio de 10px entre los elementos */
    gap: 10px;
    /* Agrega un margen superior de 10px */
    margin-top: 30px;
    text-align: center;

}

/* Estilo para el botón 'Ver Más' dentro de la clase 'proyecto-links' */
.proyecto-links .btn-ver-mas {
    /* Aplica un color de fondo azul (#007BFF) */
    background-color: #007BFF;
    /* Aplica un color de texto blanco */
    color: #fff;
    /* Agrega un padding de 10px en vertical y 15px en horizontal */
    padding: 10px 15px;
    /* Redondea las esquinas del botón */
    border-radius: 5px;
    /* Elimina el subrayado del texto */
    text-decoration: none;
    /* Aplica una transición suave al cambiar el color de fondo */
    transition: background-color 0.3s;
    margin-top: 1rem;
    text-align: center;
}

/* Estilo para cuando el botón 'Ver Más' es hover */
.proyecto-links .btn-ver-mas:hover {
    /* Cambia el color de fondo a un azul más oscuro (#0056b3) */
    background-color: #0056b3;
}

/* Estilo para el enlace a GitHub dentro de la clase 'proyecto-links' */
.proyecto-links .github-link {
    /* Aplica un color gris oscuro (#333) al texto */
    color: #333;
    /* Elimina el subrayado del texto */
    text-decoration: none;
    /* Establece el tamaño de fuente a 0.9em (un poco más pequeño que el tamaño base) */
    font-size: 0.9em;
    margin-bottom: 0.2rem;
}

/* Estilo para cuando el enlace a GitHub es hover */
.proyecto-links .github-link:hover {
    /* Añade un subrayado al texto */
    text-decoration: underline;
}

</style>