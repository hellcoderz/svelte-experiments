<script>
    export let synonyms;
</script>

<main>
    <ul>
        {#each synonyms as syn}
        <li>{syn}</li>
        {/each}
    </ul>
</main>


<style>
    ul {
        list-style-type: none;
    }
</style>