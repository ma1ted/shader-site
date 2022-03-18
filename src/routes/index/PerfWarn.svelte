<div id="warning">
	<h1>Mobile Device Detected</h1>
	<h2>Shaders will perform poorly</h2>
</div>

<style>
	#warning {
		top: 0;
		height: 5rem;
		width: 100%;
		margin: 0;
		background-color: var(--col-red);
	}
	@media (pointer:fine) {
		#warning {
			display: none;
		}
	}

	h1, h2 {
		margin: 0;
		text-align: center;
		color: black
	}

	h1 {
		font-size: 1.7rem;
	}
	h2 {
		font-size: 1.3rem;
		margin: 0.5rem;
	}
</style>