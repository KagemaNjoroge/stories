<script lang="ts">
	import Heading from '$lib/ui/heading.svelte'
</script>

<svelte:head>
	<title>About</title>
</svelte:head>

<Heading>About</Heading>

<main>
	<p>Hey! 👋</p>
	<p>
		I'm <b>Kagema Njoroge</b>- A Storyteller, Software Developer, and Humorist. 
		I'm mostly passionate about ☕
		<b>African Literature,</b>
		🎨
		<b>Software Development, </b> and 🎨
		<b>IT laws</b>
	</p>
	<h2 class="text-white add-letter-space my-5">
		My Mission: Telling Stories That Matter
	</h2>
	<ul class="list-unstyled">
		<li class="bullet-list-item mb-4">
			<h3 class="text-white mb-3 add-letter-space">
				Writing Stories That Resonate
			</h3>
			<p>
				I create stories that entertain, educate, and spark conversations.
				Whether it’s a humorous village chronicle, a deep book review, or a
				social commentary, my goal is to keep readers engaged and inspired.
			</p>
		</li>
		<li class="bullet-list-item mb-4">
			<h3 class="text-white mb-3 add-letter-space">
				Bridging Literature and Technology
			</h3>
			<p>
				With my background in Computer Science, I am exploring the intersection
				of technology and storytelling. Digital platforms are the new libraries,
				and I aim to build tools that amplify African storytelling.
			</p>
		</li>
		<li class="bullet-list-item mb-4">
			<h3 class="text-white mb-3 add-letter-space">
				Building a Community of Readers and Writers
			</h3>
			<p>
				I believe in the power of storytelling to unite people. Through my
				website and social platforms, I aim to foster a vibrant community that
				appreciates and contributes to African literature.
			</p>
		</li>
	</ul>
</main>

<style>
	main {
		max-width: 60ch;
		margin-inline: auto;
		display: grid;
		row-gap: var(--spacing-32);
		margin-bottom: var(--spacing-64);
	}
</style>
