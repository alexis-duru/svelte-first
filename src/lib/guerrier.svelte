<script>
  export let name;

  export let power = 10;

  let exp = 0;
</script>

<div
  id="guerrier"
  on:mousemove={() => {
    exp += 1;
  }}
>
  <h1>{name}</h1>
  <div>{power}</div>
  <p>{exp}</p>
</div>
