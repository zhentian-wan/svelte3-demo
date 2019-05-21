<script>
    let name;
    const sayHello = () => alert('Hello ' + name);
    const handleInput = e => name = e.target.value;
</script>

<h1>
    Hello:
</h1>
<input type="text" on:change={handleInput} />
<button on:click|preventDefault|once={sayHello}>Say name</button>