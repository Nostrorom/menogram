<script lang="ts">
	import '../app.css';
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

<body class="flex w-screen">
	<div class="h-screen fixed top-0 w-12">
		<Sidebar />
	</div>

	<main class="mr-12">
		<slot />
	</main>
</body>
