<script>
	let interested = [
		{
			name: "Johan Ronsse",
			twitter: "wolfr_2",
			location: "Antwerp"
		},
		{
			name: "Sebastian De Deyne",
			twitter: "sebdedeyne",
			location: "Ghent"
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
		}
	]
</script>

<style>
	:global(body) {
		line-height: 1.5;
		max-width: 60rem;
		margin: 0 auto;
		padding: 1.2rem;
	}
</style>

<h1>Svelte Camp BE🇧🇪</h1>

<p>
	A Barcamp style event in Belgium.
</p>
<p>
	Let's learn about Svelte through some presentations and some coding together. (A bit like the Jekyll camp I organized quite some time ago)
</p>
<p>
	Location to be decided, but probably a classroom or shared office in Ghent or Antwerp. If you are a school or have a location and interested in hosting this event, get in touch!</p>
<p>
	Timing to be decided, probably in the coming 2-3 months. Beginning of December seems realistic.
</p>

<h2>
	Interested:
</h2>

<ul>
{#each interested as interestedPerson}
	<li>
		{interestedPerson.name},
		<a href="https://twitter.com/{interestedPerson.twitter}">@{interestedPerson.twitter}</a>
		{#if interestedPerson.location}, {interestedPerson.location}{/if}
	</li>
{/each}
</ul>

<p>Want to get on the list? Tweet to <a href="https://twitter.com/wolfr_2">@wolfr_2</a>.</p>
