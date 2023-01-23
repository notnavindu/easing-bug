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
		<div in:fly={{ y: 150, duration: 1000 }}>Text</div>
	{/if}
</div>
