<svelte:head>
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com">
	<link href="https://fonts.googleapis.com/css2?family=Roboto+Mono:wght@100;400&display=swap" rel="stylesheet">
</svelte:head>

<slot></slot>

<style>
	:root {
		--col-red: #ff595e;
		--col-bg: #1a2123;
		--col-grey: #c4c0c4;
		--col-green: #5b9279;
		--col-yellow: #e6c229;
		--col-blue: #1a8fe3;

		font-family: "Roboto Mono", monospace;

		overflow-x: hidden;
	}

	:global(*) {
		text-decoration: none;
		color: black;
	}

	:global(body) {
		margin: 0;
	}

	.no-scroll-horiz {
		overflow-x: hidden;
	}
	.no-scroll {
		overflow: hidden;
	}
</style>