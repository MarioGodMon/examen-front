<script lang="ts">
    import { navigate } from "svelte-routing";
    import Button from "../components/Button.svelte";


</script>

<div class="title">
    <h1 style="color: var(--golden);">Ejercicio 2</h1>
</div>

<div style="margin: 20px;" />


<div class="text">
    Realizar un formulario, con los siguientes campos :
    <ul style="margin: 10px  20px; ">
        <li>Input para el nombre</li>
        <li>Input para correo electronico</li>
        <li>Input para edad</li>
        <li>Pregunta , Que lenguajes de programacion dominas ? : con las opciones: Rust , C++, Svelte, CSS, HTML</li>
        <li>Pregunta</li>
        <li>Una caja de texto para escribir una opinión</li>
        <li>Un boton para mandar toda la información</li>
    </ul>
    Muestre toda la informacion alamacenada en un log 
</div>


<div class="ejercicio">

</div>

<div style="margin: 20px;" />


<Button on:click={() => navigate("/")}>
    Regresar
</Button> 

<style>
    .title{
        display: flex;
        flex-direction: row;
    }
    .text{
        display: flex;
        flex-direction: column;
        width: 80%;
        border: 3px solid var(--golden);
        font-size: 1.2rem;
        font-weight: bold;
        color: var(--golden);
        padding: 10px;
    }

</style>