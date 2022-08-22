<script>
    import Logo from "./Logo.svelte";
</script>

<style>
    .Footer {
        background-color: #F5F5F5;
        width: 100%;
        height: auto;
        display: flex;
        justify-content: space-evenly;
        margin-top: 50px;
        padding: 10px;
    }

    .Footer div {
        margin-right: 200px;
        width: 20%;
        text-align: center;
        width: 20%;
    }

    .Footer-logo {
        margin-top: 20px;
    }

    .Footer h3 {
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
    }

    .Footer i {
        font-size: 1.3rem;
        margin-right: 20px;
    }

    .Footer a {
        text-align: center;
        text-decoration: none;
        color: black;
    }

    .Footer a:hover {
        color: darkcyan;
    }
</style>

<div class="Footer">
    <div class="Footer-logo">
        <Logo />
    </div>
    <div>
        <h3>Contacto</h3>
        <ul>
            <li>
                <i class="fa-solid fa-location-dot"></i>
                Colombia
            </li>
            <li>
                <i class="fa-solid fa-envelope"></i>
                daovotion@gmail.com
            </li>
        </ul>
    </div>
    <div>
        <h3>Informacion</h3>
        <ul>
            <li><a href="__blank">Whitepaper</a></li>
            <li><a href="__blank">FAQs</a></li>
            <li><a href="__blank">Sobre nosotros</a></li>
        </ul>
    </div>
    <div>
        <h3>Redes</h3>
        <ul>
            <li><a href="__blank">Discord</a></li>
            <li><a href="__blank">Telegram</a></li>
            <li><a href="__blank">Twitter</a></li>
            <li><a href="__blank">Instagram</a></li>
        </ul>
    </div>
</div>