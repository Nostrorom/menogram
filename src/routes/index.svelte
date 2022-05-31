<script lang="ts">
	import QnA from '$lib/QnA.svelte';
	import type { Content } from '$types/content';
	import monogram from '$data/monogram';

	const pageContent: Content[] = monogram;
	console.log(monogram);
</script>

{#each pageContent as content}
	<QnA {content} />
{/each}
