<script>
    let name = 'Gabo';
    function changeBackground() {
    var bodyStyle = getComputedStyle(document.body);
    var currentColor = bodyStyle.backgroundColor;

    if (currentColor === 'rgb(255, 0, 0)') {
        document.body.style.backgroundColor = 'white';
    } else {
        document.body.style.backgroundColor = 'red';
    }
}
</script>
<svelte:head>
    <title>Science</title>
    <meta name="description" content="Science" />
    <meta name="keywords" content="Science" />
    <meta name="author" content="Gabo" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="icon" href="/favicon.ico" />
</svelte:head>
<section>
<h1>Bienvenidos a Ciencia con {name}</h1>

<p>La ciencia es un proceso sistemático de adquisición y organización de conocimientos sobre el mundo natural a través de la observación, experimentación y el razonamiento lógico. Busca comprender las leyes y principios que rigen el universo y utiliza métodos rigurosos para validar y ampliar nuestro entendimiento.</p>
<p>
    Entre los grandes científicos que han contribuido significativamente al avance del conocimiento, destacan:
</p>
<ul>
    <li>
        Albert Einstein
    </li>
    <li>
        Marie Curie
    </li>
    <li>
        Charles Darwin
    </li>
    <li>
        Nicolás Copérnico
    </li>
    <li>
        Stephen Hawking
    </li>
</ul>
<div id="button">
    <button on:click={changeBackground}>Change</button>
</div>
</section>
<style>
    section{
        margin: 0 auto;
        width: 80%;
        border: 1px solid black;
        padding: 1em;
        background-color: white;
    }
    h1 {
        color: black;
        text-align: center;
    }
    p {
        text-align: center;
        color: black;
    }
    li {
        color: black;
    }
    #button {
        text-align: center;
    }
    #button button {
        color: purple;
        border-radius: 25px;
        background-color: black;
        border: 1px solid purple;
        padding: 0.5em;
    }
</style>