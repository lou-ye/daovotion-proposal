<script>
    let IslaImg = "https://imgs.search.brave.com/MkwMi69Ql_OzTWY5CRWgVlR0k6brPhmKAmQUE2PSB9o/rs:fit:711:225:1/g:ce/aHR0cHM6Ly90c2U0/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC5J/SzBkUjg3YU92MGIx/SHl4TnZsNG1nSGFF/OCZwaWQ9QXBp";
    
    export let name;
    export let description;
    export let logo;
    export let url;
    export let score;
    export let funds;
    export let price;
</script>

<style>
    .Project {
        margin-top: 50px;
        width: 300px;
        height: 400px;
        font-size: 0.8rem;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
        border-radius: 30px;
        text-align: center;
        padding: 10px;
    }

    .Project-info {
        text-align: center;
    }

    .Project-info-header {
        margin-top: 5%;
        margin-left: 10%;
        display: flex;
    }

    .Project-info-header h1 {
        margin-left: 10%;
        display: flex;
    }

    .Project-img {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        border: 0.5px solid #F8F8FF;
    }

    .Project-description {
        word-wrap: break-word;
    }

    .Project-repository {
        color: darkcyan;
    }

    .Project-balance {
        margin-top: 10px;
        display: flex;
        justify-content: space-evenly;
    }

    .Project-balance h2 {
        margin-left: 20px;
    }

    .Project-prestige-icon {
        display: flex;
    }

    .fa-star {
        margin-top: 10px;
        color: gold;
        font-size: 30px;
    }

    .Project-funds-icon {
        display: flex;
    }

    .fa-coins {
        margin-top: 10px;
        color: gold;
        font-size: 30px;
    }

    .Project-land-icon {
        margin-left: 30%;
        display: flex;
    }

    .Project-land h3 {
        margin-top: 10px;
        margin-bottom: 0px;
    }

    .Project-land-icon h2 {
        margin-left: 30px;
        margin-top: 20px;
        display: flex;
    }

    .Project-land img {
        width: 60px;
        height: 60px;
    }

    .Project-land-button {
        margin-top: 10px;
        width: 100px;
        height: 50px;
        border: none;
        padding: 10px 15px;
        text-align: center;
        font-size: 1rem;
        background-color: darkcyan;
        border-radius: 50px;
        color: white;
        font-family: 'Inter', sans-serif;
        font-weight: bold;
    }
</style>

<div class="Project">
    <div>
        <div class="Project-info">
            <div class="Project-info-header">
                <img class="Project-img" src={logo} alt="Project img">
                <h1>{name}</h1>
            </div>
            <p class="Project-description">{description}</p>
            <a class="Project-repository" href="__blank">{url}</a>
        </div>
        <div class="Project-balance">
            <div class="Project-prestige-icon">
                <i class="fa-solid fa-star"></i>
                <h2>{score}</h2>
            </div>
            <div class="Project-funds-icon">
                <i class="fa-solid fa-coins"></i>
                <h2>${funds}</h2>
            </div>
        </div>
        <div class="Project-land">
            <h3>¡Apoya este proyecto!</h3>
            <div class="Project-land-icon">
                <img src={IslaImg} alt="Isla">
                <h2>{price}</h2>
            </div>
            <button class="Project-land-button">Comprar</button>
        </div>
    </div>
</div>