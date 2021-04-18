<script>
  import { onMount } from "svelte";
  import { httpGet } from "../common/api.js";
  export let id;
  onMount(async () => {
    await httpGet("/" + id);
  });
</script>

<div>Detail page - {id}</div>
