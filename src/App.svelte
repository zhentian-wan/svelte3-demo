<script>
  import Firstname from "./Firstname.svelte";
  import Counter from "./Counter.svelte";
  import Hello from "./Hello.svelte";
  import People from "./People.svelte";
  export let name;
  export let age;

  let cities = [
    {
      id: "3287",
      name: "London"
    },
    {
      id: "3914",
      name: "Warsaw"
    },
    {
      id: "8833",
      name: "Berlin"
    },
    {
      id: "3231",
      name: "Lisbon"
    }
  ];
</script>

<style>
  h1 {
    color: purple;
  }
</style>

<h1>{name.toUpperCase()}!</h1>
<h2>In age {age}!</h2>
<Firstname firstname={'wan'} />
<Counter />
<ul>
  {#each cities as { id, name }, index}
    <li>{index + 1}: {name} (id: {id})</li>
  {/each}
</ul>
<Hello />
<People />
