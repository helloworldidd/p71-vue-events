<script setup>

import { onMounted, onUnmounted } from 'vue';

const detectarTecla = (event) => {
    if (event.ctrlKey && event.code === 'Space') {
        alert('tecla espacio presionada')
    }
}

onMounted(() => {
    window.addEventListener('keydown', detectarTecla)
})

onUnmounted(() => {
    window.removeEventListener('keydown', detectarTecla)
})





</script>


<template>
    <div>
        <h2>Event Global</h2>
        <p>Este es un evento global</p>
        <p>Presionando 9 en cualquier lugar se lanza la función</p>
    </div>
</template>


<style scoped>

</style>