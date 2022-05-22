<nav>
    <a href="https://tritonhacks.org"><img src="/tritonhacks-logo.webp" alt=""></a>
    <div>
        <a href="/">Information</a>
        <a href="/visualizations">Visualizations</a>
    </div>
</nav>
<slot />

<style>
    nav {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 24px;
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

    @media (min-width: 640px) {
        nav {
            flex-direction: row;
            justify-content: space-between;
            align-items: center;
        }
    }
</style>