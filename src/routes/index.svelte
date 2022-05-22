<script>
    // @ts-ignore
    import TypedJs from '@loscrackitos/svelte-typed-js';
import LoadingScreen from '../lib/LoadingScreen.svelte';
</script>

<LoadingScreen />
<nav>
    <img src="/tritonhacks-logo.webp" alt="">
    <div>
        <a href="/">Information</a>
        <a href="/">Visualizations</a>
    </div>
</nav>
<header>
    <video autoplay loop>
        <source src="/video.mp4" autoplay type="video/mp4">
        Your browser does not support the video tag
    </video>
    <TypedJs strings={['Saving Ocean Animals', 'Drinking Ocean Water', "Attacking Ocean Wildlife", 
'Killing Turtles']} loop>
        <h1>Our mission is: <span class='typing'></span></h1>
    </TypedJs>
</header>
<section class="information">
    <div class="airgun"><h2>Airgun</h2><h3>225 dB</h3><p>An airgun in the water is comparable to a human standing next to a rocket engine when it's launching.</p></div>
    <div class="sonar"><h2>Propeller</h2><h3>180 dB</h3><p>It is comparable to standing next to a 12 gauge shotgun blast</p></div>
    <div class="animal"><h2>Sea Creature Info</h2><p>Noise is amplified in the ocean because sound travels faster in the water. Because of this, sea creatures are fatally affected by noise. Noises as simple as a propeller from a ship to a whale is like firing a 12 gauged shot gun next to a human's ear. Noise pollution disrupts creatures lives as they rely on sonar and echolocation to communicate. Various noises caused by humans have caused many of these species, to get lost, leading to ocean activity decrease every day. Some creatures, such as whales, are detrimentally affected because hearing loss can lead to massive amounts of damage and even death.</p></div>
</section>

<style>
    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 24px 24px;
        background-color: rgb(29, 29, 29);
    }
    
    nav img {
        width: 48px;
    }

    nav > div {
        display: flex;
        justify-content: center;
        gap: 16px;
    }

    nav a {
        text-decoration: none;
        color: white;
    }

    header {
        position: relative;
        display: flex;
        /* justify-content: center; */
        align-items: center;
        
    }

    video {
        width: 100%;
        height: 100%;
        aspect-ratio: 16 / 9;
    }

    h1 {
        position: absolute;   
        left: 24px;
        font-size: 48px;
        color: white;
    }

    .typing {
        font-size: 48px;
        color: white;
    }

    .information {
        width: 100%;

        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: auto auto;
        grid-template-areas: 'airgun sonar' 'animal animal';
        justify-items: center;
    }

    .information > div {
        width: 100%;
        text-align: center;
        padding: 64px 32px;
        box-sizing: border-box;
    }

    .information h2 {
        font-size: 36px;
    }

    .information h3 {
        margin-top: 16px;
        font-size: 24px;
    }

    .information p {
        margin-top: 8px;
    }

    .airgun {
        grid-area: airgun;
        background-color: pink;
    }

    .sonar {
        grid-area: sonar;
        background-color: green;
    }

    .animal {
        grid-area: animal;
        background-color: blue;
    }
</style>