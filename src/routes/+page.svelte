<script>
    import Select from '$lib/selectDropdown.svelte';

    const expertises = [
        { value: "Design" },
        { value: "UI/UX" },
        { value: "Graphic" },
    ];

    const provincies = [
        { value: "Noord-holland" },
        { value: "Zuid-holland" },
        { value: "Utrecht" },
    ];

    const voertalen = [
        { value: "Nederlands" },
        { value: "Engels" },
        { value: "Chinees" },
    ]

    let selectedDesign, selectedDevelopment, selectedLanguage = "";
</script>

    <h1>Select & Option element</h1>
    <Select
        bind:selectedOption={selectedDesign}
        filterLabel="Expertise"
        filter={expertises} 
    />

    <Select
        bind:selectedOption={selectedDevelopment}
        filterLabel="Provincie"
        filter={provincies} 
    />

    <Select
        bind:selectedOption={selectedLanguage}
        filterLabel="Voertaal"
        filter={voertalen}
    />

    <h1>Details & summary</h1>



<style>
    h1 {
        color: rgb(0, 174, 255);
    }


</style>
