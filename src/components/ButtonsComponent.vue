<script setup>


const saludo = () => {
    alert('hello!!!!')
}

const saludoPorConsola = () => {
    console.log('hola por consola', new Date())
}


</script>

<template>

    <h3>click</h3>
    <button @click="saludo" class="btn">click</button>
    <button v-on:click="saludo" class="btn">click</button>

    <h3>Doble click</h3>
    <button @dblclick="saludo" class="btn">doble click</button>


        <br><br><br><br><br><br>

    <h3>Mouse over</h3>
    <div @mouseover="saludoPorConsola" class="block">mouse over</div>

    <h3>Mouse out</h3>
    <div @mouseout="saludoPorConsola" class="block">mouse out</div>

    <h3>Mouse move</h3>
    <div @mousemove="saludoPorConsola" class="block">mouse move</div>

    <h3>Scroll</h3>
    <div @scroll="saludoPorConsola" class="block-scroll">scroll Lorem, ipsum dolor sit amet consectetur adipisicing elit. Asperiores minima adipisci dolores velit, ratione mollitia harum voluptas numquam eius molestiae odit debitis voluptatem, vero rerum veritatis aperiam illum ipsam quaerat officiis nisi! Iusto ad rerum dolorem tenetur rem quidem voluptas sit consequuntur quod nisi! Exercitationem ducimus cupiditate nihil nobis voluptatem aspernatur, iure officia vero fugit totam voluptatibus similique, magnam aliquam nulla eius non vitae unde debitis placeat! Obcaecati ex culpa nesciunt suscipit perferendis tempore dolore eum sapiente, quo ipsa impedit quod porro cupiditate provident dolorum eveniet asperiores voluptatem illum? Illo, tenetur quasi! Quaerat, hic. Doloribus corrupti debitis animi! Non, voluptates.</div>

        <br><br><br><br><br><br>







    <h3>Input (ingresar texto)</h3>
    <input type="text" @input="saludoPorConsola" class="input">

    <h3>Change (cambiar texto)</h3>
    <input type="text" @change="saludoPorConsola" class="input">

    <h3>Focus (enfocar)</h3>
    <input type="text" @focus="saludoPorConsola" class="input">
    
    <h3>Blur (sacar el foco)</h3>
    <input type="text" @blur="saludoPorConsola" class="input">

    <br><br><br><br><br><br>






    <h3>Keydown (tecla presionada)</h3>
    <input type="text" @keydown="saludoPorConsola" class="input">

    <h3>KeyDown Escape (escape)</h3>
    <input type="text" @keydown.escape="saludoPorConsola" class="input">

    <h3>KeyDown Ctrl + ALT + K</h3>
    <input type="text" @keydown.ctrl.alt.k="saludoPorConsola" class="input">
    <br><br><br><br><br><br>




    <h3>Keyup (tecla soltada)</h3>
    <input type="text" @keyup="saludoPorConsola" class="input">

    <h3>Keyup Enter (enter)</h3>
    <input type="text" @keyup.enter="saludoPorConsola" class="input">

    <h3>Keyup Tab (tab)</h3>
    <input type="text" @keyup.tab="saludoPorConsola" class="input">

    <br><br><br><br><br><br>







    <h3>Submit (formulario enviado)</h3>
    <form @submit.prevent="saludoPorConsola" class="block-form">
        <input type="text" class="input">
        <button type="submit" class="btn">enviar</button>
    </form>


<br>
<br>
<br>
<br>
<br>




</template>


<style scoped>

    h3{
        margin: 40px 10px 0 10px;
        padding-top: 10px;
        border-top: 1px solid #000;
    }

    .block{
        width: 200px;
        height: 100px;
        background-color: #a3e2e8;
        margin: 10px;
        padding: 10px;
        border-radius: 5px;

    }

    .block-scroll{
        width: 200px;
        height: 100px;
        background-color: #a3e2e8;
        margin: 10px;
        padding: 10px;
        border-radius: 5px;
        overflow: scroll;
    }

    .block-form{
        width: 240px;
        height: auto;
        background-color: #94cb6d;
        margin: 10px;
        padding: 10px;
        border-radius: 5px;
    }


    .input{
        background-color: #a59a9a;
        color: white;
        border: none;
        padding: 10px 20px;
        border-radius: 5px;
        cursor: pointer;
        margin: 10px;
    }

    .btn{
        background-color: #db7575;
        color: white;
        border: none;
        padding: 10px 20px;
        border-radius: 5px;
        cursor: pointer;
        margin: 10px;
    }
    .btn:hover{
        background-color: #a85555;

    }
</style>