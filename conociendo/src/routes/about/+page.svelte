<script>
    import ScientistBio from "./ScientistBio.svelte";
    import { scientists } from "./js/scientists.js";

  </script>
  
  <svelte:head>
    <title>About Scientist</title>
    <meta name="description" content="About page" />
    <meta name="keywords" content="About" />
    <meta name="author" content="Gabo" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="icon" href="/favicon.ico" />
  </svelte:head>
  
  <section>
    {#each scientists as scientist}
      <ScientistBio {scientist} />
    {/each}
  </section>
  
  <style>
    section {
      margin: 0 auto;
      width: 80%;
      border: 1px solid black;
      padding: 1em;
      background-color: white;
    }
  </style>
  