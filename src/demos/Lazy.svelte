<script>
	let data = {
        characterName: undefined,
        loading: false,
    };

    function loadData() {
        data.loading = true;
        fetch('https://swapi.dev/api/people/1')
            .then((resp) => resp.json())
            .then((res) => {
                data = {
                    characterName: res.name,
                    loading: false,
                };
            });
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
