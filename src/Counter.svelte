<script>
  let count = 0;
  $: squared = count ** 2;
  $: squaredMinusOne = squared - 1;

  const handleClick = () => count++;
</script>

<button on:click={handleClick}>Counter: {count}</button>
<p>Square of the counter is {squared}</p>
<p>Square of the counter minus one is {squaredMinusOne}</p>
