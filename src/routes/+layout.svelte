<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/icon.png';
	
	let { children } = $props();

	let video: HTMLVideoElement;
	let timeoutId: ReturnType<typeof setTimeout>;

	const MauseMove = (event: MouseEvent) => {
        if (video) {
			// 動いた瞬間に速度を上げる
            video.playbackRate = 5; 

			// 前回の停止予約をリセットする
			clearTimeout(timeoutId);

			timeoutId = setTimeout(() => {
				while (video.playbackRate > 1) {
					video.playbackRate -= 1; // 徐々に速度を下げる
				}
			}, 200);
        }
    };

</script>

<svelte:window onmousemove={MauseMove} />

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}

<title>Who's da1k0n</title>

<main>

	<div class="relative h-screen w-screen overflow-hidden z-0">

		<video bind:this={video} autoplay muted loop src="./video/bg.mp4" class="flex items-center justify-center w-full h-full object-cover"></video>

	</div>

</main>