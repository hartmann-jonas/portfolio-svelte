<script>
    import Icon from 'svelte-awesome' 
    import instagram from 'svelte-awesome/icons/instagram'
    import linkedin from 'svelte-awesome/icons/linkedin'
    import twitter from 'svelte-awesome/icons/twitter'
    import code from 'svelte-awesome/icons/code'
</script>

<svelte:head>
    <!--
    <meta name="theme-color" media="(prefers-color-scheme: light)" content="cyan" />
    <meta name="theme-color" media="(prefers-color-scheme: dark)" content="black" />
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
-->
<meta name="theme-color" content="#0802104e">

</svelte:head>

<nav>
    <p><a href="/"> JONAS HARTMANN</a></p>
    <div class="links">
        <p><a href="/about">ABOUT</a></p>
        <p><a href="/work">WORK</a></p>
        <p><a href="/">CONTACT</a></p>
    </div>
</nav>

<slot />

<footer>
    <div class="top">
        <p class="name">Jonas Hartmann</p>
        <p class="design">designed with love using svelte <Icon data={code} scale="0.5" class="icon"/></p>
    </div>
    <div class="bottom">
        <div class="contact">
            <p>+49 123 3414524</p>
            <p>contact@jonashartmann.live</p>
            <a href="mailto:contact@jonashartmann.live">Send me a mail</a>
        </div>
        <div class="address">
            <p>Musterstraße 123</p>
            <p>63165 Mühlheim</p>
        </div>
        <div class="socials">
            <p><a href="/"><Icon data={instagram} scale=0.75 style="padding-right: 5px"/> Instagram</a></p>
            <p><a href="/"><Icon data={linkedin} scale=0.75 style="padding-right: 5px"/> LinkedIn</a></p>
            <p><a href="/"><Icon data={twitter} scale=0.75 style="padding-right: 5px"/> Twitter</a></p>
        </div>
    </div>
</footer>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;800&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Reenie+Beanie&display=swap');
    
    /* general styles */
    a {
        color: white;
        text-decoration: none;
    }

    .links a:hover, footer a:hover {
        transition: 300ms;
        color: rgb(107, 107, 107);
    }

    /* styles for navbar when screen wider than 400px */
    @media (min-width: 420px) {
        nav {
            width: 100%;
            font-family: 'Playfair Display', serif;
            color: white;
            align-items: center;
            display: flex;
            justify-content: space-around;
            cursor: default;
        }
        
        nav p {
            font-size: 25px;
            font-weight: 800;
        }
        
        nav .links a {
            font-size: 16px;
            font-weight: 700;
        }
        
        .links {
            display: flex;
            gap: 3vh;
        }
    }

    /* styles for navbar for screens up to 400px width */
    @media (max-width: 420px) {
        nav {
            width: 100%;
            font-family: 'Playfair Display', serif;
            color: white;
            align-items: center;
            display: flex;
            justify-content: space-around;
            cursor: default;
        }
        
        nav p {
            font-size: 25px;
            font-weight: 800;
        }
        
        .links a, .links p{
            font-size: 13px;
            font-weight: 700;
            margin: 5px;
        }
    }
    
    /* styles for footer when screen wider than 800px */
    @media (min-width: 920px) {
        footer {
            width: 100%;
            font-family: 'Playfair Display', serif;
            font-size: 12px;
            color: white;
            /*background-color: rgb(25, 2, 57);*/
        }

        .top {
            display: flex;
            justify-content: center;
            gap: 10vmin;
            text-align: center;
        }

        .name {
            font-size: 16px;
        }

        .design {
            margin: auto 0;
            font-size: 11px;
        }

        .bottom {
            margin-top: 2vmin;
            margin-bottom: 2vmin;
            display: flex;
            flex-direction: row;
            justify-content: space-around;
        }

        .contact, .address, .socials {
            width: 10%;
        }

        .contact p, .address p, .socials p {
            height: 1vh
        }
    }

    /* styles for footer with screens up to 800px width */
    @media (max-width: 920px) {
        footer {
            padding-top: 10vmin;
            width: 100%;
            font-family: 'Playfair Display', serif;
            color: white;
            /*background-color: rgb(25, 2, 57);*/
        }

        .top {
            display: flex;
            justify-content: center;
            gap: 10vmin;
            text-align: center;
        }

        .name {
            font-size: 2vh;
        }

        .design {
            margin: auto 0;
            font-size: 1.5vh;
        }

        .bottom {
            margin: 2vmin;
            display: flex;
            flex-direction: row;
            justify-content: space-between;
        }

        .contact, .address, .socials {
            width: 25%;
            font-size: 1.2vh;
            text-align: center;
        }

        .contact p, .address p, .socials p {
            height: 1vh
        }
    }
</style>