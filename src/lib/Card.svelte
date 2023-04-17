<script>
    import Github from "./logo/Github.svelte";

    export let title = "";
    export let overview = "";
    export let details = "";
    export let link = "";
</script>

<div class="card">
    <div>
        <h3 class="text">{title}</h3>
        <p class="text">{overview}</p>
        <p class="text">{details}</p>
    </div>
    <a href={link}>
        <Github />
    </a>
</div>

<style>
    .card {
		width: 300px;
		min-height: 300px;
		border: 1px solid #e6dcd5;
		margin: 1em;
		padding: 16px;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
        font-size: 1.2em;
        box-shadow: 4px 4px 4px #000;
	}

    .text {
        padding-bottom: 16px;
    }
</style>
