<script>
	let interested = [
		{
			name: "Johan Ronsse",
			twitter: "wolfr_2"
		},
		{
			name: "Sebastian De Deyne",
			twitter: "sebdedeyne"
		},
		{
			name: "Pieter De vriendt",
			twitter: "pieter_dv",
		},
		{
			name: "Jérôme Coupé",
			twitter: "jeromecoupe"
		},
		{
			name: "Dries De Roeck",
			twitter: "DriesDeRoeck"
		},
		{
			name: "Jan De Wilde",
			twitter: "Mr_Jean"
		},
		{
			name: "Olivier Van Biervliet",
			twitter: "Ovan"
		},
		{
			name: "Jeremy Swinnen",
			twitter: "Jereswinnen"
		}
	]

	import Box from './Box.svelte';
</script>

<style>
	/* overpass-regular - latin */
	@font-face {
	font-family: 'Overpass';
	font-style: normal;
	font-weight: 400;
	src: local('Overpass Regular'), local('Overpass-Regular'),
		url('./assets/fonts/overpass-v4-latin-regular.woff2') format('woff2'), /* Chrome 26+, Opera 23+, Firefox 39+ */
		url('./assets/fonts/overpass-v4-latin-regular.woff') format('woff'); /* Chrome 6+, Firefox 3.6+, IE 9+, Safari 5.1+ */
	}
	/* overpass-600 - latin */
	@font-face {
	font-family: 'Overpass';
	font-style: normal;
	font-weight: 600;
	src: local('Overpass SemiBold'), local('Overpass-SemiBold'),
		url('./assets/fonts/overpass-v4-latin-600.woff2') format('woff2'), /* Chrome 26+, Opera 23+, Firefox 39+ */
		url('./assets/fonts/overpass-v4-latin-600.woff') format('woff'); /* Chrome 6+, Firefox 3.6+, IE 9+, Safari 5.1+ */
	}

	:global(body) {
		line-height: 1.5;
		max-width: 70rem;
		margin: 0 auto;
		padding: 1.2rem;
		font-family: 'Overpass';
		color: #444444;
	}

	main {
		display: flex;
		justify-content: space-between;
		margin-top: 3.5rem;
	}
	.header__logo {
		margin: 2.5rem 0 2.25rem 0;
		max-width: 100%;
	}

	.divider {
		height: 1px;
		background: #C4C4C4;
		opacity: 0.5;
	}

	.footer__content {
		display: flex;
		justify-content: space-between;
		margin: 1.5rem 0;
		color: #444444;
	}
	.column {
		width: 48%;
	}
	.list {
		padding: 0;
		margin:0;
		border-radius: 3px;
		background: #F7FAFD;
		list-style: none;
		display: flex;
		flex-wrap: wrap;
	}

	.list__item {
		width: 50%;
	}

	.list__item p {
		margin: 1rem 0 .5rem 0;
	}

	.link {
		text-decoration: underline;
	}

	.link--blue {
		color: #63B1F9;
	}

	.link--grey {
		color: #444444;
		opacity: 0.5;
	}

	section {
		margin-bottom: 1.5rem;
	}

	@media only screen and (max-width: 960px) {
		main {
			flex-wrap: wrap;

		}

		.column {
			width: 100% !important;
		}
	}

	@media only screen and (max-width: 650px) {
		.footer__content {
			flex-direction: column;
		}
	}

</style>

<header class="header">
	<img class="header__logo" src="./assets/images/logo.svg" alt="Svelte camp logo">
	<div class="divider"></div>
</header>

<main>
	<div class="column">
		<section>
			<p>A Barcamp style event in Belgium.</p>
			<p>Let's learn about Svelte through some presentations and some coding together. (A bit like the Jekyll camp I organized quite some time ago)</p>
			<p>Location to be decided, but probably a classroom or shared office in Ghent or Antwerp. If you are a school or have a location and interested in hosting this event, get in touch!</p>
			<p>Timing to be decided, probably in the coming 2-3 months. Beginning of December seems realistic.</p>
		</section>

		<Box variant="blue">
			<h2>What is Svelte anyway?</h2>
			<p>Svelte is a new web app framework, comparable to Vue.js and React, but with key differences. Want to learn more about Svelte? Check the <a class="link link--blue" href="https://github.com/ryanatkn/awesome-svelte-resources">Svelte resources list</a>.</p>
		</Box>

		<Box variant="blue">
			<h2>What is an “unconference”?</h2>
			<p>A typical conference is usually expensive, and presented as a big deal. An unconference tries to deliver similar value but the rules are different.</p>
			<p>The value is created by the audience. At the beginning of the day, we will arrange speaker slots on a whiteboard.</p>
			<p>Inspired by <a class="link link--blue" href="http://barcamp.org/w/page/405173/TheRulesOfBarCamp">BarCamp</a>.</p>
		</Box>

	</div>

	<div class="column">
		<Box variant="orange">
			<h2>Call for speakers</h2>
			<p>Do you want to speak about Svelte or a related topic (i.e. front-end frameworks or modern Javascript tooling?). Let us know, so we are sure we at least have some speakers at the event!</p>
		</Box>

		<Box variant="blue">
			<h2>Interested</h2>
			<p>Want to get on the list? Tweet to <a class="link link--blue" href="https://twitter.com/wolfr_2">@wolfr_2</a>.</p>

			<div class="divider"></div>

			<ul class="list">
			{#each interested as interestedPerson}
				<li class="list__item">
					<p>{interestedPerson.name}</p>
					<a class="link link--grey" href="https://twitter.com/{interestedPerson.twitter}">@{interestedPerson.twitter}</a>
				</li>
			{/each}
			</ul>
		</Box>

	</div>

</main>

<footer>
	<div class="divider"></div>
	<div class="footer__content">
		<p>A <a class="link link--grey" href="https://mono.company">Mono</a> initiative.</p>
		<p>Want to organise a local meetup? <a class="link link--grey" href="https://github.com/monocompany/sveltecamp">Fork this repo.</a></p>
	</div>
</footer>
