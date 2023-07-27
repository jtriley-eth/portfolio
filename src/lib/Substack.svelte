<script>
	import substack from '$lib/assets/substack.png';
	export let width = 24;
	export let height = 24;
	export let className = '';
	export let link = '';
</script>

<a href={link} class="pill">
	<img alt="Substack Logo" src={substack} {width} {height} class={className} />

	<p class="text">Article</p>
</a>

<style>
	.pill {
		background: #a71bbd;
		border-radius: 1000px;
		width: fit-content;
		display: flex;
		align-items: center;
		font-size: 0.75em;
		color: #f0f0f0;
		padding: 8px;
		text-decoration: none;
	}

	.text {
		padding-left: 12px;
	}
</style>
