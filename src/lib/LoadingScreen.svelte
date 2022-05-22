<script lang='ts'>
import { onMount } from 'svelte';

    import { fade } from 'svelte/transition';

    let visible = true;
    onMount(() => {
        setTimeout(() => {
            visible = false
        }, 2000)
    })
</script>

{#if visible}
    <div in:fade={{duration: 3000, delay: 1000}} out:fade={{delay: 5000, duration: 1000}}>
        <p>Imagine going through every second of your day hearing noises as loud as a rocket engine next to your ear. This is what ocean creatures go through.</p>
    </div>
{/if}

<style>
    div {
        position: fixed;
        background-color: rgba(0, 0, 0, 1);
        width: 100%;
        height: 100%;
        z-index: 99;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        text-align: center;
        font-size: 30px;
        top: 0;
    }

    p {
        max-width: 80%;
        font-style: italic;
    }
</style>