<script>
	let characterName;

	fetch('https://swapi.dev/api/people/1')
		.then((resp) => resp.json())
		.then((res) => {
			characterName = res.name;
		})
</script>

<main>
    {#if characterName === undefined}
        Loading Character Name...
    {:else}
        {characterName}
    {/if}
</main>
