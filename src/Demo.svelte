<script>
    import Simple from './demos/Simple.svelte';
    import Loading from './demos/Loading.svelte';
    import Lazy from './demos/Lazy.svelte';
</script>

<main>
    <section>
        <header>
            <h2>
                Fetching Data
            </h2>
        </header>
        <Simple />
    </section>
    <section>
        <header>
            <h2>
                Fetching Data with Loading Screen
            </h2>
        </header>
        <Loading />
    </section>
    <section>
        <header>
            <h2>
                Lazy Loading Data
            </h2>
        </header>
        <Lazy />
    </section>
</main>
