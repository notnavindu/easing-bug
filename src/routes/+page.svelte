<script>
	import { fly } from 'svelte/transition';
	import { onMount } from 'svelte';
	import { circOut } from 'svelte/easing';

	let mounted = false;

	onMount(() => {
		mounted = true;
	});
</script>

{#if mounted}
	<div in:fly={{ y: 150, duration: 1100, easing: circOut }}>Text</div>
{/if}
