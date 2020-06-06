<script>
    import { createEventDispatcher } from "svelte";

    const dispatch = createEventDispatcher(); 

    export let activeTab;
    export let tabs;

</script>

<div class="tabs">
    <ul>
    {#each tabs as tab} 
        <li on:click={() => dispatch("tabChange", tab)}>
            <div class:active={tab === activeTab}>
                {tab}
            </div>
        </li>
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
        margin: 0 5px;
        font-size: 18px;
        color: #555;
        cursor: pointer;
    }

    .active {
        color: rgb(255, 102, 0);
        border-bottom: 2px solid red;
    }

</style>