<script lang="ts">
	import { fly } from 'svelte/transition';
	import { onMount } from 'svelte';

	let mounted = false;

	onMount(() => {
		setTimeout(() => {
			mounted = true;
		}, 100);
	});
</script>

{#if mounted}
	<div class="relative">
		<div class="transform translate-y-0 animate-none" in:fly={{ y: 150, duration: 1000 }}>Text</div>
	</div>
{/if}
