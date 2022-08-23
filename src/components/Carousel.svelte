<script>
    import Project from "./Project.svelte";

    let projects = [
        { name: 'Proyecto 1', description: 'fwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWfwcdSEfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 2', description: 'fwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCvhvCfwcdSEVFWEDvwefsdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 3', description: 'fwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 4', description: 'fwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
        { name: 'Proyecto 5', description: 'fwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCfwcdSEVFWEDvwefsdcjvhvCdcjvhvC' , logo: "https://imgs.search.brave.com/2qsV1m3NAbyCkQKYdO0tbd4rOK-bUydTX5DWb8KqcpI/rs:fit:844:225:1/g:ce/aHR0cHM6Ly90c2Uy/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5n/eGxsVDBmTHlhTzF6/bkxoSGNwa0ZnSGFF/SyZwaWQ9QXBp", url: "www.github.com.ar", score: 45, funds: 3000, price: 34},
    ];
</script>

<style>    
    @keyframes display {
        0% {
        transform: translateX(150px);
        opacity: 0;
        }
        10% {
        transform: translateX(0);
        opacity: 1;
        }
        20% {
        transform: translateX(0);
        opacity: 1;
        }
        30% {
        transform: translateX(-100px);
        opacity: 0;
        }
        50% {
        transform: translateX(-100px);
        opacity: 0;
        }
        100% {
        transform: translateX(-50px);
        opacity: 0;
        }
    }
    
    .Carousel {
        position: relative;
    }
    
    .Carousel > div {
        position: absolute;
        top: 0;
        left: calc(50% - 100px);
        opacity: 0;
        animation: display 20s infinite;
    }
    
    div:nth-child(2) {
    animation-delay: 4s;
    }

    div:nth-child(3) {
    animation-delay: 8s;
    }

    div:nth-child(4) {
    animation-delay: 12s;
    }

    div:nth-child(5) {
    animation-delay: 16s;
    }
</style>

<div class="Carousel">
    <div>
        <Project {...projects[0]}/>
    </div>
    <div>
        <Project {...projects[1]}/>
    </div>    
    <div>
        <Project {...projects[2]}/>
    </div>
    <div>
        <Project {...projects[3]}/>
    </div>
    <div>
        <Project {...projects[4]}/>
    </div>
</div>