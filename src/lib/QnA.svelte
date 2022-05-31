<script lang="ts">
	import { slide } from 'svelte/transition';
	import type { Content } from '$types/content';

	export let open: boolean = true;

	export let content: Content;
</script>

<div
	on:click={() => {
		open = !open;
	}}
	class="border-l-2 border-indigo-800 bg-neutral-500 bg-opacity-25 italic rounded-md"
>
	<div>
		{content.q}
	</div>
	<slot name="q" />
</div>
{#if open}
	<div transition:slide class="p-2">
		<slot name="a" />
	</div>
{/if}
