<script lang="ts">
    import { navigate } from "svelte-routing";
    import Button from "../components/Button.svelte";


</script>

<div class="title">
    <h1 style="color: var(--golden);">Ejercicio 4</h1>
</div>

<!-- svelte-ignore element_invalid_self_closing_tag -->
<div style="margin: 20px;" />


<div class="text">
    Props en componente.
    <ul style="margin: 10px  20px;">
        <li>Dado el siguiente objeto:</li>
        <!-- let colors = [
                { id: 1, name: 'Rojo' },
                { id: 2, name: 'Azul' },
                { id: 3, name: 'Amarillo' },
                { id: 4, name: 'Verde' },
                { id: 3, name: 'Rosa' }
            ];
        -->
        <li>Iterar sobre este objeto.</li>
        <li>En un componente nuevo, escribir 3 variables que su funcionalidad será ser props</li>
        <li>Hacer una función que elimine uno por uno, elemento de ese objeto.</li>
        <li>Con ayuda de esos props, realizar dicha acción.</li>
    </ul>
</div>

<!-- svelte-ignore element_invalid_self_closing_tag -->
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