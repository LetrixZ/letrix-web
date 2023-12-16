<script lang="ts">
	import '../app.postcss';

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });
</script>

<div class="flex flex-col h-screen">
	<slot />

	<div class="mt-auto mx-auto w-fit py-2">
		<p class="text-sm font-medium text-surface-600-300-token">
			<a
				class="border-surface-600-300-token"
				href="https://github.com/LetrixZ/letrix-web"
				target="_blank"
			>
				GitHub
			</a>
			|
			<span> v23.10.24-02 </span>
		</p>
	</div>
</div>

<style lang="postcss">
	a {
		@apply border-b hover:border-surface-700-200-token hover:text-surface-900-50-token active:border-primary-400-500-token active:text-primary-400-500-token transition duration-75;
	}
</style>
