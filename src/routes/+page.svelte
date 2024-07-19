<script>
	let datas = [
		{
			image: "/images/3.png",
			text: "This application is designed to streamline your workforce management. Easily track attendance, manage annual leave requests, and handle reimbursement submissions all in one place.",
		},
		{
			image: "/images/2.png",
			text: "This application is designed to streamline store visit marketing, simplify the generation of monthly commission reports, and facilitate easy payslip downloads.",
		},

		{
			image: "/images/1.png",
			text: "This application is designed to help you efficiently manage your expenses, track your income, and generate detailed monthly reports.",
		},
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="text-column">
	<p
		style="font-family: Comic Sans MS cursive; font-size: 1.5em; text-align:center;"
	>
		I've successfully built and launched apps on both the Play Store and App
		Store. From brainstorming ideas to seeing them live, I love every step
		of the process. Let's team up and create something amazing together!
	</p>
</div>

<div class="data">
	{#each datas as data, i}
		<div class="content">
			<img src={data.image} alt="${i}" />
			<p style="font-family: Comic Sans MS cursive; text-align:center;">
				{data.text}
			</p>
		</div>
	{/each}
</div>

<style>
	.data {
		display: flex;
		flex-direction: row;
		gap: 20px;
		width: 100%;
		overflow: auto;
	}
	.content {
		display: flex;
		flex-direction: column;
		gap: 20px;
	}
	.content img {
		width: 700px;
		height: 350px;
	}
</style>
