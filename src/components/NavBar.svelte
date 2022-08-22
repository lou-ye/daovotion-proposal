<script>
    import {link} from 'svelte-spa-router'
</script>

<style>
    .NavBar {
        margin-left: 100px;
    }

    .NavBar-ul {
        padding: 0;
        list-style: none;
    }

    .NavBar-ul-li {
        display: inline-block;
        padding-right: 2rem;
    }

    .NavBar-ul-li a {
        color: black;
        text-decoration: none;
    }

    .NavBar-ul-li a:hover {
        color: darkcyan;
    }
</style>

<div class="NavBar">
    <nav>
        <ul class="NavBar-ul">
            <li class="NavBar-ul-li"><a href="/projects/" use:link>Proyectos</a></li>
            <li class="NavBar-ul-li"><a href="/governance/" use:link>Gobernanza</a></li>
            <li class="NavBar-ul-li"><a href="/blog/" use:link>Blog</a></li>
            <li class="NavBar-ul-li"><a href="/help/" use:link>Ayuda</a></li>
        </ul>
    </nav>
</div>