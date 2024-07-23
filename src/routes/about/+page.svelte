<script>
	let data = {
		about: "I'm a passionate Mobile Developer driven by creating user-friendly and high-performing mobile applications. My expertise lies in the Flutter framework for building engaging mobile experiences. I'm also expanding my skillset towards backend development, currently working as a junior with Go lang for API development and Postgres for database management.",
		skills: ["Flutter", "Firebase", "Supabase", "Go", "Postgres"],
	};
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="text-column">
	<h3 style="text-align:center;">About me</h3>

	<p
		style="font-family: Comic Sans MS cursive; font-size: 1.2em; text-align:center;"
	>
		{data.about}
	</p>
	<h3 style="text-align:center;">Skill</h3>
	<div class="row">
		{#each data.skills as t}
			<div
				class="chip"
				style="font-family: Comic Sans MS cursive; font-size: 1.1em; text-align:center; color:yellow"
			>
				{t}
			</div>
		{/each}
	</div>
</div>

<style>
	.chip {
		display: inline-block;
		padding: 0 25px;
		height: 40px;
		margin-left: 15px;
		margin-bottom: 10px;
		font-size: 16px;
		line-height: 40px;
		border-radius: 20px;
		background-color: #2f467a;
	}
</style>
