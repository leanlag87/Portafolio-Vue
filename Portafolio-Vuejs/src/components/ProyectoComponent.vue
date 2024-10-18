<script setup>
import { ref } from 'vue' // Importamos ref de vue para crear una referencia reactiva

const proyectos = ref([
    {
        id: 1,
        nombre: 'Pagina de Starbuck',
        descripcion: 'Creé un clon de la página de inicio de Starbucks con React y CSS.',
        imagen: '/src/assets/673_1x_shots_so.png',
        urlProyecto: 'https://proyecto1.com',
        urlGithub: 'https://github.com/leanlag87/Starbucks-React/tree/master/tarea-01',
    },
    {
        id: 2,
        nombre: 'Formulario de inicio Login',
        descripcion: 'Creé un formulario de login y register con HTML, CSS y JavaScript.',
        imagen: '/src/assets/836shots_so.png',
        urlProyecto: 'https://form-interactivo.netlify.app/',
        urlGithub: 'https://github.com/leanlag87/login-and-register-final',
    },
    {
        id: 3,
        nombre: 'To Do List App',
        descripcion: 'Creé una aplicación de lista de tareas con React y Bootstrap.',
        imagen: '/src/assets/373shots_so.png',
        urlProyecto: 'https://proyecto1.com',
        urlGithub: 'https://github.com/leanlag87/Listas-react',
    },
    {
        id: 4,
        nombre: 'Carrito de Compras',
        descripcion: 'Creé un carrito de compras para simular la compras de frutas.',
        imagen: '/src/assets/233shots_so.png',
        urlProyecto: 'https://proyecto1.com',
        urlGithub: '',
    },
    {
        id: 5,
        nombre: 'App de Rick and Morty',
        descripcion: 'Creé una App de Rick and Morty consumiendo una API para mostrar los personajes, con React y Bootstrap .',
        imagen: '/src/assets/517shots_so.png',
        urlProyecto: 'https://proyecto1.com',
        urlGithub: 'https://github.com/leanlag87/rick-and-morty-react',
    },
    {
        id: 6,
        nombre: 'Pagina de Rockstar',
        descripcion: 'Creé una pagina clon de la pagina de Rockstar de videos juegos, con tecnologias como React y CSS, etc.',
        imagen: '/src/assets/687_1x_shots_so.png',
        urlProyecto: 'https://proyecto1.com',
        urlGithub: 'https://github.com/leanlag87/rockstar-react',
    },
])

</script>


<template>
    <div class="cards">

        <div v-for="proyecto in proyectos" :key="proyecto.id" class="card">
            <img :src="proyecto.imagen" alt="imagen proyecto" />
            <div class="content">
                <h2>{{ proyecto.nombre }}</h2>
                <p>{{ proyecto.descripcion }}</p>
                <a :href="proyecto.urlProyecto" target="_blank" rel="noopener noreferrer">Ver proyecto</a>
                <a :href="proyecto.urlGithub" target="_blank" rel="noopener noreferrer">Ver código</a>
            </div>
        </div>

    </div>

</template>

<style scoped>
.cards {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
    background-image: url('/src/assets/2508252.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    padding: 20px;
    margin-top: 20px;
    filter: drop-shadow(1px 1px 5px rgb(66, 184, 131));
    cursor: pointer;
}

.card {
    width: 300px;
    border: 1px solid #ccc;
    border-radius: 5px;
    overflow: hidden;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    background-color: rgb(26, 26, 26);

}

img {
    width: 100%;
    height: 200px;
    object-fit: cover;
}

.content {
    padding: 20px;
}

h2 {
    margin: 0;
    font-size: 20px;
    color: rgb(225, 225, 225);
}

p {
    margin: 10px 0;
    color: rgb(151, 147, 147);
}

a {
    display: block;
    margin-top: 10px;
    text-align: center;
    background-color: rgb(66, 184, 131);
    color: black;
    padding: 10px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: bold;
}

a:hover {
    background-color: rgb(66, 184, 131, 0.8);
    filter: drop-shadow(1px 1px 5px azure);
}
</style>
