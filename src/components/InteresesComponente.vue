<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLineal.vue';

const intereses = ref([
    '* Me gusta salir a camimar, ir al gimnasio.',
    '* Me gusta todo tipo de musica.',
    '* Me gusta mucho la fotografia.',
    '* Me gusta ver la formula 1.',
    '* Me gusta el rugby.',
    '* Me gusta el futbol, Boquita siempre.',
    '* Me gusta juntarme con mis amigos.',
    '* Me gusta pasar el tiempo jugando con amigos en linea.'

]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLava />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
    .intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 80%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.1rem;
    text-shadow: 3px 3px 6px rgba(255, 255, 255, 0);
}

.item {
    margin-bottom: 1rem;
}
</style>