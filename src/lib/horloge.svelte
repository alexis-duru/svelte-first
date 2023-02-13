<!-- Affiche et désaffiche l'heure dans la page avec onMount et onDestroy -->
<script>
  import { onMount, onDestroy } from "svelte";

  let time = new Date();
  $: seconds = time.getSeconds();
  $: minutes = time.getMinutes();
  $: hours = time.getHours();

  onMount(() => {
    const i = setInterval(() => {
      time = new Date();
    }, 1000);

    return () => {
      clearInterval(i);
    };
  });
</script>

<div>{time}</div>
<div>{seconds}</div>
<div>{minutes}</div>
<div>{hours}</div>
