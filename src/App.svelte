<script>
  import { onMount } from "svelte";
  import { onDestroy } from "svelte/types/runtime/internal/lifecycle";
  import Count from "./lib/count.svelte";
  import Guerrier from "./lib/guerrier.svelte";

  onMount(() => {
    console.log("App mounted");

    // Posibilité d'un fetch
  });

  // onDestroy(() => {
  //   console.log("App destroyed");
  // });
</script>

<!-- <Count nb={6} /> -->
<h1>GUERRIER</h1>
<Guerrier name="Guerrier 1" />
