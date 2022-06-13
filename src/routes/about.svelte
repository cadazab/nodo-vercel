<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="content">
	Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec sit amet pulvinar nunc. Duis egestas at lorem nec varius. Ut ut tempor ante. Morbi aliquam mi nibh. Morbi commodo ornare ornare. Pellentesque lobortis ex et nisi commodo, ac vestibulum lectus convallis. Suspendisse imperdiet leo leo, at eleifend nisl vehicula sit amet.

Integer vitae dui est. Fusce ac justo ex. Nam scelerisque auctor malesuada. Donec ultricies ipsum vitae massa vulputate porta. Nullam ultricies urna tortor, et lacinia nunc aliquet non. Donec congue, justo quis maximus convallis, enim justo mollis leo, non pretium nibh orci sit amet sapien. Fusce laoreet, augue nec convallis efficitur, ex ipsum lacinia nisl, sed aliquam sem purus et tellus. Vivamus aliquam arcu efficitur felis lacinia suscipit. Duis nec nunc id arcu maximus vestibulum a ac nunc. Nam vel semper ante. Maecenas hendrerit non sem non pharetra.

Donec bibendum tristique sodales. Cras convallis lacinia scelerisque. Nullam sit amet varius metus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Pellentesque vestibulum eu enim eget rhoncus. Nullam molestie augue leo, a iaculis eros tristique et. Aliquam porttitor, ipsum ut laoreet gravida, risus elit eleifend leo, eu accumsan dolor tellus et magna. Fusce scelerisque pharetra purus vitae placerat. Vestibulum luctus varius orci, a fermentum tellus convallis in. In in viverra ligula, sit amet rutrum ipsum. Aenean orci ante, blandit at urna vel, hendrerit auctor neque. Duis et mauris pretium purus pellentesque lacinia.

</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
