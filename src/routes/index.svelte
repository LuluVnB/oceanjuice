<script>
    // @ts-ignore
    import TypedJs from '@loscrackitos/svelte-typed-js';
import LoadingScreen from '../lib/LoadingScreen.svelte';
</script>

<!-- <LoadingScreen /> -->

<header>
    <video autoplay loop muted>
        <source src="/video.mp4" autoplay loop type="video/mp4">
        Your browser does not support the video tag
    </video>
    <h1>Our mission is: <TypedJs strings={['Saving Ocean Animals', 'Drinking Ocean Water', "Attacking Ocean Wildlife", 
'Killing Turtles']} loop>
        <span class='typing'></span>
    </TypedJs></h1>
</header>
<section class="information">
    <div class="airgun"><h2>Airgun</h2><h3>225 dB</h3><p>An airgun in the water is comparable to a human standing next to a rocket engine when it's launching.</p></div>
    <div class="propeller"><h2>Propeller</h2><h3>180 dB</h3><p>It is comparable to standing next to a 12 gauge shotgun blast</p></div>
    <div class="animal"><h2>Sea Creature Info</h2><p>Noise is amplified in the ocean because sound travels faster in the water. Because of this, sea creatures are fatally affected by noise. Noises as simple as a propeller from a ship to a whale is like firing a 12 gauged shot gun next to a human's ear. Noise pollution disrupts creatures lives as they rely on sonar and echolocation to communicate. Various noises caused by humans have caused many of these species, to get lost, leading to ocean activity decrease every day. Some creatures, such as whales, are detrimentally affected because hearing loss can lead to massive amounts of damage and even death.</p></div>
</section>

<style>
    header {
        position: relative;
        display: flex;
        /* justify-content: center; */
        align-items: center;        
    }

    video {
        max-height: 80vh;
        object-fit: cover;
    }

    h1 {
        position: absolute;   
        /* top: 50%;
        margin-top: -50%; */
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
    }

    .information > div {
        width: 100%;
        text-align: center;
        padding: 64px 32px;
        box-sizing: border-box;
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
        
        color: white;
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
        background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://media.discordapp.net/attachments/973416247935004682/977994134776344576/IMG_8431.jpg');   
    }

    .propeller {
        grid-area: propeller;
        background-color: green;
        background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://media.discordapp.net/attachments/973416247935004682/978013798193578014/unknown.png');   
    }

    .animal {
        grid-area: animal;
        background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('https://media.discordapp.net/attachments/973416247935004682/978013532350201867/unknown.png?width=721&height=405');   
    }

    @media (min-width: 640px) {
        video {
            width: 100%;
            height: 100%;
            aspect-ratio: 16 / 9;
        }
        .information {
            display: grid;
            justify-items: center;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: auto auto;
            grid-template-areas: 'airgun propeller' 'animal animal';
        }
    }
</style>