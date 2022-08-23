<script>
    import Footer from "../components/Footer.svelte";
    import Header from "../components/Header.svelte";
    import Project from "../components/Project.svelte";
    import { writable, derived } from 'svelte/store';

    let projects = [
        { name: 'Proyecto 43', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 41', description: 'fwcdSEVFW51EDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
    ];


    let term = writable('');
    let items = writable(projects);
    let filtered = derived([term, items], ([$term, $items]) => $items.filter(x => x.name.includes($term) || x.description.includes($term)));
	let val = '';
	$: term.set(val);
</script>

<style>
    .Projects-search {
        width: 400px;
        height: auto;
        padding: 10px 20px;
        display: flex;
        color: darkcyan;
        background-color: white;
        border: 3px solid darkcyan;
        border-radius: 30px;
        font-family: 'Inter', sans-serif;
        margin-top: 30px;
        margin-left: 35%;
    }

    .Projects-search i {
        margin-right: 5%;
    }

    .Projects-search input {
        border: 0;
        outline: 0;
        font-size: 1rem;
    }

    .Projects-list {
        text-align: center;
    }

    .Projects-list p {
        margin-top: 12%;
        margin-bottom: 12%;
    }

    .Projects-list div {
        margin: 0px 50px 0px 50px;
        display: inline-flex;
    }
</style>

<div class="Projects">
    <Header />
    <div class="Projects-search">
        <i class="fa-solid fa-magnifying-glass"></i>
        <input type="text" placeholder="Buscar proyecto" bind:value={val} id="searchInput">
    </div>
    <div class="Projects-list">
        {#each $filtered as project}
            <div>
                <Project {...project}></Project>
            </div>
        {:else}
            <p>No pudimos encontrar ese proyecto.</p>
        {/each}
    </div>
    <Footer />
</div>