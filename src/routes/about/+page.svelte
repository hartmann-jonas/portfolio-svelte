<script>
    import { fly } from 'svelte/transition';
</script>

<body in:fly={{ y: 60, duration: 700, delay: 500 }} out:fly={{ y: -40, duration: 500 }}>
    <div class="about">
        <h2>About me:</h2>
        <div class="p1">
            <p>Mauris rhoncus aenean vel elit scelerisque mauris pellentesque pulvinar pellentesque. Nam aliquam sem et tortor. Accumsan tortor posuere ac ut. Eget est lorem ipsum dolor sit. Turpis nunc eget lorem dolor sed. Dis parturient montes nascetur ridiculus. Senectus et netus et malesuada. Justo nec ultrices dui sapien eget mi. Interdum posuere lorem ipsum dolor sit amet. Facilisi cras fermentum odio eu feugiat. Sit amet porttitor eget dolor. Cursus mattis molestie a iaculis at erat pellentesque adipiscing commodo. Dictumst quisque sagittis purus sit amet volutpat. Pharetra massa massa ultricies mi quis.</p>
        </div>
        <div class="p2">
            <img src="images/about1.JPG" alt="about1">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Magna fermentum iaculis eu non diam phasellus vestibulum lorem sed. Venenatis a condimentum vitae sapien pellentesque habitant morbi tristique. Amet aliquam id diam maecenas ultricies mi eget mauris. Enim ut tellus elementum sagittis. Lectus vestibulum mattis ullamcorper velit sed ullamcorper morbi tincidunt. Eget nunc lobortis mattis aliquam. Egestas congue quisque egestas diam in arcu cursus euismod. Neque laoreet suspendisse interdum consectetur. Ornare massa eget egestas purus viverra accumsan in. In mollis nunc sed id semper risus in. Lacus luctus accumsan tortor posuere ac ut consequat semper viverra.</p>
        </div>
    </div>
</body>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;800&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Reenie+Beanie&display=swap');

    body {
        font-family: 'Reenie Beanie', cursive;
        color: white;
        margin: 0;
        width: 100%;
        height: 100vh;
        /*background-image: linear-gradient(rgb(8, 2, 16), rgb(25, 2, 57));*/
        background-color: rgb(8, 2, 16);
    }

    .about {
        margin: 7vmin;
    }

    .p1 {
        width: 80%;
    }

    .p2 {
        display: flex;
        justify-content: center;
        margin-top: 10vmin;
        gap: 5vmin;
    }

    .p2 img {
        width: 30%;
        height: 30%;
        min-width: 200px;
    }

    .p2 p {
        width: 50%;
    }

    @media (max-width: 820px) {
        .p1 {
            margin: auto;
        }

        .p2 {
            flex-direction: column;
            margin: auto;
        }
        .p2 img {
            margin: auto;
            width: 80%;
            height: 80%;
        }

        .p2 p {
            margin: auto;
            width: 80%;
        }
    }
</style>