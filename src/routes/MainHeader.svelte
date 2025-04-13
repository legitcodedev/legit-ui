<script lang="ts">
	import { Container } from '$lib/index.js';

	const links = [
		{
			text: 'Getting started',
			href: '/'
		},
		{
			text: 'Components',
			href: '/'
		},
		{
			text: 'Examples',
			href: '/'
		}
	];
</script>

<Container class="flex h-16 items-center">
	<p class="mr-auto text-lg font-semibold">
		<a href="/">Legit UI</a>
	</p>

	<nav class="flex items-center gap-6">
		{#each links as link}
			<a href={link.href} class="text-foreground-muted text-sm font-medium">{link.text}</a>
		{/each}
	</nav>
</Container>
