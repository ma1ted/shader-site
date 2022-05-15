<slot></slot>

<style>
	@font-face {
		font-family: "JetBrains Mono";
		src: url("/fonts/JetBrainsMono-Regular.woff2") format("woff2");
		font-weight: 400;
		font-style: normal;
	}
	@font-face {
		font-family: "JetBrains Mono";
		src: url("/fonts/JetBrainsMono-Thin.woff2") format("woff2");
		font-weight: 100;
		font-style: normal;
	}

	:root {
		--col-red: #ff595e;
		--col-bg: #1a2123;
		--col-grey: #c4c0c4;
		--col-green: #5b9279;
		--col-yellow: #e6c229;
		--col-blue: #1a8fe3;

		font-family: "JetBrains Mono", monospace;
		font-weight: 400;

		background-color: #292e29;
	}

	:global(*) {
		text-decoration: none;
		color: white;
	}

	:global(body) {
		margin: 0;
		width: 100%;
		overflow-x: hidden;
	}
</style>
