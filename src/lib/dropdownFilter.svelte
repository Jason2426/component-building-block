<script>
    export let selectedOption = "";
    export let filterLabel = "";
    export let filter = [];
</script>

<select bind:value={selectedOption}>
    <option value="">{filterLabel}</option>
    {#each filter as filter}
        <option value={filter.value}>{filter.value}</option>
    {/each}
</select>

<h2>De gebruiker kiest : {selectedOption}</h2>

<style>
    h2 {
        color: white;
    }
    select {
        background-color: inherit;
        color: white;
        border: 1px solid white;
        padding: 1em 1.5em;
    }
</style>
  