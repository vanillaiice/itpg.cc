<script>
	import 'beercss';
	import '../style.css'

	let themeDark = window.localStorage.getItem('theme') == 'dark' ? true : false;

	const setTheme = (theme) => {
		window.localStorage.setItem('theme', theme);
		document.body.className = theme;
	};

	const toggleTheme = () => {
		let current_theme = document.body.className;
		const theme = current_theme === 'light' ? 'dark' : 'light';
		themeDark = theme == 'dark' ? true : false;
		setTheme(theme);
	};
</script>

<header>
	<nav>
		<h5 class="max">itpg ?</h5>
		<a class="button circle transparent" href="https://github.com/vanillaiice/itpg" target="_blank">
			<i>
				<img src="/github.svg" alt="github" />
			</i>
		</a>
		<label class="switch icon">
			<input type="checkbox" checked={themeDark} on:change={toggleTheme} />
			<span>
				<i>dark_mode</i>
			</span>
		</label>
	</nav>
</header>

<main class="responsive">
	<article class="no-padding">
		<div class="grid no-space">
			<div class="s7">
				<img class="responsive" src="/itpg-logo.png" alt="itpg logo" />
			</div>
			<div class="s5">
				<div class="padding">
					<h5>Is This Professor Good ?</h5>
					<p>
						ITPG is a platform where students can grade their professors after taking courses. This
						allows students to make more informed decisions when choosing their courses.
					</p>
					<h6>Relevant Links:</h6>
					<article>
						<a class="row wave" href="https://demo.itpg.cc" target="_blank">
							<i>link</i>
							Demo website
						</a>
						<hr />
						<a class="row wave" href="https://github.com/vanillaiice/itpg" target="_blank">
							<i>link</i>
							Backend Source Code
						</a>
						<hr />
						<a class="row wave" href="https://github.com/vanillaiice/itpg-frontend" target="_blank">
							<i>link</i>
							Frontend Client Source Code
						</a>
						<hr />
						<a class="row wave" href="https://github.com/vanillaiice/itpg-seeder" target="_blank">
							<i>link</i>
							Go Package to Seed DB with fake data (useful for testing)
						</a>
						<hr />
						<a
							class="row wave"
							href="https://github.com/vanillaiice/itpg-docker-compose"
							target="_blank"
						>
							<i>link</i>
							Docker compose example
						</a>
						<hr />
					</article>
				</div>
			</div>
		</div>
	</article>

	<footer class="fixed center-align">
		<p class="no-margin">
			&copy; 2024 <a target="_blank" href="https://vanillaiice.xyz" class="link">vanilllaiice</a> ~ made
			with sveltekit &amp; beercss
		</p>
	</footer>
</main>
