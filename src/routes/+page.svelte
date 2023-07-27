<script>
	import Introduction from '$lib/Introduction.svelte';
	import Card from '$lib/Card.svelte';
	import Footer from '$lib/Footer.svelte';
	import { contributions, works, articles } from '$lib/constants/contributions';
</script>

<main>
	<Introduction />
	<section class="contributions">
		<header class="info-header">
			<h2 class="info-h2">Writing</h2>
		</header>
		<div class="info-container">
			{#each articles as article}
				<Card {...article} />
			{/each}
		</div>
		<header class="info-header">
			<h2 class="info-h2">Projects</h2>
		</header>
		<div class="info-container">
			{#each works as work}
				<Card {...work} />
			{/each}
		</div>
		<header class="info-header">
			<h2 class="info-h2">Contributions</h2>
		</header>
		<div class="info-container">
			{#each contributions as contribution}
				<Card {...contribution} />
			{/each}
		</div>
	</section>
	<Footer />
</main>

<style>
	main {
		min-height: 100vh;
	}

	.info-header {
		margin: 2em;
		border-bottom: 4px solid #a71bbd;
		border-bottom-left-radius: 16px;
		overflow: hidden;
	}

	.info-h2 {
		padding: 0.75em;
		padding-bottom: calc(1em - 4px);
		font-size: 2em;
		background: #a71bbd;
		border-radius: 16px 16px 0 0;
		width: fit-content;
	}

	.info-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: space-evenly;
		margin: 1em;
	}

	@media (max-width: 600px) {
		.info-header {
			border-bottom: none;
		}

		.info-h2 {
			border-radius: 16px;
			font-size: 1.5em;
		}
	}
</style>
