<script setup>

import { h, ref } from 'vue';

const estadoPopUp = ref(false);

</script>


<template>
    <h3>pop up</h3>

    <button @click="estadoPopUp = true" class="btn btn--abrir">click</button>

    <div v-if="estadoPopUp" class="contenedor-popup">
        <div  class="popup">
            <h4>pop up</h4>
            <p>Lorem ipsum dolor sit amet.</p>
            <input type="text" placeholder="ingrese contraseña">
            <button @click="estadoPopUp = false" class="btn btn--cerrar">cerrar</button>
        </div>
    </div>

</template>


<style scoped>


.contenedor-popup{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;

}
.popup{
    background: #fff;
    width: 300px;
    height: fit-content;
    margin: 30px;
    padding: 30px;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 20px;
}


.btn{
    background: #a8a8a8;
    color: #fff;
    padding: 10px 20px;
    border-radius: 10px;
    cursor: pointer;
}

.btn--abrir{
    background: #8baad3;
}

.btn--cerrar{
    background: #d38b8b;
}

.btn:hover{
    filter: brightness(0.7);
}


input{
    padding: 10px 20px;
    border-radius: 10px;
    border: 1px solid #a8a8a8;
}
</style>