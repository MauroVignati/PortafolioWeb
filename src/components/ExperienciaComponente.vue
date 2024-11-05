<script setup>
import {ref} from 'vue';
const titulo = 'Desarrollador Full Stack';
const fecha = 'Desde Enero / Julio 2024';
const experiencias = ref([
    {id:1, src: '/src/assets/ventas.svg', parrafo: 'Lidere un equipo de 5 desarrolladores en la creación de una plataforma de comercio electrónico que incrementó las ventas en un 35% durante el primr año.'},
    {id:2, src: '/src/assets/appweb.svg', parrafo: 'Diseñé y desarrollé aplicaciones web utilizando Node.js, React y MongoDB, lorando reducir el tiempo de carga de las páginas en un 50%'},
    {id:3, src: '/src/assets/seguridad.svg', parrafo: 'Implementé soluciones de autenticación y autorización, mejorando la seguridad del sitio web y reduciendo los intentos de acceso no autorizado en un 20%.'},
    {id:4, src: '/src/assets/interfase.svg', parrafo: 'Colaboré con deseñadores de UX/UI para crear interfaces de usuario atractivas y fáciles de usar aumentando la satisfacción del cliente en un 15%.'},
    {id:5, src: '/src/assets/procesos.svg', parrafo: 'Automaticé procesos de despliegue continuo utilizando Jenkins y Docker, reduciendo los tiempos de despliegue en un 40%.'}
]);

</script>

<template>
    <nav class="card">
        <h3 class="titulo">{{ titulo.toUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id" >
                <img class="imagen-svg" :src="experiencia.src" :alt="experiencia.parrafo"  width="45rem">
                <p>{{experiencia.parrafo}}</p>
            </li>
            <!-- <li class="item"><img src="/src/assets/ventas.svg" alt="" class="imagen-svg" width="45rem">
                <p>Lidere un equipo de 5 desarrolladores en la creación de una plataforma de comercio electrónico que incrementó las ventas en un 35% durante el primr año.</p>
            </li>
            <li class="item"><img src="/src/assets/appweb.svg" alt="" class="imagen-svg" width="45rem">
                <p>Diseñé y desarrollé aplicaciones web utilizando Node.js, React y MongoDB, lorando reducir el tiempo de carga de las páginas en un 50%</p>
            </li>
            <li class="item"><img src="/src/assets/seguridad.svg" alt="" class="imagen-svg" width="45rem">
                <p>Implementé soluciones de autenticación y autorización, mejorando la seguridad del sitio web y reduciendo los intentos de acceso no autorizado en un 20%.</p>
            </li>
            <li class="item"><img src="/src/assets/interfase.svg" alt="" class="imagen-svg" width="45rem">
                <p>Colaboré con deseñadores de UX/UI para crear interfaces de usuario atractivas y fáciles de usar aumentando la satisfacción del cliente en un 15%.</p>
            </li>
            <li class="item"><img src="/src/assets/procesos.svg" alt="" class="imagen-svg" width="45rem">
                <p>Automaticé procesos de despliegue continuo utilizando Jenkins y Docker, reduciendo los tiempos de despliegue en un 40%.</p>
            </li> -->
        </ul>
    </nav>
</template>

<style scoped>
    .card{
        display: flex;
        flex-direction: column;
        padding: 2rem;
        background-color: rgb(28,41,52);
        border-radius: 15px;
    }
    .titulo{
        color: coral;
        font-size: 1rem;
    }
    .fecha{
        font-size: 1rem;
        color: burlywood;
        margin-bottom: 1rem;
    }
    .listado{
        display: flex;
        flex-direction: column;
    }
    .item{
        align-items: center;
        display: flex;
        padding: 1rem;
        gap: 1.5rem;
    }

    </style>