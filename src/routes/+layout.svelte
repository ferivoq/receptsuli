<svelte:head>
    <title>Receptek</title>
</svelte:head>

<div class="container">
    <header>
        <a href="/"><h1 class="page-title">Feri Receptjei</h1></a>
        <nav>
            <a class="navbar-link" href="/">Főoldal</a>
            <a class="navbar-link" href="/receptek">Receptek</a>
            <a class="navbar-link" href="/rolam">Rólam</a>
            <a class="navbar-link" href="/kontaktok">Kontaktok</a>
        </nav>
    </header>
    <div class="card">
        <div class="card-inner">
            <slot />
        </div>
    </div>
</div>

<style>
        :global(html) {
            margin: 0;
            height: 100%;
            font-family: "Mulish", sans-serif;
            color: #ffffff;
            background: linear-gradient(135deg, #e3dbf6, #a99bf9);
        }

        header {
            text-align: center;
            margin-bottom: 20px;
        }

        nav {
            display: flex;
            justify-content: center;
        }

        a {
            color: #fff;
            text-decoration: none;
        }

        .navbar-link {
            margin: 0 20px;
            transition: transform 0.2s;
        }

        .navbar-link:hover {
            transform: scale(1.1);
        }

        .page-title {
            text-align: center;
            margin: 20px 0;
        }

        .container {
            width: auto;
            height: 100%;
            padding: 10px;
        }

        .card {
            width: 500px;
            margin: auto;
            padding: 100px;
            border-radius: 1.5rem;
            background: #fff;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.2);
        }

        @media (max-width: 769px) {
            .card{
                width: 300px;
            }
        }

        @media (max-width: 530px) {
            .card{
                width: 160px;
            }
        }
</style>
