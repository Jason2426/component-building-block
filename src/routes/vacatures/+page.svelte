<script>
    import Select from "$lib/selectDropdown.svelte";


    const expertises = [
        { value: "Development" },
        { value: "Design" },
        { value: "Traffic" },
        { value: "Management" },
    ];

    const soorten = [
        { value: "Full-time" },
        { value: "Part-time" },
        { value: "Min-max" },
        { value: "Stage" },
    ];

    const provincies = [
        { value: "Noord-holland" },
        { value: "Zuid-holland" },
        { value: "Utrecht" },
        { value: "Gelderland" },
        { value: "Noord-Brabant" },
        { value: "Limburg" },
        { value: "Zeeland" },
    ];

    const voertalen = [
        { value: "Nederlands" },
        { value: "Engels" },
        { value: "Spaans" },
        { value: "Duits" },
        { value: "Chinees" },
    ];

    let selectedExpertise, selectedType, selectedProvince, selectedLanguage = "";
</script>

<main>
    <section class="filters">
        <Select
        bind:selectedOption={selectedExpertise}
        filterLabel="Expertise"
        filter={expertises}
        />
        <Select
            bind:selectedOption={selectedType}
            filterLabel="Soort"
            filter={soorten}
        />
        <Select
            bind:selectedOption={selectedProvince}
            filterLabel="Locatie"
            filter={provincies}
        />
        <Select
            bind:selectedOption={selectedLanguage}
            filterLabel="Voertaal"
            filter={voertalen}
        />
    </section>
</main>

<style>

    .filters {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 1.5em;
    }

</style>