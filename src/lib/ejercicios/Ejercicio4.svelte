<script lang="ts">
    import { navigate } from "svelte-routing";
    import Button from "../components/Button.svelte";


</script>
<div class="title">
    <h1 style="color: var(--golden);">Ejercicio 4</h1>
</div>

<div style="margin: 20px;" />

<div class="text">
    Asincronia.
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