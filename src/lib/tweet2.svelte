<script>
  import { onMount } from "svelte";

  let tweets = [];

  $: tweet1 = tweets[0];

  onMount(async () => {
    const response = await fetch(
      "https://raw.githubusercontent.com/iOiurson/data/master/data/tweets.json"
    );

    tweets = await response.json();
  });
</script>

{#if tweet1 != undefined}
  <div>{tweet1.full_text}</div>
{/if}
