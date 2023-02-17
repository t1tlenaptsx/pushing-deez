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

<main>
  <h1 id="title">{title}</h1>
  <button on:click={handleClick}>Deez WHAT?</button>

  <a on:click={handleReset} id="reset">Reset</a>

</main>

<style>
  #title {
    filter: drop-shadow(0 0 2rem blue);
  }
  button:hover {
    filter: drop-shadow(0 0 7em #646cffaa);
  }
  #reset {
    cursor: pointer;
  }
  #reset:hover {
    color: red;
  }
</style>
