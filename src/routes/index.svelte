<script>
	import Warning from "./index/PerfWarn.svelte";
	import Title from "./index/title.svelte";
	import Footer from "./index/footer.svelte";

	// @ts-ignore
	import previewData from "/static/previews/previewData.json";
</script>

<svelte:head>
	<!-- Primary Meta Tags -->
	<title>Malted's Shaders</title>
	<meta name="title" content="Malted's Shaders">
	<meta name="description" content="Cool and epic shader gallery">

	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website">
	<meta property="og:url" content="https://metatags.io/">
	<meta property="og:title" content="Malted's Shaders">
	<meta property="og:description" content="Cool and epic shader gallery">
	<meta property="og:image" content="https://cdn.discordapp.com/attachments/811964301669695550/954480233862553640/wubble.png">

	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image">
	<meta property="twitter:url" content="https://metatags.io/">
	<meta property="twitter:title" content="Malted's Shaders">
	<meta property="twitter:description" content="Cool and epic shader gallery">
	<meta property="twitter:image" content="https://cdn.discordapp.com/attachments/811964301669695550/954480233862553640/wubble.png">

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