<script lang="ts">
	export let items: string[] = [];
</script>

<ul>
	{#each items as item}
		<li>{item}</li>
	{/each}
</ul>
