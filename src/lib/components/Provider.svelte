<script lang="ts">
	let { children } = $props();
</script>

<svelte:head>
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
