<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Maibam Rakesh Singh · Mathematician & Statistician</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Fira+Code:wght@400;500&display=swap" rel="stylesheet" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #080e08;
            font-family: 'Inter', -apple-system, sans-serif;
            color: #d4ecd4;
            padding: 1.5rem;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .profile-card {
            max-width: 1100px;
            width: 100%;
            background: radial-gradient(ellipse at 20% 30%, #102010, #0a120a 70%);
            border-radius: 3rem;
            padding: 2.5rem 2.2rem 2rem;
            box-shadow: 0 30px 60px rgba(0, 0, 0, 0.9), 0 0 0 1px #39ff1422, 0 0 60px #39ff1408;
            border: 1px solid #39ff1422;
            transition: all 0.3s ease;
        }

        /* ---- capsule header ---- */
        .wave-header {
            width: 100%;
            margin-bottom: 1.2rem;
            border-radius: 2rem 2rem 0 0;
            overflow: hidden;
            line-height: 0;
        }
        .wave-header img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* ---- identity ---- */
        .identity {
            text-align: center;
            margin: 1.5rem 0 0.8rem 0;
        }
        .identity h1 {
            font-size: 3.6rem;
            font-weight: 800;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #b0f0b0 0%, #39ff14 40%, #00e676 80%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 40px #39ff1422;
            margin-bottom: 0.2rem;
        }
        .identity .tagline {
            font-size: 1.2rem;
            font-weight: 300;
            color: #b8e0b8;
            letter-spacing: 3px;
        }
        .identity .tagline span {
            color: #39ff14;
            font-weight: 500;
        }
        .identity .tagline .bullet {
            color: #39ff1466;
            margin: 0 8px;
        }

        /* ---- typing area ---- */
        .typing-area {
            display: flex;
            justify-content: center;
            margin: 1.4rem 0 1.2rem;
        }
        .typing-pill {
            font-family: 'Fira Code', monospace;
            background: #0b160b;
            padding: 0.7rem 2.2rem;
            border-radius: 60px;
            border: 1px solid #39ff1433;
            box-shadow: 0 0 30px #39ff1408, inset 0 0 30px #00000044;
            color: #c8eac8;
            font-size: 1.05rem;
            font-weight: 400;
            display: inline-flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
            justify-content: center;
        }
        .typing-pill i {
            color: #39ff14;
            font-size: 1.1rem;
        }
        .typing-pill .dot {
            display: inline-block;
            width: 6px;
            height: 6px;
            background: #39ff14;
            border-radius: 50%;
            margin: 0 4px;
            animation: pulse-dot 1.6s infinite;
        }
        @keyframes pulse-dot {
            0%, 100% { opacity: 0.2; transform: scale(0.8); }
            50% { opacity: 1; transform: scale(1.2); }
        }

        /* ---- social badges ---- */
        .social-links {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.6rem 1.2rem;
            margin: 1.2rem 0 0.8rem;
        }
        .social-links a, .social-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            padding: 0.45rem 1.4rem;
            border-radius: 40px;
            background: #0f1a0f;
            color: #c8eac8;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            border: 1px solid #39ff1422;
            transition: all 0.25s ease;
        }
        .social-links a:hover {
            background: #1a2c1a;
            border-color: #39ff14;
            transform: translateY(-2px);
            box-shadow: 0 8px 24px #39ff1418;
            color: #f0fff0;
        }
        .social-links a i {
            color: #39ff14;
            font-size: 1.1rem;
        }
        .social-badge {
            background: #0b160b;
            cursor: default;
            border-color: #39ff1433;
        }
        .social-badge i {
            color: #39ff14;
        }

        hr.divider-light {
            border: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, #39ff1433, #39ff1466, #39ff1433, transparent);
            margin: 2rem 0 1.8rem;
        }

        /* ---- focus section ---- */
        .section-title {
            text-align: center;
            font-weight: 300;
            letter-spacing: 2px;
            color: #c0e0c0;
            margin-bottom: 1.2rem;
            font-size: 1.1rem;
            text-transform: uppercase;
        }
        .section-title i {
            color: #39ff14;
            margin-right: 10px;
        }

        .focus-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1rem;
        }
        .focus-card {
            background: #0b160bcc;
            backdrop-filter: blur(2px);
            border-radius: 24px;
            padding: 1.2rem 0.6rem;
            border: 1px solid #39ff1418;
            text-align: center;
            transition: 0.3s ease;
        }
        .focus-card:hover {
            border-color: #39ff1444;
            background: #102010cc;
            transform: scale(1.01);
            box-shadow: 0 0 30px #39ff1408;
        }
        .focus-card h4 {
            color: #d4f0d4;
            font-weight: 600;
            font-size: 1rem;
            letter-spacing: 0.5px;
            border-bottom: 1px solid #39ff1418;
            padding-bottom: 0.5rem;
            margin-bottom: 0.6rem;
        }
        .focus-card ul {
            list-style: none;
            padding: 0;
        }
        .focus-card ul li {
            font-size: 0.9rem;
            padding: 0.2rem 0;
            color: #c0e0c0;
            font-weight: 300;
            border-bottom: 1px solid #1a2a1a;
        }
        .focus-card ul li:last-child {
            border-bottom: none;
        }
        .focus-card ul li::before {
            content: "◆ ";
            color: #39ff14;
            font-size: 0.65rem;
            opacity: 0.7;
        }

        /* ---- tech stack ---- */
        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.6rem 1rem;
            margin: 0.8rem 0 0.2rem;
        }
        .tech-icons img {
            width: 52px;
            height: 52px;
            background: #0b160b;
            padding: 6px;
            border-radius: 16px;
            border: 1px solid #39ff1418;
            transition: 0.25s ease;
            filter: drop-shadow(0 0 6px #00000066);
        }
        .tech-icons img:hover {
            transform: scale(1.1) rotate(-2deg);
            border-color: #39ff14;
            filter: drop-shadow(0 0 20px #39ff1422);
        }

        /* ---- exploring pills ---- */
        .explore-pills {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.7rem 1.2rem;
            margin: 0.8rem 0 0.2rem;
        }
        .explore-pill {
            background: #0b160b;
            padding: 0.5rem 1.8rem;
            border-radius: 60px;
            border: 1px solid #39ff1422;
            font-weight: 500;
            font-size: 0.95rem;
            color: #c8eac8;
            transition: 0.25s ease;
            letter-spacing: 0.3px;
            box-shadow: 0 0 20px #00000033;
        }
        .explore-pill i {
            color: #39ff14;
            margin-right: 8px;
            font-size: 0.9rem;
        }
        .explore-pill:hover {
            background: #1a2c1a;
            border-color: #39ff14;
            transform: translateY(-3px);
            box-shadow: 0 10px 30px #39ff1418;
        }

        /* ---- quote + language stats ---- */
        .quote-block {
            background: #0b160bcc;
            backdrop-filter: blur(4px);
            padding: 1.2rem 2rem;
            border-radius: 60px;
            border-left: 4px solid #39ff14;
            border-right: 4px solid #39ff14;
            max-width: 780px;
            margin: 0 auto 1.8rem;
            text-align: center;
            font-size: 1.2rem;
            font-weight: 300;
            font-style: italic;
            color: #d4ecd4;
            box-shadow: 0 0 40px #39ff1408;
        }
        .quote-block i {
            color: #39ff14;
            opacity: 0.5;
            margin: 0 8px;
        }
        .quote-block strong {
            color: #39ff14;
            font-weight: 600;
            font-style: normal;
        }

        .lang-stats-box {
            background: #0b130b;
            border-radius: 28px;
            padding: 1.8rem 2rem 1.5rem;
            border: 1px solid #39ff1422;
            max-width: 720px;
            margin: 0 auto;
            box-shadow: 0 10px 30px #00000055;
        }
        .lang-stats-box .header-lang {
            display: flex;
            align-items: center;
            gap: 12px;
            color: #c0e0c0;
            font-weight: 400;
            border-bottom: 1px solid #1a2a1a;
            padding-bottom: 0.7rem;
            margin-bottom: 1rem;
        }
        .lang-stats-box .header-lang i {
            color: #39ff14;
            font-size: 1.5rem;
        }
        .lang-stats-box .header-lang small {
            font-weight: 300;
            color: #6a8a6a;
            margin-left: 6px;
            font-size: 0.8rem;
        }
        .lang-row {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            padding: 0.3rem 0;
            border-bottom: 1px solid #142414;
        }
        .lang-row:last-child {
            border-bottom: none;
        }
        .lang-name {
            width: 110px;
            font-weight: 400;
            color: #c8eac8;
            font-size: 0.95rem;
        }
        .lang-bar-track {
            flex: 1;
            height: 8px;
            background: #142414;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: inset 0 2px 6px #00000066;
        }
        .lang-bar-fill {
            height: 100%;
            border-radius: 20px;
            background: linear-gradient(90deg, #00c853, #39ff14, #76ff76);
            width: 0%;
            transition: width 0.8s cubic-bezier(0.2, 0.9, 0.3, 1.1);
            box-shadow: 0 0 12px #39ff1433;
        }
        .lang-percent {
            width: 75px;
            text-align: right;
            font-size: 0.85rem;
            color: #a0c0a0;
            font-weight: 400;
        }

        /* ---- mini stats ---- */
        .mini-stats {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.2rem 2.5rem;
            margin: 1.8rem 0 0.2rem;
        }
        .mini-stat {
            background: #0b160b;
            padding: 0.4rem 1.8rem;
            border-radius: 40px;
            border: 1px solid #39ff1418;
            text-align: center;
        }
        .mini-stat .num {
            font-size: 1.8rem;
            font-weight: 700;
            color: #39ff14;
            letter-spacing: 0.5px;
        }
        .mini-stat .lbl {
            font-size: 0.75rem;
            text-transform: uppercase;
            color: #6a8a6a;
            letter-spacing: 1px;
        }

        /* ---- footer ---- */
        .footer-credit {
            text-align: center;
            font-size: 0.8rem;
            color: #3a5a3a;
            margin-top: 2.2rem;
            padding-top: 1.2rem;
            border-top: 1px solid #1a2a1a;
            letter-spacing: 0.5px;
        }
        .footer-credit i {
            color: #39ff14;
            margin: 0 4px;
        }

        /* responsive */
        @media (max-width: 800px) {
            .profile-card { padding: 1.8rem 1.2rem; }
            .identity h1 { font-size: 2.6rem; }
            .focus-grid { grid-template-columns: 1fr; gap: 0.6rem; }
            .typing-pill { font-size: 0.9rem; padding: 0.5rem 1.2rem; }
            .lang-row { flex-wrap: wrap; gap: 0.1rem; }
            .lang-name { width: 80px; font-size: 0.85rem; }
            .lang-percent { width: 60px; }
            .quote-block { font-size: 1rem; padding: 1rem 1.2rem; }
        }
        @media (max-width: 480px) {
            .identity h1 { font-size: 2rem; }
            .identity .tagline { font-size: 0.9rem; }
            .tech-icons img { width: 42px; height: 42px; }
            .explore-pill { font-size: 0.8rem; padding: 0.3rem 1rem; }
            .social-links a { font-size: 0.75rem; padding: 0.3rem 0.8rem; }
        }
    </style>
</head>
<body>
<div class="profile-card">

    <!-- waving header -->
    <div class="wave-header">
        <img src="https://capsule-render.vercel.app/api?type=waving&height=170&section=header&color=0:006400,50:00C853,100:39FF14" alt="wave" />
    </div>

    <!-- identity -->
    <div class="identity">
        <h1>Maibam Rakesh Singh</h1>
        <div class="tagline">
            <span>Mathematician</span> <span class="bullet">•</span> 
            <span>Statistician</span> <span class="bullet">•</span> 
            <span>Applied Mathematician</span>
        </div>
    </div>

    <!-- typing area -->
    <div class="typing-area">
        <div class="typing-pill">
            <i class="fas fa-code"></i>
            Mathematics · Probability · Scientific ML · Random Matrix · Stochastic · Finance · Networks
            <span class="dot"></span><span class="dot" style="animation-delay:0.3s;"></span><span class="dot" style="animation-delay:0.6s;"></span>
        </div>
    </div>

    <!-- social -->
    <div class="social-links">
        <a href="https://github.com/maibamrakeshsingh" target="_blank"><i class="fab fa-github"></i> GitHub</a>
        <a href="https://www.linkedin.com/in/maibamrakeshsingh/" target="_blank"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
        <a href="mailto:maibamrakeshsingh31@gmail.com"><i class="fas fa-envelope"></i> Email</a>
        <span class="social-badge"><i class="fas fa-eye"></i> 1.2k views</span>
    </div>

    <hr class="divider-light" />

    <!-- research focus -->
    <div class="section-title"><i class="fas fa-flask"></i> Research Focus</div>
    <div class="focus-grid">
        <div class="focus-card">
            <h4>📐 Theory</h4>
            <ul>
                <li>Probability Theory</li>
                <li>Mathematical Statistics</li>
                <li>Statistical Inference</li>
                <li>Stochastic Calculus</li>
                <li>Random Matrix Theory</li>
            </ul>
        </div>
        <div class="focus-card">
            <h4>⚙️ Computation</h4>
            <ul>
                <li>Scientific Machine Learning</li>
                <li>Numerical Optimization</li>
                <li>High‑Performance Computing</li>
                <li>Scientific Computing</li>
                <li>Parallel Computing</li>
            </ul>
        </div>
        <div class="focus-card">
            <h4>📊 Applications</h4>
            <ul>
                <li>Financial Mathematics</li>
                <li>Complex Network Inference</li>
                <li>Statistical Physics</li>
                <li>Data Science</li>
                <li>Quantitative Finance</li>
            </ul>
        </div>
    </div>

    <hr class="divider-light" />

    <!-- tech stack -->
    <div class="section-title"><i class="fas fa-microchip"></i> Tech Stack</div>
    <div class="tech-icons">
        <img src="https://skillicons.dev/icons?i=python" alt="python" />
        <img src="https://skillicons.dev/icons?i=r" alt="R" />
        <img src="https://skillicons.dev/icons?i=c" alt="C" />
        <img src="https://skillicons.dev/icons?i=tensorflow" alt="tensorflow" />
        <img src="https://skillicons.dev/icons?i=pytorch" alt="pytorch" />
        <img src="https://skillicons.dev/icons?i=sklearn" alt="sklearn" />
        <img src="https://skillicons.dev/icons?i=docker" alt="docker" />
        <img src="https://skillicons.dev/icons?i=git" alt="git" />
        <img src="https://skillicons.dev/icons?i=mysql" alt="mysql" />
        <img src="https://skillicons.dev/icons?i=postgres" alt="postgres" />
        <img src="https://skillicons.dev/icons?i=vscode" alt="vscode" />
    </div>

    <hr class="divider-light" />

    <!-- currently exploring -->
    <div class="section-title"><i class="fas fa-compass"></i> Currently Exploring</div>
    <div class="explore-pills">
        <span class="explore-pill"><i class="fas fa-chart-line"></i> Probability Theory</span>
        <span class="explore-pill"><i class="fas fa-th"></i> Random Matrix Theory</span>
        <span class="explore-pill"><i class="fas fa-brain"></i> Scientific ML</span>
        <span class="explore-pill"><i class="fas fa-language"></i> Large Language Models</span>
        <span class="explore-pill"><i class="fas fa-microchip"></i> High‑Performance Computing</span>
    </div>

    <hr class="divider-light" />

    <!-- quote + language stats (the graph) -->
    <div class="quote-block">
        <i class="fas fa-quote-left"></i> 
        <strong>“Mathematics is the language of certainty, while statistics is the language of uncertainty”</strong>
        <i class="fas fa-quote-right"></i>
    </div>

    <div class="lang-stats-box">
        <div class="header-lang">
            <i class="fab fa-github-alt"></i> GitHub Language Statistics
            <small>· 17 repositories</small>
        </div>
        <!-- ASP -->
        <div class="lang-row">
            <span class="lang-name">ASP</span>
            <div class="lang-bar-track"><div class="lang-bar-fill" style="width: 0.667%;"></div></div>
            <span class="lang-percent">0.667%</span>
        </div>
        <!-- C# -->
        <div class="lang-row">
            <span class="lang-name">C#</span>
            <div class="lang-bar-track"><div class="lang-bar-fill" style="width: 16.333%;"></div></div>
            <span class="lang-percent">16.333%</span>
        </div>
        <!-- JavaScript -->
        <div class="lang-row">
            <span class="lang-name">JavaScript</span>
            <div class="lang-bar-track"><div class="lang-bar-fill" style="width: 71.492%;"></div></div>
            <span class="lang-percent">71.492%</span>
        </div>
        <!-- PowerShell -->
        <div class="lang-row">
            <span class="lang-name">PowerShell</span>
            <div class="lang-bar-track"><div class="lang-bar-fill" style="width: 1.058%;"></div></div>
            <span class="lang-percent">1.058%</span>
        </div>
        <!-- Python -->
        <div class="lang-row">
            <span class="lang-name">Python</span>
            <div class="lang-bar-track"><div class="lang-bar-fill" style="width: 7.652%;"></div></div>
            <span class="lang-percent">7.652%</span>
        </div>
        <!-- Ruby -->
        <div class="lang-row">
            <span class="lang-name">Ruby</span>
            <div class="lang-bar-track"><div class="lang-bar-fill" style="width: 1.457%;"></div></div>
            <span class="lang-percent">1.457%</span>
        </div>
        <!-- Other -->
        <div class="lang-row">
            <span class="lang-name">Other</span>
            <div class="lang-bar-track"><div class="lang-bar-fill" style="width: 1.141%;"></div></div>
            <span class="lang-percent">1.141%</span>
        </div>
    </div>

    <!-- mini stats -->
    <div class="mini-stats">
        <div class="mini-stat"><span class="num">17</span><div class="lbl">Repositories</div></div>
        <div class="mini-stat"><span class="num">1.2k</span><div class="lbl">Commits</div></div>
        <div class="mini-stat"><span class="num">8</span><div class="lbl">Followers</div></div>
    </div>

    <!-- footer -->
    <div class="footer-credit">
        <i class="fas fa-crown"></i> Maibam Rakesh Singh · Mathematics &amp; Statistics 
        <i class="fas fa-circle" style="font-size: 0.3rem; vertical-align: middle; margin: 0 6px; opacity: 0.3;"></i>
        built with <i class="fas fa-heart" style="color: #39ff14;"></i> for science
    </div>

</div>
</body>
</html>
