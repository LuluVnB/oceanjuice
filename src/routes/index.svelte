<script>
    // @ts-ignore
    import TypedJs from '@loscrackitos/svelte-typed-js';
</script>

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
</style>