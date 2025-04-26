<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vexto Services</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #1a1a2e, #16213e);
            color: #fff;
            overflow-x: hidden;
        }

        /* Navigation */
        nav {
            background: rgba(0, 0, 0, 0.8);
            padding: 1rem 2rem;
            position: fixed;
            width: 100%;
            z-index: 1000;
            backdrop-filter: blur(5px);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 2rem;
        }

        nav a {
            color: #fff;
            text-decoration: none;
            font-size: 1.2rem;
            transition: color 0.3s ease;
        }

        nav a:hover {
            color: #00ff88;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 2rem;
        }

        .hero h1 {
            font-size: 4rem;
            margin-bottom: 1rem;
            animation: slideIn 1s ease-out;
            text-shadow: 0 0 10px rgba(0, 255, 136, 0.5);
        }

        .hero p {
            font-size: 1.5rem;
            max-width: 600px;
            animation: fadeIn 2s ease-out;
        }

        /* About Section */
        .about {
            padding: 5rem 2rem;
            background: rgba(255, 255, 255, 0.05);
        }

        .about h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 2rem;
            animation: slideIn 1s ease-out;
        }

        .about-content {
            max-width: 800px;
            margin: 0 auto;
            line-height: 1.6;
            font-size: 1.2rem;
            animation: fadeIn 2s ease-out;
        }

        /* Socials Section */
        .socials {
            padding: 5rem 2rem;
            text-align: center;
        }

        .socials h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            animation: slideIn 1s ease-out;
        }

        .social-link {
            display: inline-flex;
            align-items: center;
            gap: 1rem;
            font-size: 1.5rem;
            color: #fff;
            text-decoration: none;
            background: #7289da;
            padding: 0.8rem 1.5rem;
            border-radius: 50px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: fadeIn 2s ease-out;
        }

        .social-link:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0, 255, 136, 0.4);
        }

        .social-link img {
            width: 30px;
            height: 30px;
        }

        /* Snow Effect */
        .snow {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 0;
        }

        .snowflake {
            position: absolute;
            background: #fff;
            border-radius: 50%;
            opacity: 0.6;
            animation: fall linear infinite;
        }

        @keyframes fall {
            0% {
                transform: translateY(-10vh);
                opacity: 0.6;
            }
            100% {
                transform: translateY(100vh);
                opacity: 0.2;
            }
        }

        /* Text Animations */
        @keyframes slideIn {
            from {
                transform: translateY(50px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.2rem;
            }

            .about h2,
            .socials h2 {
                font-size: 2rem;
            }

            nav ul {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#socials">Socials</a></li>
        </ul>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <h1>Vexto Services</h1>
        <p>Premium scripting and instant delivery for your development needs.</p>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <h2>About Me</h2>
        <div class="about-content">
            <p>I provide top-tier scripting services with a focus on instant delivery. Specializing in Lua and Python, I create efficient, reliable, and customized scripts tailored to your needs. Whether you're looking for game development solutions or automation scripts, I've got you covered with professional-grade code and fast turnaround times.</p>
        </div>
    </section>

    <!-- Socials Section -->
    <section id="socials" class="socials">
        <h2>Socials</h2>
        <a href="https://discord.com" class="social-link">
            <img src="https://cdn.jsdelivr.net/npm/simple-icons@v9/icons/discord.svg" alt="Discord">
            414_fivestare
        </a>
    </section>

    <!-- Snow Effect -->
    <div class="snow"></div>

    <script>
        // Snow Effect
        function createSnowflake() {
            const snowflake = document.createElement('div');
            snowflake.classList.add('snowflake');
            snowflake.style.width = `${Math.random() * 5 + 2}px`;
            snowflake.style.height = snowflake.style.width;
            snowflake.style.left = `${Math.random() * 100}vw`;
            snowflake.style.animationDuration = `${Math.random() * 5 + 5}s`;
            document.querySelector('.snow').appendChild(snowflake);

            setTimeout(() => {
                snowflake.remove();
            }, 10000);
        }

        setInterval(createSnowflake, 100);
    </script>
</body>
</html>
