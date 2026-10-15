<script lang="ts">
	let count = $state(1);
	let isAboveFive = $derived(count > 5);
</script>

<h1 class="text-2xl font-bold">About</h1>

<div>
	<p class="text-xl font-semibold">{count}</p>
</div>

{#if isAboveFive}
	<p>Count is greater than 5</p>
{/if}

<button onclick={() => count++} class="rounder border bg-[blue] px-3 py-1 text-white">
	Update Count
</button>
