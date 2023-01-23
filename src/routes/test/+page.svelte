<script lang="ts">
	import { fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let mounted = false;

	onMount(() => {
		setTimeout(() => {
			mounted = true;
		}, 200);
	});
</script>

<div class="relative">
	{#if mounted}
		<div class="text-5xl transform translate-y-0 animate-none" in:fly={{ y: 500, duration: 1000 }}>
			Text
		</div>
	{/if}
</div>

<style>
	div {
		font-size: 4rem;
	}
</style>
