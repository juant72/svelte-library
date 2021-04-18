<script>
  import Detail from "./detail/Detail.svelte";
  import Library from "./library/Library.svelte";

  let page = "library";
  let pageArgs = {};
  function handleBookSelect(event) {
    page = "Detail";
    pageArgs = event.detail;
  }
</script>

<main>
  {#if page === "Detail"}
    <Detail {...pageArgs} />
  {:else}
    <Library on:book-select={handleBookSelect} />
  {/if}
</main>

<style>
  main {
    padding: var(--spacingLarge);
  }
</style>
