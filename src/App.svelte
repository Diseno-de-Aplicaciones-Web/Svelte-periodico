<nav>
    <ul>
        <li>
            <button on:click={manejadorNavNoticias}>
                Noticias
            </button>
        </li>
        <li>
            <button on:click={manejadorNavFormulario}>
                Formulario
            </button>
        </li>
    </ul>
</nav>

{#if (vistaActual === "noticias")}

    <h1>Novas</h1>

    {#each novas as estaNova}
        <Noticias
            titulo={estaNova.titulo}
            contido={estaNova.contido}
            fonteImaxe={estaNova.fonteDaImaxe}
            textoAlternativoImaxe={estaNova.textoAlternativo}
        />
    {/each}

{/if}

{#if (vistaActual === "formulario")}

    <h1>Formulario</h1>
    <Formulario bind:listaNovas={novas}/>

{/if}

<script>

    import Noticias from "./conponents/Noticias/Noticias.svelte";
    import Formulario from "./conponents/Formulario/Formulario.svelte";

    let novas = []
    let vistaActual = "noticias"

    function manejadorNavNoticias() {
        vistaActual = "noticias"
    }

    function manejadorNavFormulario() {
        vistaActual = "formulario"
    }

</script>