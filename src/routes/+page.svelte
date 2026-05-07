<script>

    import Header from '$lib/header.svelte';

</script>

<Header />

<main class="w-full h-full z-10 relative">

    <div class="flex justify-center items-center">

        <div class="box overflow-auto bg-white/20 backdrop-blur-md shadow-blue fixed top-0 bottom-0 left-0 right-0 m-20 rounded-4xl flex justify-center">

            <div class="flex flex-col items-center">
                <img src="/images/icon.svg" alt="daikon-icon" class="w-40 h-40 m-10 drop-shadow-2xl border border-gray-400 drop-shadow-xl/80 bg-white rounded-full" />
                <img src="/images/da1k0n.svg" class="w-50 h-20"/>
                <p class="text-white text-xl text-center mt-4">Webアプリ・ゲームを主に触ってます。<br>将来はシステムエンジニアになりたい！</p>
            </div>  

        
        </div>

    </div>

</main>

<style>

    .box {
    scrollbar-width: none; /* Firefox */
    }

</style>