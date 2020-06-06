<script>

    export let activeTab;
    export let tabs;

</script>

<div class="tabs">
    <ul>
    {#each tabs as tab}
         <div class:active={tab === activeTab}>
            <li>{tab}</li>
         </div>
    {/each}
    </ul>
</div>

<style>
    .tabs {
        margin-bottom: 40px;
    }

    ul {
        display: flex;
        justify-content: center;
        padding: 0;
        list-style-type: none;
    }

    li {
        margin: 0 16px;
        
    }

    .active {
        color: rgb(255, 102, 0);
        border-bottom: 2px solid red;
    }

</style>