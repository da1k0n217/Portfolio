<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/icon.png';
	
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}

<title>Who's da1k0n</title>

<main>

	<div class="h-screen w-screen overflow-hidden z-0">

		<video autoplay muted loop src="./video/bg.mp4"></video>

	</div>

</main>