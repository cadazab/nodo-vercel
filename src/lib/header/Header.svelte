<script lang="ts">
	import { page } from '$app/stores';
	
	let hue = 0
	setInterval(() => {
		hue ++
  }, 100);
</script>

<header class="mb-10">	
	<div style="background-color:hsl({hue}, 100%, 50%)" class=" w-full h-60 flex justify-center">
		<h1 class="text-6xl font-extrabold mt-28">NODO</h1>
	</div>

	<nav>
		<ul class="flex justify-around">
			<li class:active={$page.url.pathname === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.url.pathname === '/about'}>
				<a sveltekit:prefetch href="/about">About</a>
			</li>
			<li class:active={$page.url.pathname === '/todos'}>
				<a sveltekit:prefetch href="/todos">Todos</a>
			</li>
		</ul>
	</nav>

</header>

<style lang="postcss">
	li {
		@apply transition ease-in-out duration-300 hover:scale-105 hover:text-blue-600
	}
	.active{
		@apply border-b-2 border-indigo-500
	}
</style>
