
<h1>Novas</h1>

{#each novas as estaNova}
    <Noticias
        titulo={estaNova.titulo}
        contido={estaNova.contido}
        fonteImaxe={estaNova.fonteDaImaxe}
        textoAlternativoImaxe={estaNova.textoAlternativo}
    />
{/each}

<h1>Formulario</h1>
<Formulario bind:listaNovas={novas}/>


<script>

    import Noticias from "./conponents/Noticias/Noticias.svelte";
    import Formulario from "./conponents/Formulario/Formulario.svelte";
    let novas = []

</script>