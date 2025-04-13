<script lang="ts">
	let { children } = $props();
</script>

<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link
		href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&family=JetBrains+Mono:ital,wght@0,100..800;1,100..800&display=swap"
		rel="stylesheet"
	/>

	<link
		rel="stylesheet"
		href="https://cdnjs.cloudflare.com/ajax/libs/prism-themes/1.9.0/prism-one-dark.min.css"
		integrity="sha512-c6S8OdtvoqZCbMfA1lWE0qd368pLdFvVHVILQzNizfowC+zV8rmVKdSlmL5SuidvATO0A7awDg53axd+s/9amw=="
		crossorigin="anonymous"
		referrerpolicy="no-referrer"
	/>

	<script>
		if (
			localStorage.theme === 'dark' ||
			(!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)
		) {
			document.documentElement.setAttribute('data-theme', 'dark');
			// @ts-ignore
			window.theme = 'dark';
		} else {
			document.documentElement.setAttribute('data-theme', 'light');
			// @ts-ignore
			window.theme = 'light';
		}
	</script>
</svelte:head>

{@render children()}
