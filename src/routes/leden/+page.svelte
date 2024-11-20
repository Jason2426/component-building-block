<script>
    import Select from "$lib/selectDropdown.svelte";


    const expertises = [
        { value: "Development" },
        { value: "Design" },
        { value: "Traffic" },
        { value: "Management" },
    ];

    const branches = [
        { value: "Handel" },
        { value: "Cultuur" },
        { value: "Entertainment" },
        { value: "Onderwijs" },
        { value: "Bouwsector" },
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

    const omvang = [
        { value: "1-10" },
        { value: "10-20" },
        { value: "20-40" },
        { value: "40-80" },
        { value: "80-160" },
        { value: "160-320" },
    ];

    let selectedExpertise, selectedBranch, selectedProvince, selectedCapacity = "";
</script>

<main>
    <section class="filters">
        <Select
        bind:selectedOption={selectedExpertise}
        filterLabel="Expertise"
        filter={expertises}
        />
        <Select
            bind:selectedOption={selectedBranch}
            filterLabel="Branche"
            filter={branches}
        />
        <Select
            bind:selectedOption={selectedProvince}
            filterLabel="Provincie"
            filter={provincies}
        />
        <Select
            bind:selectedOption={selectedCapacity}
            filterLabel="Omvang"
            filter={omvang}
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
