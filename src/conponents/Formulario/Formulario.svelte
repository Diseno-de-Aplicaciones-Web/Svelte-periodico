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

<Noticias
    titulo={novaNova.titulo}
    contido={novaNova.contido}
    fonteImaxe={novaNova.fonteDaImaxe}
    textoAlternativoImaxe={novaNova.textoAlternativo}
/>

<script>

    import Noticias from "../Noticias/Noticias.svelte";

    export let listaNovas

    let valorTitulo = ""
    let valorContido = ""
    let valorURLimaxe = ""
    let novaNova

    function manexadorGuardar() {
        const novaLista = [...listaNovas]
        novaLista.push(novaNova)
        listaNovas = novaLista
    }

    /*
    function manexadorGuardar() {
        listaNovas.push(novaNova)
        listaNovas = listaNovas
    }
    */

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

</style>