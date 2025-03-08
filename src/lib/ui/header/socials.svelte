<script lang="ts">
	import { Facebook, X } from '$lib/icons'
	import * as config from '$lib/site/config'
</script>

<div class="socials">
	<a href={config.facebook} target="_blank" rel="noreferrer">
		<Facebook width={24} height={24} aria-label="Facebook" />
	</a>
	<a href={config.twitter} target="_blank" rel="noreferrer">
		<X width={24} height={24} aria-label="Twitter" />
	</a>
</div>

<style>
	.socials {
		display: none;

		@media (width >= 768px) {
			display: flex;
			align-items: center;
			gap: var(--spacing-16);
		}
	}
</style>
