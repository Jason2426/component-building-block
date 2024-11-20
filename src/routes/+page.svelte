<script>
    import Select from '$lib/selectDropdown.svelte';
    import Detail from '$lib/detailDropdown.svelte';

    const opties = [
        { value: "Dit is optie 1" },
        { value: "Dit is optie 2" },
        { value: "Dit is een echte optie" },
        { value: "Dit is ook een optie" },
    ];

    let selectedOption;
</script>

<div class="container">
    <a href="/vacatures">Vacaturepagina</a>
    <a href="/leden">Ledenpagina</a>
    <h1>Select & Option element</h1>
    <section class="filters">
        <Select
            bind:selectedOption={selectedOption}
            filterLabel="Test"
            filter={opties}
        />
    </section>

    <h1>Details & summary</h1>
    <Detail
        filterLabel="Expertise"
    />

    <h1>Imported listbox</h1>
</div>

<style>
    .container {
        container-type: inline-size;
        padding: 3em;
        border: solid 1px black
    }

    h1 {
        color: rgb(0, 174, 255);
    }
    
    .filters{
        display: flex;
        gap: 1em;
        flex-wrap: wrap;
    }
</style>