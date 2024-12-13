<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Biblio - Your Personal Book Haven</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
            color: #333;
        }
        header {
            background-color: #a2d5f2; /* Pastel blue */
            color: white;
            padding: 20px;
            text-align: center;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 1000;
            transform: translateY(0);
            transition: transform 0.3s ease-in-out;
        }
        nav {
            display: none;
            justify-content: center;
            background-color: #a2d5f2; /* Pastel blue */
            padding: 10px 0;
            position: fixed;
            top: 0;
            width: 100%;
            z-index: 999;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            padding: 10px 15px;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        nav a:hover {
            background-color: #7bb1d1;
        }
        main {
            text-align: center;
            margin: 120px 20px 20px; /* To account for the fixed header */
            font-size: 1.2em;
        }
        .scrolled header {
            transform: translateY(-100%);
        }
        .scrolled nav {
            display: flex;
        }
    </style>
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const header = document.querySelector('header');
            const nav = document.querySelector('nav');
            let lastScrollY = window.scrollY;

            window.addEventListener('scroll', () => {
                if (window.scrollY > lastScrollY) {
                    document.body.classList.add('scrolled');
                } else {
                    document.body.classList.remove('scrolled');
                }
                lastScrollY = window.scrollY;
            });
        });
    </script>
</head>
<body>
    <header>
        <h1>Welcome to Biblio</h1>
        <p>Your personalized book experience, all in one place.</p>
    </header>
    <nav>
        <a href="#favourites">Your Favourites</a>
        <a href="#reading-challenge">Reading Challenge</a>
        <a href="#curate-playlists">Curate Playlists</a>
        <a href="#your-reviews">Your Reviews</a>
    </nav>
    <main>
        <p>Select a menu option above to explore your literary journey.</p>
    </main>
</body>
</html>

