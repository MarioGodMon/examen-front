<script lang="ts">
    import { navigate } from "svelte-routing";
    import Button from "../components/Button.svelte";


</script>
<div class="title">
    <h1 style="color: var(--golden);">Ejercicio 1</h1>
</div>

<div style="margin: 20px;" />

<div class="text">
    Operaciones con valores numéricos.
    <ul style="margin: 10px  20px;">
        <li>Crear una lista de opciones con inputs.</li>
        <li>Éstas opciones deben ser las siguientes: Suma, Resta, Multiplicación.</li>
        <li>Al hacer click en una de esas opciones, se deben abrir 2 inputs.</li>
        <li>Sólo cuando ambos campos estén definidos, se debe realizar la operación. </li>
        <li>Mostrar el resultado de dicha operación. </li>
    </ul>
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