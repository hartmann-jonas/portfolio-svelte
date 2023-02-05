<nav>
    <p><a href="/"> Jonas Hartmann</a></p>
    <div class="links">
        <p><a href="/about">about</a></p>
        <p><a href="/">work</a></p>
        <p><a href="/">contact</a></p>
    </div>
</nav>

<slot />

<footer>
    <div class="top">
        <p class="name">Jonas Hartmann</p>
        <p class="design">designed with love using svelte</p>
    </div>
    <div class="bottom">
        <div class="contact">
            <p>+49 123 3414524</p>
            <p>contact@jonashartmann.com</p>
        </div>
        <div class="address">
            <p>Musterstraße 123</p>
            <p>63165 Mühlheim</p>
        </div>
        <div class="socials">
            <p><a href="/">Instagram</a></p>
            <p><a href="/">LinkedIn</a></p>
            <p><a href="/">Twitter</a></p>
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

    .links a:hover {
        transition: 300ms;
        color: rgb(107, 107, 107);
    }

    /* styles for navbar when screen wider than 400px */
    @media (min-width: 400px) {
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
    @media (max-width: 400px) {
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