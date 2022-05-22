<script lang='ts'>
    import { io } from "socket.io-client";
    import { onMount } from "svelte";
    
    const socket = io('http://localhost:5000/')

    let dB = 0;
    let image: HTMLImageElement;

    onMount(() => {
        if (typeof window !== 'undefined')
            socket.on("dB", (arg) => {
                if (arg > 45) {
                    image.classList.add('rotate')
                } else {
                    image.classList.remove('rotate')
                }
            });
        }
    )

   
</script>

<img class="rotate" bind:this={image} src="/turtle.png" alt="">