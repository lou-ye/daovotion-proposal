<script>
    let SpanishFlag = "https://upload.wikimedia.org/wikipedia/commons/thumb/8/89/Bandera_de_Espa%C3%B1a.svg/400px-Bandera_de_Espa%C3%B1a.svg.png";
    let EnglishFlag = "https://upload.wikimedia.org/wikipedia/commons/thumb/a/ae/Flag_of_the_United_Kingdom.svg/400px-Flag_of_the_United_Kingdom.svg.png";
</script>

<style>
    .Language-dropdown {
        position: relative;
        display: inline-block;
        margin-left: 350px;
    }

    p {
        font-family: 'Inter', sans-serif;
    }

    .Language-dropdown-button {
        width: 60px;
        height: 40px;
        border: none;
        padding: 15px 32px;
        text-align: center;
        display: inline-block;
        font-size: 1.1rem;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 0;
        padding: 3px;
        border-radius: 3px;
        background-color: white;
    }

    .Language-dropdown-button img {
        width: 20px; 
        height: 15px;
    }

    .Language-dropdown:hover .Language-dropdown-button {
        background-color: #F8F8FF;
    }

    .Language-dropdown-content {
        width: 60px;
        display: none;
        position: absolute;
        z-index: 1;
        font-size: 1.1rem; 
        border: 0.5px solid #DCDCDC;
        border-radius: 3px;
    }

    .Language-dropdown:hover .Language-dropdown-content {
        display: block;
    }
    
    .Language-dropdown-content li {
        display: flex;
        text-align: center;
    }

    .Language-dropdown-content li p {
        margin-left: 5px;
        margin-right: 10px;
    }

    .Language-dropdown-content img {
        margin-top: 20px;
        width: 20px; 
        height: 15px;
    }
  
    .Language-dropdown-content li:hover {
        background-color: #F8F8FF;
    }
</style>

<div class="Language">
    <div class="Language-dropdown">
        <button class="Language-dropdown-button">
            <p>ES</p>
            <img src={SpanishFlag} alt="Spanish Flag">
        </button>
          
        <div class="Language-dropdown-content">
            <li>
                <p>ES</p> 
                <img src={SpanishFlag} alt="Spanish Flag">
            </li>
            <li>
                <p>EN</p> 
                <img src={EnglishFlag} alt="English Flag">
            </li>
        </div>
    </div>
</div>