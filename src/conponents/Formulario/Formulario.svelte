<main>

    <label>
        Título:
        <input type="text" bind:value={valorTitulo}>
    </label>
    <label>
        Contido:
        <textarea bind:value={valorContido}/>
    </label>
    <label>
        URL imaxe:
        <input type="url" bind:value={valorURLimaxe}>
    </label>

    <button on:click={manexadorGuardar}>Guardar</button>

</main>

<aside>
    <Noticias
        titulo={novaNova.titulo}
        contido={novaNova.contido}
        fonteImaxe={novaNova.fonteDaImaxe}
        textoAlternativoImaxe={novaNova.textoAlternativo}
    />
</aside>

<script>

    import Noticias from "../Noticias/Noticias.svelte";

    export let listaNovas

    let valorTitulo = ""
    let valorContido = ""
    let valorURLimaxe = ""
    let novaNova

    function manexadorGuardar() {
        listaNovas.push(novaNova)
        listaNovas = listaNovas
    }

    $: { 
        novaNova =     {
            titulo: valorTitulo,
            contido: valorContido,
            textoAlternativo: "", //ToDo
            fonteDaImaxe: valorURLimaxe
        }
    }

</script>

<style>
    main {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    label {
        display: flex;
        margin: 1rem;
        min-width: 50%;
    }

    label > * {
        margin: 0rem 1rem;
    }

    label input, label textarea {
        flex-grow: 1;
    }

    textarea {
        vertical-align: text-top;
    }
</style>