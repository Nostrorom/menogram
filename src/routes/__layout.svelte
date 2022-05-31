<script lang="ts">
	import '../app.css';
	import '@fontsource/syncopate';
	import '@fontsource/m-plus-2';
	import Sidebar from '$lib/Sidebar.svelte';

	const switchDarkmode = (): void => {
		if (localStorage.theme === 'light') {
			localStorage.theme = 'dark';
			document.documentElement.classList.add('dark');
		} else {
			localStorage.theme = 'light';
			document.documentElement.classList.remove('dark');
		}
	};
</script>

<body
	class="flex w-screen min-h-screen bg-gradient-to-tl from-slate-900 to-slate-900 via-slate-800 text-violet-200 font-main antialiased text-sm"
>
	<div class="h-screen fixed top-0 w-12 lg:w-20">
		<Sidebar />
	</div>

	<main class="ml-12 lg:ml-20">
		<slot />
	</main>
</body>
