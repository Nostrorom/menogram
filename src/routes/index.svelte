<script lang="ts">
	import QnA from '$lib/QnA.svelte';
	import Icon from '$lib/Icon.svelte';
	import type { Content } from '$types/content';
	import monogram from '$data/monogram';

	const pageContent: Content[] = monogram;
</script>

<h1 class="uppercase text-center pt-10 text-xl tracking-[1rem] text-indigo-300 font-title">
	me<span class="text-fuchsia-600">の</span>gram
</h1>
<div class="pt-10 space-y-1">
	<div class="flex space-x-1 justify-center items-center text-slate-500">
		<p>Built with</p>
		<a
			href="https://kit.svelte.dev/"
			target="_blank"
			rel="noopener noreferrer"
			class="h-6 p-1 lg:p-3 bg-slate-600 text-indigo-50 rounded-md bg-opacity-0 hover:bg-opacity-60 opacity-60 hover:opacity-100"
		>
			<Icon icon="svelte" />
		</a>
		<p class="italic">- source</p>
		<a
			href="https://github.com/Nostrorom/menogram"
			target="_blank"
			rel="noopener noreferrer"
			class="h-6 p-1 lg:p-3 bg-slate-600 rounded-md bg-opacity-0 hover:bg-opacity-60 hover:text-indigo-100"
		>
			<Icon icon="github" />
		</a>
	</div>
	<div class="flex space-x-1 justify-center items-center text-slate-500">
		<p>Also exists in</p>
		<a
			href="https://menogram-astro.vercel.app"
			target="_blank"
			rel="noopener noreferrer"
			class="h-6 p-1 lg:p-3 bg-slate-600 text-indigo-50 rounded-md bg-opacity-0 hover:bg-opacity-60 opacity-60 hover:opacity-100"
		>
			<Icon icon="astro" />
		</a>
		<p class="italic">- source</p>
		<a
			href="https://github.com/Nostrorom/menogram-astro"
			target="_blank"
			rel="noopener noreferrer"
			class="h-6 p-1 lg:p-3 bg-slate-600 rounded-md bg-opacity-0 hover:bg-opacity-60 hover:text-indigo-100"
		>
			<Icon icon="github" />
		</a>
	</div>
</div>
<div class="px-4 md:px-12 lg:px-96 mb-12">
	{#each pageContent as content}
		<QnA {content} />
	{/each}
</div>
