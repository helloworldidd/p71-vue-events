<script setup>

import { ref } from 'vue';


const estadoTitulo = ref(false);
const estadoInput = ref(false);


alert('hola')
</script>



<template>

<h3 :class="{'estilo-titulo': estadoTitulo}">Event Style</h3>

<input
    type="text"
    :class="{'estilo-activo': estadoInput}"
    @focus="estadoInput = true"
    @blur="estadoInput = false"
    placeholder="escribe algo"
>

<button @click="estadoTitulo = !estadoTitulo">click</button>

</template>







<style scoped>


h3{
    margin:  40px;
}

input{
    border: 2px solid #888;
    margin: 40px;
    padding: 10px;
    border-radius: 5px;
}

button{
    margin: 40px;
    padding: 10px 20px;
    border-radius: 5px;
    background-color: #277cd1;
    color: #fff;
    border: none;
    cursor: pointer;
}

.estilo-activo{
    border: 2px solid #27d15a;
    background-color: #bfe2c9;
    transition: all 0.1s ease;
    transform: scale(1.1);
    outline: none;
}

.estilo-titulo{
    
    color: #277cd1;
    transition: all 0.1s ease;
    transform: scale(1.1);


}
</style>