<script lang="ts">
	import QnA from '$lib/QnA.svelte';
	import type { Content } from '$types/content';
	import monogram from '$data/monogram';

	const pageContent: Content[] = monogram;
</script>

<h1 class="uppercase text-center pt-10 text-xl tracking-[1rem] text-indigo-300 font-title">
	me<span class="text-fuchsia-600">の</span>gram
</h1>
<div class="px-4 md:px-12 lg:px-96 mb-12">
	{#each pageContent as content}
		<QnA {content} />
	{/each}
</div>
