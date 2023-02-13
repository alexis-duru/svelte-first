<script>
  import { onMount, onDestroy } from "svelte";
  import Count from "./lib/count.svelte";
  import Tweet from "./lib/tweet.svelte";
  import Guerrier from "./lib/guerrier.svelte";
  import Horloge from "./lib/horloge.svelte";
  import Tweet2 from "./lib/tweet2.svelte";


  let clockActive = false;

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
<Tweet />
<Tweet2 />

<button on:click={() => (clockActive = !clockActive)}>Toggle</button>

{#if clockActive}
  <Horloge />
{/if}
