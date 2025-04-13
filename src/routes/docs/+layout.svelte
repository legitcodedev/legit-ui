<script lang="ts">
	import { Container } from '$lib/index.js';
	import { twJoin } from 'tailwind-merge';
	import MainHeader from '../MainHeader.svelte';

	let { children } = $props();
</script>

<MainHeader />

<Container
	class={twJoin(
		'prose prose-neutral prose-base dark:prose-invert',
		'prose-headings:font-bold prose-h1:text-display-sm prose-h2:text-display-xs prose-h2:mt-9',
		'prose-pre:!rounded-md prose-pre:text-md prose-pre:!bg-background-muted',
		'prose-a:font-semibold',
		'flex-1 pb-11 pt-7'
	)}
>
	{@render children()}
</Container>
