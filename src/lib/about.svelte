<script>
    import { pokemon_data, description } from "$lib/fetchData.js";
</script>

<div id="about">
    <p id="header">About</p>

    <p id="height">Height: {$pokemon_data.height/10} m</p>
    <p id="weight">Weight: {$pokemon_data.weight/10} kg</p>

    <p id="description">{$description[Math.floor(Math.random() * $description.length)]}</p>
</div>

<style>
    #about {
        width: 90%;
        height: 90%;
        margin: 1rem;
    }

    #header {
        font-size: calc(var(--header-font) - 0.3rem);
        font-weight: bold;
        margin-bottom: 2rem;
    }

    #height, #weight {
        font-size: var(--font);
    }

    #description {
        font-size: var(--font);
        margin-top: 2rem;
    }

    @media only screen and (max-width: 40em) {
        #header {
            margin-bottom: 0.5rem;
        }

        #height, #weight {
            font-size: var(--small-font);
        }

        #description {
            font-size: var(--small-font);
            margin-top: 0.5rem;
        }
    }
</style>