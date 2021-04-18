<script>
  import Detail from "./detail/detail.svelte";
  import Library from "./library/Library.svelte";

  let page = "library";
  let pageArgs = {};
  function handleBookSelect(event) {
    page = "detail";
    pageArgs = event.detail;
  }
</script>

<main>
  {#if page === "detail"}
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
