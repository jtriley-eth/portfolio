<script>
	// DUP0
	import Github from './Github.svelte';
	import Substack from './Substack.svelte';

	export let title = '';
	export let overview = '';
	export let details = '';
	export let link = '';
</script>

<div class="card">
	<h3 class="title">{title}</h3>
	<p class="text">{overview}</p>
	{#if details != ''}
		<p class="text">{details}</p>
	{/if}
	<!-- DUP0 -->
	{#if link.startsWith('https://github.com/')}
		<Github {link} />
	{:else}
		<Substack {link} />
	{/if}
</div>

<style>
	.card {
		width: 600px;
		min-height: 250px;
		margin: 1em;
		padding: 16px;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		font-size: 1.2em;
		background: #232023;
		border-radius: 16px;
		transition-duration: 0.2s;
		box-shadow: 2px 2px 2px #000;
	}

	.card:hover {
		background: #2b282b;
		box-shadow: 4px 4px 4px #000;
	}

	.title {
		font-weight: 700;
	}

	.text {
		padding-bottom: 16px;
		padding-top: 16px;
		font-weight: 100;
	}
</style>
