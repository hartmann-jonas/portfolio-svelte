<script>
	import { fly } from "svelte/transition"
    export const projectsOrder = new Array;
    const projects = [
        {
            name: "LOLLAPALOOZA",
            tasks: "LIGHT OPERATING",
            location: "BERLIN",
            year: "2022",
        },
        {
            name: "MASSA TINCIDUNT",
            tasks: "STAGE DESIGN, LIGHT DESIGN, LIGHT OPERATING",
            location: "WORLD TOUR",
            year: "2022",
        },
        {
            name: "LOREM IPSUM",
            tasks: "STAGE DESIGN, LIGHT DESIGN",
            location: "EUROPE TOUR",
            year: "2021",
        },
        {
            name: "BELL FESTIVAL",
            tasks: "STAGE DESIGN, LIGHT PROGRAMMING",
            location: "QUEBEC",
            year: "2020",
        },
        {
            name: "ELECTRA",
            tasks: "LIGHT DESIGN, LIGHT OPERATING",
            location: "ON TOUR",
            year: "2023",
        },
    ];

    projects.slice().reverse()
    .forEach(function(item) {
            new Promise(r => setTimeout(r, 2000));
            projectsOrder.push(item);
        });

    console.log(projects)
</script>


<body in:fly={{ y: 60, duration: 700, delay: 500 }} out:fly={{ y: -40, duration: 500 }}>
    <div class="index">
        {#each projectsOrder as project}
        <div class="row">
            <div class="column1">
                <p>{project.name}</p>
            </div>
            <div class="column2">
                <p>{project.tasks}</p>
            </div>
            <div class="column3">
                <p>{project.location}</p>
            </div>
            <div class="column4">
                <p>{project.year}</p>
            </div>
        </div>
        {/each}
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

    .index {
        font-family: 'Playfair Display';
        font-weight: 400;
        margin-top: 5vmin;
    }

    .column1 {
        width: 15%;
    }

    .column2 {
        width: 40%;
    }

    .column3 {
        width: 15%;
    }

    .column4 {
        font-weight: 800;
        width: 10%;
    }

    .row {
        display: flex;
        justify-content: space-evenly;
        width: 100vw;
    }


    .row:hover {
        background-color: white;
        color: black
    }
</style>