<script>
	import { fly } from 'svelte/transition';
	import { onMount } from 'svelte';
	import { quadOut } from 'svelte/easing';

	let mounted = false;

	onMount(() => {
		mounted = true;
	});
</script>

{#if mounted}
	<main class="w-full h-screen flex items-center justify-center">
		<div class="w-full max-w-7xl flex">
			<div class="w-3/4 flex flex-col gap-3">
				<div class="h-40 relative overflow-hidden">
					<div
						class="absolute inset-0 text-9xl"
						in:fly={{ y: 150, duration: 1100, easing: quadOut }}
					>
						Some
					</div>
				</div>
			</div>
			<div class="w-1/4 bg-blue-300" />
		</div>
	</main>
{/if}
