<!-- afficher le premier tweet de https://raw.githubusercontent.com/iOiurson/data/master/data/tweets.json -->
<script>
  import { onMount } from "svelte";

  let tweet;

  onMount(async () => {
    const response = await fetch(
      "https://raw.githubusercontent.com/iOiurson/data/master/data/tweets.json"
    );
    const data = await response.json();
    tweet = data[0];
    console.log(tweet);
  });
</script>

{#if tweet}
  <div>
    <h1>{tweet.user.name}</h1>
    <p>{tweet.full_text}</p>
  </div>
{/if}
