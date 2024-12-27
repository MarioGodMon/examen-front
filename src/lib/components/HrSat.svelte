<script lang="ts">
    import "../../app.css";

    /** Estilo personalizado que se le será asignado al separador. */
    export let style: string = "";
    /** Estilo personalizado que se le será asignado al Hr. */
    export let hrStyle: string = "";
    /** En caso de necesitar la caja dorada asociada a los estilos de títulos del SAT. */
    export let goldenSquare: boolean = true;
    /** Animar la barra debajo del titulo. */
    export let animateBar: boolean = false;
    /** Ancho de la barra. */
    export let widthBar: number = 0;
</script>

<div class="wraper" {style}>
    <hr style={hrStyle}/>
    {#if goldenSquare}
        <!-- svelte-ignore element_invalid_self_closing_tag -->
        <div
            class="golden-box"
            style={`--width: ${animateBar ? widthBar : 7}%`}
        />
    {/if}
</div>

<style>
    .wraper {
        position: relative;
        width: 80%;
        max-width: 1500px;
        margin: 1%;
    }
    hr {
        position: relative;
        width: 100%;
    }
    .golden-box {
        position: relative;
        top: -2px;
        background-color: #b38e5d;
        height: 5px;
        width: var(--width);
    }
    @media (max-width: 500px) {
        .wraper {
            width: 90%;
        }
    }
</style>