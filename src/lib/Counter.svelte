<script lang="ts">
	

	let count = 0;

	
</script>

<div class="flex justify-center">
	<button on:click={() => (count -= 1)} aria-label="Decrease the counter by one">-</button>
	<div class="counter-viewport">
		<div>
			<!-- <strong class="hidden" aria-hidden="true">{Math.floor($displayed_count + 1)}</strong> -->
			<h1 class="my-5 text-5xl">{count}</h1>
		</div>
	</div>

	<button on:click={() => (count += 1)} aria-label="Increase the counter by one">
		+
	</button>
</div>


<style lang="postcss">
	button {
		@apply text-5xl mx-10 font-bold
	}
</style>