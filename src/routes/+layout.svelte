<script lang="ts">
	import './layout.css';
	import favicon from '#lib/assets/favicon.svg';
	import { resolve } from '$app/paths';
	import type { LayoutProps } from './$types';

	let { children }: LayoutProps = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<nav class="flex gap-4 bg-[red] p-4">
	<a href={resolve('/')}>Home</a>
	<a href={resolve('/about')}>About</a>
	<a href={resolve('/blog')}>Blog</a>
</nav>

{@render children()}
