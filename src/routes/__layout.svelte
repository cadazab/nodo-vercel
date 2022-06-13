<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main class="p-10">
	<slot />
</main>

<footer class=" text-gray-400 text-center absolute bottom-10 w-full">
	<p>derechos registrados NODO</p>
</footer>

