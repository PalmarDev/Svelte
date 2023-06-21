<!-- ScientistBio.svelte -->
<script>
    export let scientist;
    let isExpanded = false;
  
    function toggleExpansion() {
      isExpanded = !isExpanded;
    }
  </script>
  
  <div class="todo">
    <div class="nameButton">
      <img src="{scientist.img}" alt="{scientist.name}">
      <h3>{scientist.name}</h3>
      <button on:click={toggleExpansion}>
        {isExpanded ? '▲' : '▼'}
      </button>
    </div>
    <div class="bio">
      {#if isExpanded}
        <p>{scientist.biography}</p>
      {/if}
    </div>
  </div>
  
  <style>
    .todo {
      display: flex;
      flex-direction: column;
      margin: 0 auto;
      width: 80%;
      border: 1px solid black;
      padding: 1em;
      background-color: white;
    }

    .todo img {
      width: 95px;
      height: 100px;
      border-radius: 50%;
    }

    .bio p{
        text-align: justify;
    }
  
    .nameButton {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  
    button {
      width: 2em;
      height: 2em;
    }
  </style>
  