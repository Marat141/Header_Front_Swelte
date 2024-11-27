<header>
    <!--<img src="" alt="">-->
    <h1 class="Title">Title</h1>
    <div class="web-location">
        <a href="/">Home</a>
        <a href="/Login">Login</a>
        <a href="/Register">Register</a>
    </div>
</header>

<style lang="scss">
    body {
        margin: 0;
        padding: 0;
    }

    header {
        background-color: rgb(29, 127, 201);
        display: flex; /* Flexbox pro zarovnání obsahu */
        align-items: center; /* Vertikální zarovnání na střed */
        justify-content: space-between; /* Rozdělení prostoru mezi Title a odkazy */
        padding: 0 10px; /* Odsazení na stranách */
        height: 70px; /* Nastavení výšky hlavičky */
    }

    h1 {
        margin: 0;
        font-size: 24px;
        color: black; /* Bílé písmo pro kontrast */
    }

    .web-location {
        display: flex; /* Pro odkazy vedle sebe */
        gap: 20px; /* Vzdálenost mezi odkazy */

        a {
            text-decoration: none; /* Bez podtržení */
            color: black; /* Barva textu */
            font-weight: bold; /* Tučné písmo */
            font-size: 16px; /* Velikost písma */
        }

        a:hover {
            color: red; /* Efekt při přejetí myší */
        }
    }

    /* MEDIA QUERIES pro mobilní zařízení */
    @media (max-width: 600px) {
        header {
            flex-direction: column; /* Obsah bude ve sloupci */
            height: auto; /* Automatická výška */
            padding: 10px; /* Více odsazení pro lepší vzhled */
        }

        h1 {
            margin-bottom: 10px; /* Oddělení nadpisu od odkazů */
            text-align: center; /* Nadpis zarovnán na střed */
        }

        .web-location {
            justify-content: center; /* Odkazy zarovnány na střed */
            gap: 10px; /* Menší mezera mezi odkazy */
        }

        .web-location a {
            font-size: 14px; /* Menší písmo na malých obrazovkách */
        }
    }
</style>
