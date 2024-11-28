<header>
    <h1 class="Title">Title</h1>
    <input type="checkbox" id="menu-toggle" class="menu-toggle" aria-label="Menu Toggle" />
    <label for="menu-toggle" class="hamburger">
        <span></span>
        <span></span>
        <span></span>
    </label>
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
        position: relative; /* Pro absolutní pozicování navigace */
    }

    h1 {
        margin: 0;
        font-size: 24px;
        color: black; /* Bílé písmo pro kontrast */
    }

    .web-location {
        display: flex; /* Pro odkazy vedle sebe na desktopu */
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

    .menu-toggle {
        display: none; /* Skrytý checkbox */
    }

    /* Hamburger menu pro mobil */
    @media (max-width: 600px) {
        .hamburger {
            display: flex; /* Zobrazí se pouze na mobilu */
            flex-direction: column;
            justify-content: center;
            gap: 4px;
            width: 30px;
            height: 30px;
            cursor: pointer;
        }

        .hamburger span {
            display: block;
            width: 100%;
            height: 3px;
            background: black;
            transition: all 0.3s ease-in-out;
        }

        .menu-toggle {
            display: none; /* Checkbox zůstává skrytý */
        }

        /* Efekt hamburgeru při zaškrtnutí */
        .menu-toggle:checked ~ .hamburger span:nth-child(1) {
            transform: translateY(8px) rotate(45deg);
        }

        .menu-toggle:checked ~ .hamburger span:nth-child(2) {
            opacity: 0; /* Prostřední čára zmizí */
        }

        .menu-toggle:checked ~ .hamburger span:nth-child(3) {
            transform: translateY(-8px) rotate(-45deg);
        }

        .web-location {
            display: none; /* Skryté menu při načtení */
            flex-direction: column; /* Menu pod sebou */
            position: absolute;
            top: 70px;
            right: 0;
            background-color: rgb(29, 127, 201);
            width: 100%;
            gap: 10px;
            padding: 10px 0;
            overflow: hidden;
            max-height: 0; /* Výchozí výška skrytého menu */
            animation: closeMenu 0.3s ease-in-out; /* Zavírací animace */
        }

        .menu-toggle:checked ~ .web-location {
            display: flex; /* Zobrazení menu */
            max-height: 300px; /* Maximální výška při zobrazení */
            animation: openMenu 0.3s ease-in-out; /* Otevírací animace */
        }

        .web-location a {
            text-align: center; /* Zarovnání odkazů na střed */
            font-size: 14px;
            color: black;
        }

        .web-location a:hover {
            color: white; /* Efekt při hoveru */
        }
    }

    /* Keyframes pro animaci otevírání a zavírání */
    @keyframes openMenu {
        from {
            max-height: 0;
            opacity: 0;
        }
        to {
            max-height: 300px;
            opacity: 1;
        }
    }

    @keyframes closeMenu {
        from {
            max-height: 300px;
            opacity: 1;
        }
        to {
            max-height: 0;
            opacity: 0;
        }
    }
</style>
