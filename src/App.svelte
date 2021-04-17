<script>
  import Library from "./library/Library.svelte";

  function handleClick() {
    console.log("clicked", id);
  }
</script>

<main>
  <Library onClick={handleClick} />
</main>

<style>
  main {
    padding: var(--spacingLarge);
  }
</style>
