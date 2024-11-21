<script>
    export let selectedOption = "";
    export let filterLabel = "";
    export let text = ""
    export let filter = [];
</script>

<select bind:value={selectedOption}>
    <option value="">{filterLabel}</option>
    {#each filter as filter}
        <option value={filter.value}>{filter.value}</option>
    {/each}
</select>

{text}
<!-- <h1>{filterLabel} : {selectedOption}</h1> -->

<style>
    select {
        background-color: inherit;
        border: 1px solid black;
        padding: 1em ;
    }
</style>
  