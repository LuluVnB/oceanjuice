<script lang='ts'>
    import { io } from "socket.io-client";
    import { onMount } from "svelte";
    
    const socket = io('https://4006-69-196-32-69.ngrok.io/')

    let dB = 0;
    let image: HTMLImageElement;

    onMount(() => {
        if (typeof window !== 'undefined')
            socket.on("dB", (arg) => {
                if (arg > 48) {
                    image.classList.add('rotate')
                } else {
                    image.classList.remove('rotate')
                }
            });
        }
    )
</script>

<section>
    <img class="turtle" bind:this={image} src="/turtle.png" alt="">
</section>

<style>
    section {
        background-image: url(/background.png);
        background-size: 100% 100%;
        height: 100vh;
        position: relative;
        overflow: hidden;
        display: flex;
        justify-content: center;
    }

    .turtle {
        position: absolute;
        bottom: 7.5%;
        width: 50%;
        max-width: 300px;
    }
</style>