<script>
	import { onMount } from 'svelte';
	let characterName;

    onMount(async () => {
        const response = await fetch('https://swapi.dev/api/people/1');
        const character = await response.json();
        characterName = character.name;
    })
</script>

<main>
    {characterName}
</main>
