# Kavyansh-3
<!DOCTYPE html>
<html lang=“en”>
<head>
    <meta charset=“UTF-8”>
    <meta name=“viewport” content=“width=device-width, initial-scale=1.0”>
    <title>Kavyansh | Data Science Portfolio</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            —bg: #080d1c;
            —card: #121d35;
            —cyan: #00d4ff;
            —blue: #6575ff;
            —white: #ffffff;
            —text: #aab6cc;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, sans-serif;
            background: var(—bg);
            color: var(—white);
            line-height: 1.7;
        }

        #header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 8%;
            background: var(—card);
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 3px 15px #00000050;
        }

        #header h1 span,
        footer span {
            color: var(—cyan);
        }

        nav ul {
            display: flex;
            gap: 25px;
            list-style: none;
        }

        nav a {
            color: white;
            text-decoration: none;
            transition: 0.3s;
        }

        nav a:hover {
            color: var(—cyan);
        }

        #home {
            min-height: 85vh;
            padding: 80px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            gap: 40px;
            background: linear-gradient(135deg, #080d1c, #172b50);
        }

        .hero-content {
            max-width: 550px;
        }

        .tagline {
            color: var(—cyan);
            letter-spacing: 4px;
            font-weight: bold;
        }

        .hero-content h2 {
            font-size: clamp(35px, 5vw, 60px);
            line-height: 1.2;
            margin: 20px 0;
        }

        .hero-content h2 span {
            color: var(—cyan);
        }

        .hero-content p {
            color: var(—text);
            margin-bottom: 25px;
        }

        .btn {
            display: inline-block;
            padding: 12px 25px;
            background: var(—cyan);
            color: var(—bg);
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: 0.3s;
        }

        .btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 20px #00d4ff66;
        }

        .hero-card {
            background: var(—card);
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            border: 1px solid #00d4ff55;
            animation: float 3s ease-in-out infinite;
        }

        .shield {
            font-size: 75px;
            margin-bottom: 15px;
        }

        .hero-card p {
            color: var(—cyan);
            margin-top: 15px;
        }

        section:not(#home) {
            padding: 80px 8%;
        }

        section h2 {
            font-size: 35px;
            margin-bottom: 35px;
        }

        section h2 span {
            color: var(—cyan);
        }

        #about {
            background: #0b1224;
        }

        .about-container {
            display: flex;
            align-items: center;
            gap: 50px;
            flex-wrap: wrap;
        }

        .profile {
            flex: 1;
            min-width: 220px;
            padding: 30px;
            text-align: center;
            background: var(—card);
            border-radius: 15px;
        }

        .profile-circle {
            width: 130px;
            height: 130px;
            margin: auto auto 15px;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 50%;
            background: linear-gradient(135deg, var(—cyan), var(—blue));
            color: var(—bg);
            font-size: 60px;
            font-weight: bold;
        }

        .about-text {
            flex: 2;
            min-width: 250px;
            color: var(—text);
        }

        .about-text h3 {
            color: white;
            margin-bottom: 15px;
        }

        .project-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .project-card {
            background: var(—card);
            padding: 30px;
            border-radius: 15px;
            border: 1px solid #ffffff15;
            transition: 0.4s;
        }

        .project-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: var(—cyan);
            box-shadow: 0 10px 30px #00d4ff25;
        }

        .project-card h3 {
            color: var(—cyan);
            margin-bottom: 15px;
        }

        .project-card p {
            color: var(—text);
            margin-bottom: 20px;
        }

        .project-card span {
            display: inline-block;
            padding: 5px 12px;
            background: #263c60;
            border-radius: 20px;
            color: var(—cyan);
            font-size: 12px;
        }

        #skills {
            background: #0b1224;
        }

        .skills-container {
            max-width: 650px;
        }

        .skill {
            margin-bottom: 25px;
        }

        .skill p {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .skill p span {
            color: var(—cyan);
        }

        .progress {
            width: 100%;
            height: 10px;
            background: #26344f;
            border-radius: 20px;
            overflow: hidden;
        }

        .progress div {
            height: 100%;
            border-radius: 20px;
            background: linear-gradient(90deg, var(—cyan), var(—blue));
            animation: grow 2s ease forwards;
        }

        .html {
            width: 75%;
        }

        .css {
            width: 55%;
        }

        .python {
            width: 45%;
        }

        .cyber {
            width: 50%;
        }

        #contact form {
            max-width: 600px;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        #contact input,
        #contact textarea {
            width: 100%;
            padding: 15px;
            background: var(—card);
            color: white;
            border: 1px solid #354563;
            border-radius: 8px;
            font-size: 16px;
            transition: 0.3s;
        }

        #contact input:focus,
        #contact textarea:focus {
            outline: none;
            border-color: var(—cyan);
            box-shadow: 0 0 10px #00d4ff33;
        }

        #contact button {
            padding: 14px;
            background: var(—cyan);
            color: var(—bg);
            border: none;
            border-radius: 8px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
        }

        #contact button:hover {
            background: var(—blue);
            color: white;
            transform: translateY(-3px);
        }

        footer {
            padding: 30px;
            text-align: center;
            background: var(—card);
            color: var(—text);
        }

        footer p {
            font-size: 14px;
        }

        @keyframes float {
            0%, 100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(-15px);
            }
        }

        @keyframes grow {
            from {
                width: 0;
            }

            to {
                width: 100%;
            }
        }

        @media (max-width: 900px) {
            .project-container {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 600px) {
            #header {
                flex-direction: column;
                gap: 15px;
                padding: 15px;
            }

            nav ul {
                justify-content: center;
                flex-wrap: wrap;
                gap: 15px;
            }

            #home {
                flex-direction: column;
                text-align: center;
                padding: 60px 6%;
            }

            .hero-content h2 {
                font-size: 36px;
            }

            .hero-card {
                width: 100%;
            }

            .project-container {
                grid-template-columns: 1fr;
            }

            .about-container {
                flex-direction: column;
            }

            section:not(#home) {
                padding: 55px 6%;
            }
        }

        @media (prefers-reduced-motion: reduce) {
            *,
            *::before,
            *::after {
                animation: none !important;
                transition: none !important;
            }
        }
    </style>
</head>

<body>

    <header id=“header”>
        <h1>Kavyansh<span>.</span></h1>

        <nav>
            <ul>
                <li><a href=“#home”>Home</a></li>
                <li><a href=“#about”>About</a></li>
                <li><a href=“#projects”>Projects</a></li>
                <li><a href=“#skills”>Skills</a></li>
                <li><a href=“#contact”>Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>

        <section id=“home”>
            <div class=“hero-content”>
                <p class=“tagline”>DATA SCIENCE STUDENT</p>

                <h2>
                    Turning Data Into
                    <span>Insights.</span>
                </h2>

                <p>
                    Hi, I’m Kavyansh, an 18-year-old student interested in
                    data science, programming, data analysis and technology.
                </p>

                <a href=“#projects” class=“btn”>
                    Explore My Work
                </a>
            </div>

            <div class=“hero-card”>
                <div class=“shield”>📊</div>
                <h3>Stay Curious.</h3>
                <h3>Stay Secure.</h3>
                <p>Learn • Build • Secure</p>
            </div>
        </section>

        <section id=“about”>
            <h2>About <span>Me</span></h2>

            <div class=“about-container”>

                <div class=“profile”>
                    <div class=“profile-circle”>K</div>
                    <h3>Kavyansh</h3>
                    <p>Data Science Student | Age 18</p>
                </div>

                <div class=“about-text”>
                    <h3>Who Am I?</h3>

                    <p>
                        I am an 18-year-old student interested in data science.
                        I am learning Python, data analysis, statistics
                        and the fundamentals of working with data.
                    </p>

                    <p>
                        My goal is to improve my technical knowledge
                        and develop practical skills through projects.
                    </p>
                </div>

            </div>
        </section>

        <section id=“projects”>
            <h2>My <span>Projects</span></h2>

            <div class=“project-container”>

                <article class=“project-card”>
                    <h3>Portfolio Website</h3>
                    <p>
                        A responsive personal website created
                        using HTML5 and advanced CSS3.
                    </p>
                    <span>HTML • CSS</span>
                </article>

                <article class=“project-card”>
                    <h3>Data Cleaning</h3>
                    <p>
                        A beginner project to understand
                        password length and character variety.
                    </p>
                    <span>Python • Data Analysis</span>
                </article>

                <article class=“project-card”>
                    <h3>Data Visualization</h3>
                    <p>
                        An informational project about common
                        network ports and their uses.
                    </p>
                    <span>Python • Visualization</span>
                </article>

            </div>
        </section>

        <section id=“skills”>
            <h2>Technical <span>Skills</span></h2>

            <div class=“skills-container”>

                <div class=“skill”>
                    <p>HTML5 <span>75%</span></p>
                    <div class=“progress”>
                        <div class=“html”></div>
                    </div>
                </div>

                <div class=“skill”>
                    <p>CSS3 <span>55%</span></p>
                    <div class=“progress”>
                        <div class=“css”></div>
                    </div>
                </div>

                <div class=“skill”>
                    <p>Python <span>45%</span></p>
                    <div class=“progress”>
                        <div class=“python”></div>
                    </div>
                </div>

                <div class=“skill”>
                    <p>Data Analysis <span>50%</span></p>
                    <div class=“progress”>
                        <div class=“cyber”></div>
                    </div>
                </div>

            </div>
        </section>

        <section id=“contact”>
            <h2>Contact <span>Me</span></h2>

            <form action=“#”>
                <input type=“text”
                       placeholder=“Your Name” required>

                <input type=“email”
                       placeholder=“Your Email” required>

                <textarea rows=“5”
                          placeholder=“Write your message...”
                          required></textarea>

                <button type=“submit”>Send Message</button>
            </form>
        </section>

    </main>

    <footer>
        <h3>Kavyansh<span>.</span></h3>
        <p>Data Science Student | Python & Data Analysis</p>
        <p>&copy; 2026 Kavyansh. All Rights Reserved.</p>
    </footer>

</body>
</html>
