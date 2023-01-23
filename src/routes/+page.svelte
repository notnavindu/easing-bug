<script lang="ts">
	import { fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let mounted = false;

	onMount(() => {
		mounted = true;
	});
</script>

{#if mounted}
	<div in:fly={{ y: 500, duration: 1000 }}>Text</div>
{/if}

<style>
	div {
		font-size: 4rem;
	}
</style>
