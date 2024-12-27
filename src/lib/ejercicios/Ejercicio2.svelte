<script lang="ts">
    import { navigate } from "svelte-routing";
    import Button from "../components/Button.svelte";


</script>


<Button on:click={() => navigate("/")}>
    Regresar
</Button> 

<style>

</style>