<script>
	import Header from "./Header.svelte";
	import "../app.css";
	import github from "$lib/images/github.svg";
	import linkedin from "$lib/images/in.svg";
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>

	<footer>
		<p>Connect with me</p>
		<div class="corner">
			<a href="https://github.com/msarifin29">
				<img src={github} alt="GitHub" />
			</a>
		</div>
		<div class="corner">
			<a href="https://www.linkedin.com/in/muhammad-syamsul-arifin/">
				<img src={linkedin} alt="Linked In" />
			</a>
		</div>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
		overflow: auto;
	}

	footer {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}
	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
