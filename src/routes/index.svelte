<script>
	import Warning from "./index/PerfWarn.svelte";
	import Title from "./index/title.svelte";
	import Footer from "./index/footer.svelte";

	// @ts-ignore
	import previewData from "/static/previews/previewData.json";
</script>

<svelte:head>
	<title>Malted's Shaders</title>
	<meta name="viewport" content="width=device-width, initial-scale = 0.86, maximum-scale=3.0, minimum-scale=0.86">
</svelte:head>

<Warning />

<Title />

<div id="previews-parent">
	{#each previewData as preview, idx}
		<a href="{preview.nameShort}">
			<div class="preview-panel">
				<img src="{preview.src}" alt="{preview.name} shader preview" />
				<h3>{preview.name}</h3>
				<h4>#{String(idx + 1).padStart(3, '0')}</h4>
			</div>
		</a>
	{/each}
</div>

<Footer />

<style>
	#previews-parent {
		display: grid;
		grid-template-columns: 1fr 1fr;
		row-gap: 5rem;
		margin-bottom: 10rem;
	}
  	@media (max-width: 600px) {
		#previews-parent {
			grid-template-columns: 1fr;
		}
	}
	@media (min-width: 1800px) {
		#previews-parent {
			grid-template-columns: 1fr 1fr 1fr;
		}
	}

	.preview-panel {
		text-align: center;
		height: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.preview-panel > img {
		width: 15rem;
		flex-grow: 1;
		object-fit: contain;
	}

	h3 {
		font-size: 2.5rem;
		font-style: italic;
		margin: 0;
	}

	h4 {
		font-size: 2rem;
		font-weight: 100;
		margin: 0;
	}
</style>