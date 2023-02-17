<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  let title = "What is Deez?"
  const handleClick = () => {
    if (title === "What is Deez?") {
      title = "Deez Nuts"
    }
  }
  const handleReset = () => {
    if (title === "Deez Nuts") {
      title = "What is Deez?"
    }
  }
</script>

<main class="container">
  <h1 id="title">{title}</h1>
  <button on:click={handleClick}>Deez WHAT?</button>
  <br>
  <a on:click={handleReset} id="reset">Reset</a>

</main>

<style>
  .container {
    display: block
  }
  #title {
    filter: drop-shadow(0 0 2rem blue);
  }
  button:hover {
    filter: drop-shadow(0 0 7em #646cffaa);
  }
  #reset {
    cursor: pointer;
    margin: 0px 2px 2px 0px;
    position: relative;
    top: 50px;
  }
  #reset:hover {
    color: red;
  }
</style>
