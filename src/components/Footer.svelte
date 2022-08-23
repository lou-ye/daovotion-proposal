<script>
    import Logo from "./Logo.svelte";
</script>

<style>
    .Footer {
        background-color: black;
        width: 100%;
        height: auto;
        display: flex;
        justify-content: space-evenly;
        padding-top: 50px;
        color: white;
    }

    .Footer div {
        width: 20%;
        text-align: center;
        width: 20%;
    }

    .Footer-logo {
        margin-top: 50px;
    }

    .Footer h5 {
        text-align: start;
    }

    .Footer ul {
        margin: 0;
        padding: 0;
    }

    .Footer li {
        display: flex;
        list-style: none;
        margin-bottom: 20px;
        font-size: 1rem;
    }

    .Footer i {
        font-size: 1.3rem;
        margin-right: 20px;
    }

    .Footer a {
        text-align: center;
        text-decoration: none;
        color: white;
        display: flex;
    }

    .Footer a:hover {
        color: #66ff99;
    }
</style>

<div class="Footer">
    <div class="Footer-logo">
        <Logo />
    </div>
    <div>
        <h5>Contacto</h5>
        <ul>
            <li>
                <i class="fa-solid fa-location-dot"></i>
                Colombia, Bogotá.
            </li>
            <li>
                <i class="fa-solid fa-envelope"></i>
                daovotion@gmail.com
            </li>
        </ul>
    </div>
    <div>
        <h5>Informacion</h5>
        <ul>
            <li><a href="__blank">Whitepaper</a></li>
            <li><a href="__blank">FAQs</a></li>
            <li><a href="__blank">Sobre nosotros</a></li>
        </ul>
    </div>
    <div>
        <h5>Redes</h5>
        <ul>
            <li><a href="__blank">Discord</a></li>
            <li><a href="__blank">Telegram</a></li>
            <li><a href="__blank">Twitter</a></li>
            <li><a href="__blank">Instagram</a></li>
        </ul>
    </div>
</div>