<script>
  let current = "";
</script>

<!-- We will cover buttons later on! -->
<button class={current==="messi" ? 'highlight':''} on:click={() => (current = "messi")}>
  Messi
</button>

<button class={current==="ronaldo" ? 'highlight':''} on:click={() => (current = "ronaldo")}>
  Ronaldo
</button>

<button class={current==="neymar" ? 'highlight':''} on:click={() => (current = "neymar")}>
  Neymar
</button>

<style>
  .highlight{
    background-color: rgb(108, 172, 228);
    color: white;
  }
</style>