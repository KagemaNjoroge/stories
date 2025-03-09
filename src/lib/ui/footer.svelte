<script lang="ts">
	import {  GitHub, Mail, RSS } from '$lib/icons'
	import * as config from '$lib/site/config'
</script>

<div class="footer">
	<footer>
		<div class="categories">
			<p>Categories</p>
			<ul>
				{#each Object.entries(config.categories) as [slug, category]}
					<li>
						<a href="/categories/{slug}">{category}</a>
					</li>
				{/each}
			</ul>
		</div>

		<div class="follow">
			<p>Follow</p>
			<ul>
				<li>
					<a href="/newsletter">
						<Mail width={20} height={20} aria-hidden={true} />
						<span>Newsletter</span>
					</a>
				</li>
				<li>
					<a href="/rss.xml" target="_blank">
						<RSS width={20} height={20} aria-hidden={true} />
						<span>RSS</span>
					</a>
				</li>

				<!-- Facebook -->
				<li>
					<a href={config.github} target="_blank" rel="noreferrer">
						<GitHub width={20} height={20} aria-hidden={true} />
						<span>GitHub</span>
					</a>
				</li>
			</ul>
		</div>

		<div class="other">
			<p>Other</p>
			<ul>
				<li><a href="/about">Shop</a></li>
				<li><a href="/about">About</a></li>
			</ul>
		</div>
	</footer>

	<div class="name">
		Brought to you by the good folks at <a
			href="https://tomorrow.co.ke"
			referrerpolicy="no-referrer">TomorrowAI</a
		>
	</div>
</div>

<style>
	.footer {
		background-color: var(--clr-footer-bg);
		border-top: 1px solid var(--clr-menu-border);
		border-left: 1px solid var(--clr-menu-border);
		border-radius: var(--rounded-20) var(--rounded-20) 0px 0px;
		padding: var(--spacing-32);
	}
	.name {
		text-align: end;
		font-size: x-small;
	}
	footer {
		display: flex;

		gap: var(--gap);
		/* margin-block-start: var(--spacing-64); */

		flex-direction: column;
		--gap: var(--spacing-64);

		@media (width >= 600px) {
			--gap: var(--spacing-128);
			flex-direction: row;
		}

		p {
			font-weight: 700;
		}

		ul {
			width: max-content;
			display: grid;
			grid-template-rows: repeat(5, 1fr);
			grid-auto-flow: column;
			column-gap: var(--spacing-32);
			row-gap: var(--spacing-16);
			margin-top: var(--spacing-16);

			li a {
				display: flex;
				align-items: center;
				gap: var(--spacing-8);
			}
		}

		li a {
			font-weight: inherit;
			color: var(--clr-footer-txt);

			&:hover {
				color: var(--clr-primary);
			}
		}
	}
</style>
