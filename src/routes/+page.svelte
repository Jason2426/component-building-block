<script>
    import Dropdown from '$lib/selectDropdown.svelte';

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

<Dropdown
    bind:selectedOption={selectedDesign}
    filterLabel="Expertise"
    filter={expertises} 
/>

<Dropdown
    bind:selectedOption={selectedDevelopment}
    filterLabel="Provincie"
    filter={provincies} 
/>

<Dropdown 
    bind:selectedOption={selectedLanguage}
    filterLabel="Voertaal"
    filter={voertalen}
/>
