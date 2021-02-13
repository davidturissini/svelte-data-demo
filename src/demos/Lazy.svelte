<script>
	let data = {
        characterName: undefined,
        loading: false,
    };

    async function loadData() {
        data.loading = true;
        const response = await fetch('https://swapi.dev/api/people/1')
        const character = await response.json();
        data = {
            characterName: character.name,
            loading: false,
        };
    }
</script>

<main>
    <button on:click={loadData}>Load Data</button>
        {#if data.loading === true}
            Loading Character Name...
        {:else if data.characterName !== undefined}
            {data.characterName}
        {/if}
</main>
