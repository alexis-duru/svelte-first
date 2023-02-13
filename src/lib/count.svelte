<script>
  export let nb;

  const coucou = "coucou";
  let count = 0;

  $: double = nb * 2;
</script>

<div>{nb}</div>
<div>{count}</div>
<div>{double}</div>
