<script>
    import {onMount} from 'svelte';
    let people = []
    onMount(async () => {
        const response = await fetch('https://swapi.co/api/people/');
        const json = await response.json();
        people = json.results;

        return () => console.log('Destroyed');
    })
</script>

<ul>
    {#each people as {name, height, birth_year}}
        <li>
            <strong>{name}</strong>
            (height: {height}cm, birth year: {birth_year})
        </li>
    {:else}
        <p>loading...</p>
    {/each}
</ul>