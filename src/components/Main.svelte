<script>
    import Interaction from "./Interaction.svelte";
    import Project from "./Project.svelte";
    import {link} from 'svelte-spa-router'

</script>

<style>
    .Main {
        width: 100%;
        height: auto;
        font-size: 1.3rem;
        position: relative;
    }

    .Main-section-description {
        position: absolute;
        width: 800px;
        margin-top: 100px;
        margin-left: 150px;
    }

    .Main-section-description h1 {
        margin: 0;
        font-size: 4rem;
        font-weight: 700;
    }

    .Main-section-description h3 {
        font-weight: 700;
    }

    .Main-section-description p {
        margin-bottom: 40px;
    }

    .Main-section-description a {
        text-decoration: none;
        width: auto;
        height: 50px;
        padding: 10px 20px;
        font-size: 1.2rem;
        font-weight: 1000;
        color: darkcyan;
        background-color: white;
        border: 3px solid darkcyan;
        border-radius: 50px;
        font-family: 'Inter', sans-serif;
    }

    .Main-section-projects {
        position: absolute;
        width: 400px;
        height: 100%;
        margin-left: 1000px;
        display: flex;
    }

    .Main-section-projects-button {
        width: 50px;
        height: 50px;
        display: inline-block;
        color: darkcyan;
        background-color: white;
        border: 1px solid darkcyan;
        border-radius: 50px;
        margin-top: 60%;
        margin-left: 5%;
    }

    .Main-section-projects-button i {
        font-size: 1.5rem;
    }
</style>

<div class="Main">
    <section class="Main-section">
        <div class="Main-section-description">
            <h1>DAOVOTION</h1>
            <h3>Apoya el financiamiento del OSS y gana dinero en el Metaverso.</h3>
            <p>DAOVOTION es una plataforma de organizaciones decentralizadas (DAO), que gestiona el recaudo para proyectos de Software Libre (FOSS), mediante la venta de tierras ligadas al Metaverso Abierto: Las Meta Islas.</p>
            <a href="/governance/" use:link>Saber mas</a>
            <!-- <a href="/projects/" use:link>Explorar proyectos</a> -->
        </div>
        <div class="Main-section-projects">
            <Project />
            <button class="Main-section-projects-button">
                <i class="fa-solid fa-arrow-right"></i>
            </button>
        </div>
    </section>
    <Interaction />
</div>