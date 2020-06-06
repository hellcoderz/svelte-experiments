<script>
	import Tabs from "./components/Tabs.svelte";

	let tabs = ["ENG", "SPA", "FRA"];
	let activeTab = "ENG";
</script>

<main>
	<Tabs {activeTab} {tabs} on:tabChange={(e) => activeTab = e.detail}/>
	{#if activeTab === "ENG"}
		 <h2>Hello from Tab {activeTab}</h2>
	{:else if activeTab === "SPA"}
		 <h2>Hello from Tab {activeTab}</h2>
	{:else}
		 <h2>Hello from Tab {activeTab}</h2>
	{/if}
</main>

<style>
	
</style>