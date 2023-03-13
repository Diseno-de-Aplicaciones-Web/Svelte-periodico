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

<button>Guardar</button>

<Noticias
    titulo={novaNova.titulo}
    contido={novaNova.contido}
    fonteImaxe={novaNova.fonteDaImaxe}
    textoAlternativoImaxe={novaNova.textoAlternativo}
/>

<script>

    import Noticias from "../Noticias/Noticias.svelte";

    let valorTitulo = ""
    let valorContido = ""
    let valorURLimaxe = ""
    let novaNova

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