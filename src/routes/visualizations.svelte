<script lang='ts'>
    import { io } from "socket.io-client";
    import { onMount } from "svelte";
    
    const socket = io('http://localhost:5000/')

    let dB = 0;
    let image: HTMLImageElement;

    onMount(() => {
        if (typeof window !== 'undefined')
            socket.on("dB", (arg) => {
                if (arg > 48) {
                    image.classList.add('rotate')
                    image.src = '/turtle.png'
                } else {
                    image.classList.remove('rotate')
                    image.src = '/happy turtle.png'
                }
            });
        }
    )
</script>

<section>
    <h2>The turtle shakes if the sound input is at a harmful level.</h2>
    <img class="turtle" bind:this={image} src="/happy turtle.png" alt="">
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
        align-items: center;
        color: white;
        font-size: 36px;
        text-align: center;
    }

    .turtle {
        position: absolute;
        bottom: 7.5%;
        width: 50%;
        max-width: 300px;
    }
</style>