<article>
    <h2>{titulo}</h2>
    <p>{contido}</p>
    <img src={fonteImaxe} alt={textoAlternativoImaxe}>
</article>

<script>
    export let titulo = "..."
    export let contido = "..."
    export let fonteImaxe = "https://picsum.photos/200/300"
    export let textoAlternativoImaxe = "...";
</script>

<style>
    article {
        display: grid;
        width: 400px;
        height: 300px;
        grid-template-rows: 5em auto;
        grid-template-columns: 1fr 1fr;
        margin: 1rem;
    }

    h2, p {
        margin: 0px;
        padding: 1rem;
        text-overflow: ellipsis;
        overflow: hidden;
    }

    h2 {
        grid-row: 1/2;
        grid-column: 1/3;
        align-self: center;
    }

    p {
        grid-row: 2/3;
        grid-column: 1/2;
        text-align: justify;
    }

    img {
        grid-row: 2/3;
        grid-column: 2/3;
    }
</style>