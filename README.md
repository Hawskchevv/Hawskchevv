
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="theme-color" content="#1a1b26">

    <title>HAWSK | Personal Profile</title>

    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet">

    <style>
        :root {
            --bg: #1a1b26;
            --surface: #24283b;
            --surface-light: #292e42;
            --blue: #7aa2f7;
            --purple: #bb9af7;
            --cyan: #7dcfff;
            --text: #c0caf5;
            --muted: #565f89;
            --green: #9ece6a;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: var(--bg);
            color: var(--text);
            font-family: 'JetBrains Mono', monospace;
            line-height: 1.7;
        }

        a {
            color: var(--blue);
            text-decoration: none;
            transition: .3s;
        }

        a:hover {
            color: var(--purple);
        }

        .container {
            width: 90%;
            max-width: 950px;
            margin: auto;
        }

        /* HEADER */

        header {
            min-height: 390px;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
            background:
                linear-gradient(rgba(26,27,38,.55), rgba(26,27,38,1)),
                url("https://images.unsplash.com/photo-1519608487953-e999c86e7455?w=1600")
                center/cover;
            border-bottom: 1px solid var(--surface-light);
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .header-content h1 {
            font-size: clamp(3rem, 10vw, 6rem);
            letter-spacing: 12px;
            color: var(--text);
            text-shadow: 0 0 30px rgba(122,162,247,.35);
        }

        .subtitle {
            color: var(--blue);
            font-size: 13px;
            letter-spacing: 3px;
            margin-top: 5px;
        }

        .japanese {
            color: var(--purple);
            font-size: 13px;
            margin-top: 20px;
        }

        .status {
            display: inline-block;
            margin-top: 25px;
            padding: 5px 14px;
            border: 1px solid var(--muted);
            border-radius: 4px;
            font-size: 11px;
            color: var(--green);
        }

        .status::before {
            content: "● ";
        }

        /* NAVIGATION */

        nav {
            background: rgba(36,40,59,.95);
            border-bottom: 1px solid var(--surface-light);
            position: sticky;
            top: 0;
            z-index: 10;
            backdrop-filter: blur(10px);
        }

        nav .container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 25px;
            padding: 14px 0;
        }

        nav a {
            font-size: 11px;
            color: var(--muted);
        }

        nav a:hover {
            color: var(--blue);
        }

        /* SECTIONS */

        section {
            padding: 65px 0;
            border-bottom: 1px solid var(--surface-light);
        }

        .section-title {
            color: var(--blue);
            font-size: 17px;
            margin-bottom: 30px;
            letter-spacing: 2px;
        }

        .section-title span {
            color: var(--purple);
        }

        /* TERMINAL */

        .terminal {
            background: #16161e;
            border: 1px solid var(--surface-light);
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0,0,0,.2);
        }

        .terminal-header {
            background: var(--surface);
            padding: 12px 17px;
            display: flex;
            align-items: center;
            gap: 7px;
            font-size: 11px;
            color: var(--muted);
        }

        .dot {
            width: 9px;
            height: 9px;
            border-radius: 50%;
        }

        .red { background: #f7768e; }
        .yellow { background: #e0af68; }
        .green { background: #9ece6a; }

        .terminal-body {
            padding: 25px;
            font-size: 12px;
            overflow-x: auto;
        }

        .prompt {
            color: var(--green);
        }

        .command {
            color: var(--blue);
        }

        .output {
            color: var(--text);
            margin: 15px 0;
            white-space: pre-wrap;
        }

        /* ABOUT */

        .about-text {
            color: #a9b1d6;
            font-size: 13px;
            max-width: 750px;
        }

        .highlight {
            color: var(--purple);
        }

        /* INTERESTS */

        .interest-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }

        .interest-card {
            background: var(--surface);
            padding: 20px;
            border: 1px solid var(--surface-light);
            border-radius: 6px;
            transition: .3s;
        }

        .interest-card:hover {
            transform: translateY(-4px);
            border-color: var(--blue);
        }

        .interest-card h3 {
            font-size: 13px;
            color: var(--blue);
            margin-bottom: 8px;
        }

        .interest-card p {
            font-size: 11px;
            color: var(--muted);
        }

        /* SETUP */

        .setup-list {
            background: var(--surface);
            border-left: 3px solid var(--purple);
            padding: 20px 25px;
            font-size: 12px;
            color: #a9b1d6;
            overflow-x: auto;
        }

        .setup-list .folder {
            color: var(--blue);
        }

        /* TECH STACK */

        .tech-stack {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 18px;
        }

        .tech-stack img {
            width: 43px;
            transition: .3s;
        }

        .tech-stack img:hover {
            transform: translateY(-5px);
        }

        /* PROJECTS */

        .project {
            background: var(--surface);
            border: 1px solid var(--surface-light);
            padding: 20px;
            border-radius: 6px;
            margin-bottom: 13px;
        }

        .project h3 {
            color: var(--blue);
            font-size: 13px;
        }

        .project p {
            font-size: 11px;
            color: var(--muted);
            margin-top: 7px;
        }

        .project-status {
            display: inline-block;
            margin-top: 12px;
            font-size: 10px;
            color: var(--green);
        }

        /* STATS */

        .stats {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }

        .stats img {
            max-width: 100%;
            height: auto;
        }

        /* PHILOSOPHY */

        .quote {
            text-align: center;
            padding: 35px 15px;
            background: var(--surface);
            border-radius: 6px;
        }

        .quote h2 {
            color: var(--purple);
            font-size: 30px;
            margin-bottom: 10px;
        }

        .quote p {
            color: var(--muted);
            font-size: 11px;
        }

        /* FOOTER */

        footer {
            text-align: center;
            padding: 35px 15px;
            color: var(--muted);
            font-size: 10px;
        }

        footer strong {
            color: var(--blue);
        }

        /* RESPONSIVE */

        @media (max-width: 600px) {
            header {
                min-height: 300px;
            }

            .header-content h1 {
                letter-spacing: 6px;
            }

            nav .container {
                gap: 13px;
            }

            nav a {
                font-size: 9px;
            }

            section {
                padding: 45px 0;
            }

            .terminal-body {
                padding: 17px;
                font-size: 10px;
            }
        }
    </style>
</head>

<body>

    <!-- HEADER -->

    <header id="home">
        <div class="header-content">
            <h1>HAWSK</h1>
            <p class="subtitle">CODE · CREATE · EXPLORE</p>
            <p class="japanese">静かな夜、無限の可能性</p>
            <span class="status">CURRENTLY LEARNING</span>
        </div>
    </header>

    <!-- NAVIGATION -->

    <nav>
        <div class="container">
            <a href="#about">ABOUT</a>
            <a href="#interests">INTERESTS</a>
            <a href="#setup">SETUP</a>
            <a href="#stack">STACK</a>
            <a href="#projects">PROJECTS</a>
            <a href="#stats">STATS</a>
        </div>
    </nav>

    <main class="container">

        <!-- ABOUT -->

        <section id="about">
            <h2 class="section-title"><span>01.</span> ABOUT ME</h2>

            <div class="terminal">
                <div class="terminal-header">
                    <span class="dot red"></span>
                    <span class="dot yellow"></span>
                    <span class="dot green"></span>
                    <span style="margin-left: 8px;">hawsk@localhost: ~</span>
                </div>

                <div class="terminal-body">
                    <p><span class="prompt">hawsk@localhost</span>:<span class="command">~$</span> whoami</p>

                    <div class="output">
Name       : HAWSK
Age        : [YOUR AGE]
Location   : Brazil
Occupation : Student / Aspiring Developer
Interests  : Programming, Linux & Cybersecurity
Personality: Curious, creative and a little nerdy
Status     : Always learning...
                    </div>

                    <p><span class="prompt">hawsk@localhost</span>:<span class="command">~$</span> <span style="color:var(--green)">_</span></p>
                </div>
            </div>

            <br>

            <p class="about-text">
                Just a teenager who genuinely enjoys spending time in front
                of a computer. I love exploring code, learning new technologies,
                experimenting with Linux, customizing terminals and organizing
                every little detail of my digital environment.
                <br><br>
                I am interested in <span class="highlight">programming</span>,
                <span class="highlight">ethical hacking</span> and understanding
                how technology works behind the scenes.
                <br><br>
                Still learning. Still experimenting. Always curious.
            </p>
        </section>

        <!-- INTERESTS -->

        <section id="interests">
            <h2 class="section-title"><span>02.</span> INTERESTS</h2>

            <div class="interest-grid">

                <div class="interest-card">
                    <h3>01 / Programming</h3>
                    <p>Writing code, experimenting and building personal projects.</p>
                </div>

                <div class="interest-card">
                    <h3>02 / Cybersecurity</h3>
                    <p>Ethical hacking, digital security and understanding vulnerabilities.</p>
                </div>

                <div class="interest-card">
                    <h3>03 / Linux</h3>
                    <p>Exploring operating systems, shells and terminal environments.</p>
                </div>

                <div class="interest-card">
                    <h3>04 / Customization</h3>
                    <p>Dotfiles, themes, terminal configurations and organization.</p>
                </div>

                <div class="interest-card">
                    <h3>05 / Technology</h3>
                    <p>Discovering tools, understanding systems and learning new things.</p>
                </div>

                <div class="interest-card">
                    <h3>06 / Japan</h3>
                    <p>Japanese culture, Tokyo at night and urban aesthetics.</p>
                </div>

            </div>
        </section>

        <!-- SETUP -->

        <section id="setup">
            <h2 class="section-title"><span>03.</span> MY SETUP</h2>

            <div class="setup-list">
                <span class="folder">~/.hawsk</span><br>
                │<br>
                ├── projects/<br>
                │   ├── personal/<br>
                │   ├── experiments/<br>
                │   └── learning/<br>
                │<br>
                ├── configs/<br>
                │   ├── terminal/<br>
                │   ├── themes/<br>
                │   └── dotfiles/<br>
                │<br>
                ├── scripts/<br>
                │<br>
                └── README.md
            </div>

            <br>

            <p class="about-text">
                <span class="highlight">Terminal:</span> Termux<br>
                <span class="highlight">Editor:</span> VS Code<br>
                <span class="highlight">Shell:</span> Bash<br>
                <span class="highlight">Theme:</span> Tokyo Night
            </p>
        </section>

        <!-- TECH STACK -->

        <section id="stack">
            <h2 class="section-title"><span>04.</span> TECH STACK</h2>

            <p class="about-text" style="margin-bottom:25px;">
                Technologies I'm exploring and learning.
            </p>

            <div class="tech-stack">
                <img src="https://skillicons.dev/icons?i=python&theme=dark" alt="Python">
                <img src="https://skillicons.dev/icons?i=html&theme=dark" alt="HTML">
                <img src="https://skillicons.dev/icons?i=css&theme=dark" alt="CSS">
                <img src="https://skillicons.dev/icons?i=js&theme=dark" alt="JavaScript">
                <img src="https://skillicons.dev/icons?i=bash&theme=dark" alt="Bash">
                <img src="https://skillicons.dev/icons?i=linux&theme=dark" alt="Linux">
                <img src="https://skillicons.dev/icons?i=git&theme=dark" alt="Git">
                <img src="https://skillicons.dev/icons?i=github&theme=dark" alt="GitHub">
                <img src="https://skillicons.dev/icons?i=vscode&theme=dark" alt="VS Code">
            </div>
        </section>

        <!-- PROJECTS -->

        <section id="projects">
            <h2 class="section-title"><span>05.</span> PROJECTS</h2>

            <div class="project">
                <h3>project-01 / [YOUR PROJECT]</h3>
                <p>Write a short description of your project here.</p>
                <span class="project-status">● IN PROGRESS</span>
            </div>

            <div class="project">
                <h3>project-02 / [YOUR PROJECT]</h3>
                <p>Another personal experiment or programming project.</p>
                <span class="project-status">● LEARNING</span>
            </div>

            <div class="project">
                <h3>project-03 / [YOUR PROJECT]</h3>
                <p>A little idea that became something interesting.</p>
                <span class="project-status">● PLANNED</span>
            </div>

            <p style="text-align:center; margin-top:25px; font-size:12px;">
                <a href="https://github.com/USERNAME?tab=repositories">
                    [ EXPLORE MY REPOSITORIES ]
                </a>
            </p>
        </section>

        <!-- GITHUB STATS -->

        <section id="stats">
            <h2 class="section-title"><span>06.</span> GITHUB STATS</h2>

            <div class="stats">

                <img src="https://github-readme-stats.vercel.app/api?username=USERNAME&show_icons=true&hide_border=true&bg_color=1a1b26&title_color=7aa2f7&icon_color=bb9af7&text_color=c0caf5" alt="GitHub Statistics">

                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=USERNAME&layout=compact&hide_border=true&bg_color=1a1b26&title_color=7aa2f7&text_color=c0caf5" alt="Most Used Languages">

            </div>
        </section>

        <!-- PHILOSOPHY -->

        <section>
            <h2 class="section-title"><span>07.</span> PHILOSOPHY</h2>

            <div class="quote">
                <h2>学び続ける</h2>
                <p>MANABI TSUZUKERU</p>
                <br>
                <p>Never stop learning.</p>
                <br>
                <p>
                    "The best environment is the one you build yourself."
                </p>
            </div>
        </section>

    </main>

    <!-- FOOTER -->

    <footer>
        <p>Made with curiosity, coffee and too many terminal configurations.</p>
        <br>
        <strong>HAWSK</strong>
        <br>
        <p>© 2026 · Personal Profile</p>
        <br>
        <a href="#home">BACK TO TOP ↑</a>
    </footer>

</body>
</html>

