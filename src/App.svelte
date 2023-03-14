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

    <section>
        {#each novas as estaNova}
        <Noticias
            titulo={estaNova.titulo}
            contido={estaNova.contido}
            fonteImaxe={estaNova.fonteDaImaxe}
            textoAlternativoImaxe={estaNova.textoAlternativo}
        />
        {/each}
    </section>

{/if}

{#if (vistaActual === "formulario")}

    <h1>Formulario</h1>
    <Formulario bind:listaNovas={novas}/>

{/if}

<script>

    import Noticias from "./conponents/Noticias/Noticias.svelte";
    import Formulario from "./conponents/Formulario/Formulario.svelte";

    let novas = [
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados. Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/picsum/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/1/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/2/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/3/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/4/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/5/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/6/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/5/200/200"
        },
        {
            titulo: "Estudiantes reclama máis horas lectivas.",
            contido: "Os sisdicatos de estudiantes reclaman máis horas lectivas: `Máis horas lectivas implican máis exames, e cantos máis exames máis diversión` indicou o representante dos amotinados.",
            textoAlternativo: "Unha foto calquera", //ToDo
            fonteDaImaxe: "https://picsum.photos/seed/6/200/200"
        },
    ]

    let vistaActual = "noticias"

    function manejadorNavNoticias() {
        vistaActual = "noticias"
    }

    function manejadorNavFormulario() {
        vistaActual = "formulario"
    }

</script>

<style>
    section {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
</style>