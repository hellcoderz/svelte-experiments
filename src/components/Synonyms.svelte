<script>
    import Tabs from "./Tabs.svelte";
    import SynonymsList from "./SynonymsList.svelte";

	let tabs = ["ENG", "SPA", "FRA", "GER", "ITA"];
    let activeTab = "ENG";
    let synMap = {
        "ENG": ["eng1", "eng2"],
        "SPA": [],
        "FRA": [],
        "GER": [],
        "ITA": []
    }
</script>

<main>
	<Tabs {activeTab} {tabs} on:tabChange={(e) => activeTab = e.detail}/>
	{#if activeTab === "ENG"}
		 <SynonymsList synonyms={synMap[activeTab]}/>
	{:else if activeTab === "SPA"}
		 <SynonymsList synonyms={synMap[activeTab]}/>
	{:else if activeTab === "FRA"}
		 <SynonymsList synonyms={synMap[activeTab]}/>
    {:else if activeTab === "GER"}
		 <SynonymsList synonyms={synMap[activeTab]}/>
    {:else if activeTab === "ITA"}
		 <SynonymsList synonyms={synMap[activeTab]}/>
	{/if}
</main>

<style>
	
</style>