<script>
	let yes = true;
	import playstore from "$lib/images/play_store.svg";
	import apptore from "$lib/images/app_store.svg";
	let datas = [
		{
			image: "/images/j_life.jpg",
			text: "This application is designed to streamline your workforce management. Easily track attendance, manage annual leave requests, and handle reimbursement submissions all in one place.",

			frontend: {
				name: "Flutter",
				pkg: [
					"Face Detection",
					"Flutter Bloc",
					"Local Storage",
					"Depenjensi Injection",
					"Camera",
					"Geolocation",
					"Rest API",
				],
			},
			backend: { name: null, db: null, pkg: [] },

			playstore:
				"https://play.google.com/store/search?q=jobseeker%20life&c=apps&hl=id",
			appstore:
				"https://apps.apple.com/id/app/jobseeker-life/id6466165581",
		},
		{
			image: "/images/rsm.jpg",
			text: "This application is designed to streamline store visit marketing, simplify the generation of monthly commission reports, and facilitate easy payslip downloads.",
			frontend: {
				name: "Flutter",
				pkg: [
					"Flutter Bloc",
					"Local Storage",
					"Depenjensi Injection",
					"Camera",
					"Stamp Location",
					"Rest API",
					"Download PDF",
				],
			},
			backend: { name: null, db: null, pkg: [] },
			playstore:
				"https://play.google.com/store/apps/details?id=com.rsm.randu_sales_mobile&hl=id",
			appstore: null,
		},

		// {
		// 	image: "/images/1.png",
		// 	text: "This application is designed to help you efficiently manage your expenses, track your income, and generate detailed monthly reports.",
		// 	frontend: {
		// 		name: "Flutter",
		// 		pkg: [
		// 			"Flutter Bloc",
		// 			"Local Storage",
		// 			"Depenjensi Injection",
		// 			"Camera",
		// 			"Geolocation",
		// 			"Rest API",
		// 		],
		// 	},
		// 	backend: {
		// 		name: "Go",
		// 		db: "Postgres",
		// 		pkg: ["Authentication JWT Token", "Pagination", "SMTP Email"],
		// 	},
		// },
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="text-column">
	<p
		style="font-family: Comic Sans MS cursive; font-size: 1.8em; text-align:center;"
	>
		Let's team up and create something amazing together!
	</p>
</div>

<div class="data">
	{#each datas as data, i}
		<div class="content">
			<img src={data.image} alt="${i}" />
			<p
				style="font-family: Comic Sans MS cursive;font-size: 1.2em; text-align:center;"
			>
				{data.text}
			</p>

			<div
				style="display:flex; flex-direction:column; justify-content: space-between;"
			>
				<div
					style="display: flex; flex-direction:row; align-items:center; width:100%;  justify-content:center; gap:50px;"
				>
					<a href={data.playstore}>
						<img
							src={playstore}
							alt="Play Store"
							style="width: 100%; height:200px;"
						/>
					</a>

					{#if data.appstore != null}
						<a href={data.appstore}>
							<img
								src={apptore}
								alt="App Store"
								style="width: 100%; height:200px;"
							/>
						</a>
					{/if}
				</div>

				<div>
					<p
						style="font-family: Comic Sans MS cursive;  font-weight: 700; font-size: 1.4em; text-align:center;"
					>
						{data.frontend.name}
					</p>
					{#each data.frontend.pkg as t}
						<div
							class="chip"
							style="font-family: Comic Sans MS cursive; font-size: 1.1em; text-align:center; color: yellow;"
						>
							{t}
						</div>
					{/each}
				</div>
				<div>
					<p
						style="font-family: Comic Sans MS cursive; font-weight: 700; font-size: 1.4em; text-align:center;"
					>
						{#if data.backend?.name != null}
							{data.backend?.name}
						{/if}
					</p>
					{#each data.backend.pkg as t}
						<div
							class="chip"
							style="font-family: Comic Sans MS cursive; font-size: 1.1em; text-align:center;"
						>
							{t}
						</div>
					{/each}
					<p
						style="font-family: Comic Sans MS cursive; font-weight: 700; font-size: 1.4em; text-align:center;"
					>
						{#if data.backend?.db != null}
							{data.backend?.db}
						{/if}
					</p>
				</div>
			</div>
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
