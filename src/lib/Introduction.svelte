<script>
	import pfp from '$lib/assets/jtriley.png';
</script>

<section class="intro">
	<header class="about">
		<h1 class="name">jtriley.eth</h1>
		<h2 class="title">Smart Contract Engineer</h2>
	</header>
	<img alt="AI Generateed PFP" src={pfp} class="pfp" />
</section>

<style>
	.intro {
		display: flex;
		/* flex-direction: row-reverse; */
		align-items: center;
		justify-content: space-evenly;
		flex-wrap: wrap;
		padding: 32px;
	}

	.about {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.name {
		font-size: 2.5em;
		font-weight: 700;
		padding: 32px;
	}

	.title {
		font-size: 1.5em;
		padding: 32px;
		padding-top: 0;
	}

	.pfp {
		width: 50%;
		min-width: 300px;
		border-radius: 10%;
		box-shadow: 4px 4px 4px #000;
	}

	@media (min-width: 512px) {
		.name {
			font-size: 5em;
		}

		.title {
			font-size: 2em;
		}
	}
</style>
