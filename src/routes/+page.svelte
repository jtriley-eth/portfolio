<script>
    import Card from "../lib/Card.svelte";
    import { contributions, works } from "../lib/constants/contributions";
</script>

<header class="banner">
	<h1 class="name">jtriley.eth</h1>
</header>


<main>
	<section class="overview">
		<h2 class="role">Ethereum Virtual Machine Engineer,</h2>
		<h2 class="role">Security Researcher</h2>
	</section>
    <!-- <iframe title="preview" src="https://open.substack.com/pub/jtriley/p/ethereum-virtual-machine-language" width="300" height="200"></iframe> -->
	<section class="contributions">
		<header class="info-header">
			<h2 class="info-h2">Open Source Contributions</h2>
		</header>
		<div class="info-container">
            {#each contributions as contribution}
                <Card {...contribution} />
            {/each}
		</div>
		<header class="info-header">
			<h2 class="info-h2">Open Source Projects</h2>
		</header>
		<div class="info-container">
            {#each works as work}
                <Card {...work} />
            {/each}
		</div>
	</section>
</main>

<style>
	.banner {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		border-bottom: 1px solid #e6dcd5;
	}

	.name {
		font-size: 3em;
		padding-top: 0.5em;
		padding-bottom: 0.5em;
	}

	main {
		min-height: 100vh;
	}

	.overview {
		height: 60vh;
	}

	.role {
		color: #e6dcd5;
		font-size: 2em;
		padding: 2em;
	}

	.info-header {
		margin: 2em;
		border-bottom: 1px solid #e6dcd5;
	}

	.info-h2 {
		font-size: 2em;
		padding-bottom: 0.5em;
	}

	.info-container {
		display: flex;
		flex-wrap: wrap;
		margin: 1em;
	}

	@media only screen and (max-width: 850px) {
		.info-container {
			justify-content: center;
		}

		.role {
			font-size: 2em;
			padding: 1.5em;
		}
	}
</style>
