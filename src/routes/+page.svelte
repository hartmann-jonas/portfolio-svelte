<script>
    let cardStatus = "unloaded"
    function pushCards() {
        new Promise(r => setTimeout(r, 2000));
        cardStatus = "loaded";
    }
    setTimeout(pushCards, 250)
</script>

<body>
    <div class="cards">
        <div class="card" data-status={cardStatus} style="background-image: url(images/aditya-chinchure-ZhQCZjr9fHo-unsplash.jpg);">
            <p>lollapalooza - berlin 2022</p>
        </div>
        <div class="card" data-status={cardStatus} style="background-image: url(images/spencer-davis-naFHFLV5cqU-unsplash.jpg);">
            <p>lorem ipsum - europe tour 2021</p>
        </div>
        <div class="card" data-status={cardStatus} style="background-image: url(images/nainoa-shizuru-NcdG9mK3PBY-unsplash.jpg);">
            <p>massa tincidunt - world tour 2022</p>
        </div>
        <div class="card" data-status={cardStatus} style="background-image: url(images/muneeb-syed-4_M8uIfPEZw-unsplash.jpg);">
            <p>bell - quebec 2020</p>
        </div>
        <div class="card" data-status={cardStatus} style="background-image: url(images/colin-lloyd-RpK45xkkJ9o-unsplash.jpg);">
            <p>electra - tour 2023</p>
        </div>
    </div>
</body>
    
<style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;800&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Reenie+Beanie&display=swap');

    /* css for screens wider than 800px */
    @media (min-width: 800px) {
        body {
            margin: 0;
            /*background-image: linear-gradient(rgb(8, 2, 16), rgb(25, 2, 57));*/
            background-color: rgb(8, 2, 16);
            height: 100vh;
            width: 100%;
            display: grid;
            place-items: center;
        }

        .cards, .card {
            width: 50vmin;
        }

        .card {
            transition: 750ms ease-in;
            position: absolute;
            color: white;
            font-family: 'Reenie Beanie', cursive;
            font-size: 25px;
            font-weight: 400;
            box-shadow: 0px 0px 30px rgb(8, 2, 16);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            text-align: end;
        }

        .card p {
            margin: 10px;
            transform: translateY(40px)
        }

        .card:hover {
            transition: 200ms ease-in-out;
            width: 50.5vmin;
            z-index: 100;
        }

        .card:nth-child(1) {
            /*background-image: url(images/aditya-chinchure-ZhQCZjr9fHo-unsplash.jpg);*/
            aspect-ratio: 3909 / 2932;
            background-size: contain;
            transform: translate(-90%, -120%) rotate(2deg);
        }

        .card:nth-child(2) {
            /*background-image: url(images/spencer-davis-naFHFLV5cqU-unsplash.jpg);*/
            background-size: contain;
            aspect-ratio: 6299 / 4199;
            transform: translate(-80%, -4%) rotate(-3deg);
        }

        .card:nth-child(3) {
            /*background-image: url(images/nainoa-shizuru-NcdG9mK3PBY-unsplash.jpg);*/
            background-size: contain;
            aspect-ratio: 5184 / 3456;
            transform: translate(70%, -140%) rotate(-2deg);
            z-index: 2;
        }

        .card:nth-child(4) {
            /*background-image: url(images/muneeb-syed-4_M8uIfPEZw-unsplash.jpg);*/
            background-size: cover;
            width: 35vmin;
            aspect-ratio: 2054 / 2738;
            transform: translate(160%, -20%) rotate(4deg);
            z-index: 1
        }

        .card:nth-child(5) {
            /*background-image: url(images/colin-lloyd-RpK45xkkJ9o-unsplash.jpg);*/
            background-size: contain;
            width: 35vmin;
            aspect-ratio: 2054 / 2738;
            transform: translate(20%, -50%) rotate(-2deg);
            z-index: 1;
        }

        .card:nth-child(4):hover, .card:nth-child(5):hover {
            width: 35.5vmin;
            z-index: 100;
        }

        .card[data-status="unloaded"] {
            transform: translateY(-90%) rotate(0deg);
        }
    }

    /* alternative css for small screens */
    @media (max-width: 800px) {
        body {
            margin: 0;
            background-image: linear-gradient(rgb(8, 2, 16), rgb(25, 2, 57));
            width: 100%;
            display: grid;
            place-items: center;
        }

        .cards, .card {
            width: 80vmin;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            row-gap: 10vh;
        }

        .card {
            transition: 750ms ease-in;
            color: white;
            font-family: 'Reenie Beanie', cursive;
            font-size: 18px;
            font-weight: 400;
            box-shadow: 0px 0px 30px rgb(8, 2, 16);
            display: flex;
            flex-direction: column;
            justify-content: flex-end;
            text-align: end;
        }

        .card p {
            transform: translateY(40px);
        }

        .card:nth-child(1) {
            background-image: url(images/aditya-chinchure-ZhQCZjr9fHo-unsplash.jpg);
            aspect-ratio: 3909 / 2932;
            background-size: contain;
            transform: rotate(1deg);
        }

        .card:nth-child(2) {
            background-image: url(images/spencer-davis-naFHFLV5cqU-unsplash.jpg);
            background-size: contain;
            aspect-ratio: 6299 / 4199;
            transform: rotate(-2deg);
        }

        .card:nth-child(3) {
            background-image: url(images/nainoa-shizuru-NcdG9mK3PBY-unsplash.jpg);
            background-size: contain;
            aspect-ratio: 5184 / 3456;
            transform: rotate(2deg);
        }

        .card:nth-child(4) {
            background-image: url(images/muneeb-syed-4_M8uIfPEZw-unsplash.jpg);
            background-size: contain;
            aspect-ratio: 2054 / 2738;
            transform: rotate(-2.5deg);
        }

        .card:nth-child(5) {
            background-image: url(images/colin-lloyd-RpK45xkkJ9o-unsplash.jpg);
            background-size: contain;
            aspect-ratio: 2054 / 2738;
            transform: rotate(2deg);
            margin-bottom: 20px;
        }
    }
</style>