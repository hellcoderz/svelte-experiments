<script>
	import SynTable from "./components/SynTable.svelte";
	export let name;

	let tabs = ["eng", "spa", "fra"];
	let activeTab = "eng";
</script>

<main>
	<SynTable {activeTab} {tabs} ></SynTable>
</main>

<style>
	
</style>