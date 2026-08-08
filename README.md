<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <title>Maibam Rakesh Singh · Mathematician</title>
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    <!-- Google Fonts: Fira Code & Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;600&family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet" />
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0b0f0b;
            font-family: 'Inter', sans-serif;
            color: #d0e6d0;
            line-height: 1.6;
            padding: 2rem 1rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(18, 28, 18, 0.6);
            backdrop-filter: blur(2px);
            border-radius: 2.5rem;
            padding: 2.5rem 2rem;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.8), 0 0 0 1px #39ff1422;
            border: 1px solid #39ff1433;
        }

        /* ---- header waving (capsule) ---- */
        .capsule-header {
            width: 100%;
            margin-bottom: 1.5rem;
        }
        .capsule-header img {
            width: 100%;
            height: auto;
            display: block;
            border-radius: 2rem 2rem 0 0;
        }

        /* ---- name & subtitle ---- */
        .name-title {
            text-align: center;
            margin: 1.8rem 0 0.5rem 0;
        }
        .name-title h1 {
            font-size: 3.2rem;
            font-weight: 700;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #a0f0a0, #39ff14, #00c853);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-shadow: 0 0 20px #39ff1433;
        }
        .name-title .sub {
            font-size: 1.3rem;
            font-weight: 300;
            color: #b0e0b0;
            letter-spacing: 2px;
            margin-top: 0.2rem;
        }
        .name-title .sub span {
            color: #39ff14;
            font-weight: 400;
        }

        /* ---- typing SVG (we replicate with CSS + animation) ---- */
        .typing-wrapper {
            display: flex;
            justify-content: center;
            margin: 1.8rem 0 1.2rem 0;
        }
        .typing-box {
            font-family: 'Fira Code', monospace;
            font-size: 1.1rem;
            font-weight: 400;
            color: #b8e6b8;
            background: #0f1a0f;
            padding: 0.8rem 2rem;
            border-radius: 60px;
            border: 1px solid #39ff1455;
            box-shadow: 0 0 20px #39ff140d;
            display: inline-block;
            white-space: nowrap;
            overflow: hidden;
            max-width: 100%;
            text-overflow: ellipsis;
        }
        .typing-box i {
            color: #39ff14;
            margin-right: 10px;
        }

        /* ---- badges ---- */
        .badge-row {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.8rem 1.5rem;
            margin: 1.8rem 0 1.2rem 0;
        }
        .badge-row a {
            color: #d0e6d0;
            background: #1a2a1a;
            padding: 0.4rem 1.2rem;
            border-radius: 30px;
            text-decoration: none;
            font-size: 0.9rem;
            font-weight: 500;
            border: 1px solid #39ff1433;
            transition: 0.25s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }
        .badge-row a:hover {
            background: #2a402a;
            border-color: #39ff14;
            color: #eaffea;
            transform: scale(1.02);
            box-shadow: 0 0 18px #39ff1422;
        }
        .badge-row a i {
            color: #39ff14;
        }
        .badge-views {
            background: #0f1a0f;
            padding: 0.4rem 1.4rem;
            border-radius: 30px;
            border: 1px solid #39ff1444;
            font-size: 0.9rem;
            display: inline-flex;
            align-items: center;
            gap: 0.6rem;
        }
        .badge-views i {
            color: #39ff14;
        }

        hr.divider {
            border: 0;
            height: 1px;
            background: linear-gradient(90deg, transparent, #39ff1466, transparent);
            margin: 2.2rem 0;
        }

        /* ---- research focus (table style) ---- */
        .focus-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 0.2rem 1rem;
            text-align: center;
            margin: 1rem 0 0.5rem 0;
        }
        .focus-col {
            background: #0f1a0f;
            border-radius: 20px;
            padding: 0.8rem 0.5rem;
            border: 1px solid #39ff1422;
            transition: 0.2s;
        }
        .focus-col:hover {
            border-color: #39ff1466;
            background: #142414;
        }
        .focus-col h4 {
            color: #b8e6b8;
            font-weight: 600;
            letter-spacing: 0.5px;
            font-size: 1rem;
            border-bottom: 1px dashed #39ff1433;
            padding-bottom: 0.3rem;
            margin-bottom: 0.5rem;
        }
        .focus-col ul {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        .focus-col ul li {
            font-size: 0.9rem;
            padding: 0.2rem 0;
            color: #c8e6c8;
            font-weight: 300;
            border-bottom: 1px solid #39ff1408;
        }
        .focus-col ul li:last-child {
            border-bottom: none;
        }
        .focus-col ul li::before {
            content: "▹ ";
            color: #39ff14;
            font-weight: 400;
        }

        /* ---- tech stack (skill icons) ---- */
        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.8rem 1.2rem;
            margin: 1.2rem 0 0.8rem 0;
        }
        .tech-stack img {
            width: 48px;
            height: 48px;
            filter: drop-shadow(0 0 6px #39ff1433);
            transition: 0.2s;
            background: #0f1a0f;
            padding: 4px;
            border-radius: 12px;
        }
        .tech-stack img:hover {
            transform: scale(1.08);
            filter: drop-shadow(0 0 16px #39ff1466);
        }

        /* ---- currently exploring ---- */
        .explore-grid {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 0.8rem 1.2rem;
            margin: 1.2rem 0 0.2rem 0;
        }
        .explore-item {
            background: #0f1a0f;
            padding: 0.5rem 1.6rem;
            border-radius: 60px;
            border: 1px solid #39ff1444;
            color: #b8e6b8;
            font-weight: 500;
            font-size: 0.95rem;
            letter-spacing: 0.3px;
            transition: 0.2s;
            box-shadow: 0 0 10px #39ff1408;
        }
        .explore-item:hover {
            background: #1a2e1a;
            border-color: #39ff14;
            color: #eaffea;
            transform: scale(1.02);
            box-shadow: 0 0 28px #39ff1422;
        }
        .explore-item i {
            margin-right: 8px;
            color: #39ff14;
        }

        /* ---- quote + graph ---- */
        .quote-graph {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin: 2rem 0 0.5rem 0;
        }
        .quote-text {
            font-size: 1.3rem;
            font-weight: 300;
            font-style: italic;
            color: #d0e6d0;
            background: #0f1a0fcc;
            padding: 1rem 2.2rem;
            border-radius: 60px;
            border-left: 4px solid #39ff14;
            border-right: 4px solid #39ff14;
            text-align: center;
            max-width: 800px;
            margin-bottom: 2rem;
            backdrop-filter: blur(4px);
            box-shadow: 0 0 30px #39ff140d;
        }
        .quote-text strong {
            color: #39ff14;
            font-weight: 600;
        }

        /* ---- language stats (from the PNG) ---- */
        .lang-stats {
            background: #0b130b;
            border-radius: 28px;
            padding: 1.8rem 2rem;
            border: 1px solid #39ff1422;
            margin: 1.5rem 0 1rem 0;
            width: 100%;
            max-width: 700px;
        }
        .lang-stats h3 {
            display: flex;
            align-items: center;
            gap: 0.7rem;
            color: #b8e6b8;
            font-weight: 400;
            letter-spacing: 0.5px;
            border-bottom: 1px solid #39ff1422;
            padding-bottom: 0.6rem;
            margin-bottom: 1rem;
        }
        .lang-stats h3 i {
            color: #39ff14;
            font-size: 1.4rem;
        }
        .lang-stats h3 small {
            font-weight: 300;
            font-size: 0.8rem;
            color: #889f88;
            margin-left: 0.5rem;
        }
        .lang-row {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            padding: 0.25rem 0;
            border-bottom: 1px solid #1a2a1a;
        }
        .lang-row:last-child {
            border-bottom: none;
        }
        .lang-name {
            width: 100px;
            font-weight: 400;
            color: #c8e6c8;
            font-size: 0.95rem;
        }
        .lang-bar-bg {
            flex: 1;
            height: 8px;
            background: #1a2a1a;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: inset 0 0 4px #00000055;
        }
        .lang-bar-fill {
            height: 100%;
            border-radius: 20px;
            background: linear-gradient(90deg, #00c853, #39ff14);
            width: 0%;
            transition: width 0.6s ease;
        }
        .lang-percent {
            width: 70px;
            text-align: right;
            font-size: 0.85rem;
            color: #a0c0a0;
            font-weight: 400;
        }

        /* ---- GitHub stats placeholder (visual) ---- */
        .github-stats-placeholder {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1.5rem;
            margin: 2rem 0 0.5rem 0;
        }
        .stat-card {
            background: #0f1a0f;
            border-radius: 30px;
            padding: 0.8rem 2rem;
            border: 1px solid #39ff1422;
            text-align: center;
            min-width: 120px;
        }
        .stat-card .number {
            font-size: 1.8rem;
            font-weight: 700;
            color: #39ff14;
            letter-spacing: 0.5px;
        }
        .stat-card .label {
            font-size: 0.8rem;
            color: #889f88;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* ---- footer ---- */
        .footer-note {
            text-align: center;
            font-size: 0.8rem;
            color: #4a6a4a;
            margin-top: 2.5rem;
            border-top: 1px solid #1a2a1a;
            padding-top: 1.8rem;
            letter-spacing: 0.5px;
        }
        .footer-note i {
            color: #39ff14;
            margin: 0 4px;
        }

        /* responsive */
        @media (max-width: 700px) {
            .container { padding: 1.5rem 1rem; }
            .name-title h1 { font-size: 2.4rem; }
            .focus-grid { grid-template-columns: 1fr; gap: 0.6rem; }
            .typing-box { font-size: 0.9rem; padding: 0.5rem 1.2rem; white-space: normal; }
            .lang-row { flex-wrap: wrap; gap: 0.2rem; }
            .lang-name { width: 80px; }
            .lang-percent { width: 60px; }
            .badge-row a { font-size: 0.8rem; padding: 0.2rem 0.8rem; }
            .quote-text { font-size: 1rem; padding: 0.8rem 1.2rem; }
        }
        @media (max-width: 480px) {
            .name-title h1 { font-size: 1.8rem; }
            .tech-stack img { width: 38px; height: 38px; }
            .explore-item { font-size: 0.8rem; padding: 0.3rem 1rem; }
        }
    </style>
</head>
<body>
<div class="container">

    <!-- capsule header: waving -->
    <div class="capsule-header">
        <img src="https://capsule-render.vercel.app/api?type=waving&height=170&section=header&color=0:006400,50:00C853,100:39FF14" alt="waving header" />
    </div>

    <!-- name + title -->
    <div class="name-title">
        <h1>Maibam Rakesh Singh</h1>
        <div class="sub">✦ <span>Mathematician</span> · Statistician · Applied Mathematician ✦</div>
    </div>

    <!-- typing effect (simulated) -->
    <div class="typing-wrapper">
        <div class="typing-box">
            <i class="fas fa-terminal"></i> 
            Mathematics · Probability · Scientific ML · Random Matrix · Stochastic Calculus · Finance · Complex Networks
        </div>
    </div>

    <!-- badges -->
    <div class="badge-row">
        <a href="https://github.com/maibamrakeshsingh" target="_blank"><i class="fab fa-github"></i> GitHub</a>
        <a href="https://www.linkedin.com/in/maibamrakeshsingh/" target="_blank"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
        <a href="mailto:maibamrakeshsingh31@gmail.com"><i class="fas fa-envelope"></i> Email</a>
        <span class="badge-views"><i class="fas fa-eye"></i> Profile Views · 1.2k</span>
    </div>

    <hr class="divider" />

    <!-- research focus (3 cols) -->
    <div style="text-align: center; margin-bottom: 0.2rem;">
        <h3 style="font-weight: 300; letter-spacing: 2px; color: #b8e6b8;"><i class="fas fa-flask" style="color: #39ff14; margin-right: 10px;"></i>Research Focus</h3>
    </div>
    <div class="focus-grid">
        <div class="focus-col">
            <h4>📐 Theory</h4>
            <ul>
                <li>Probability Theory</li>
                <li>Mathematical Statistics</li>
                <li>Statistical Inference</li>
                <li>Stochastic Calculus</li>
                <li>Random Matrix Theory</li>
            </ul>
        </div>
        <div class="focus-col">
            <h4>⚙️ Computation</h4>
            <ul>
                <li>Scientific Machine Learning</li>
                <li>Numerical Optimization</li>
                <li>High‑Performance Computing</li>
                <li>Scientific Computing</li>
                <li>Parallel Computing</li>
            </ul>
        </div>
        <div class="focus-col">
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

    <hr class="divider" />

    <!-- Tech stack -->
    <div style="text-align: center; margin-bottom: 0.5rem;">
        <h3 style="font-weight: 300; letter-spacing: 2px; color: #b8e6b8;"><i class="fas fa-code" style="color: #39ff14; margin-right: 10px;"></i>Tech Stack</h3>
    </div>
    <div class="tech-stack">
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

    <hr class="divider" />

    <!-- Currently Exploring -->
    <div style="text-align: center; margin-bottom: 0.8rem;">
        <h3 style="font-weight: 300; letter-spacing: 2px; color: #b8e6b8;"><i class="fas fa-compass" style="color: #39ff14; margin-right: 10px;"></i>Currently Exploring</h3>
    </div>
    <div class="explore-grid">
        <span class="explore-item"><i class="fas fa-chart-line"></i> Probability Theory</span>
        <span class="explore-item"><i class="fas fa-th"></i> Random Matrix Theory</span>
        <span class="explore-item"><i class="fas fa-brain"></i> Scientific ML</span>
        <span class="explore-item"><i class="fas fa-language"></i> Large Language Models</span>
        <span class="explore-item"><i class="fas fa-microchip"></i> High‑Performance Computing</span>
    </div>

    <hr class="divider" />

    <!-- Quote + Graph (the requested "add this graph in codes") -->
    <div class="quote-graph">
        <div class="quote-text">
            <i class="fas fa-quote-left" style="color: #39ff14; opacity: 0.5; margin-right: 10px;"></i>
            <strong>“Mathematics is the language of certainty, while statistics is the language of uncertainty”</strong>
            <i class="fas fa-quote-right" style="color: #39ff14; opacity: 0.5; margin-left: 10px;"></i>
        </div>

        <!-- Language statistics table (exactly from the PNG) -->
        <div class="lang-stats">
            <h3>
                <i class="fab fa-github-alt"></i> GitHub Language Statistics 
                <small>· 17 repositories</small>
            </h3>
            <!-- ASP -->
            <div class="lang-row">
                <span class="lang-name">ASP</span>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="width: 0.667%;"></div></div>
                <span class="lang-percent">0.667%</span>
            </div>
            <!-- C# -->
            <div class="lang-row">
                <span class="lang-name">C#</span>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="width: 16.333%;"></div></div>
                <span class="lang-percent">16.333%</span>
            </div>
            <!-- JavaScript -->
            <div class="lang-row">
                <span class="lang-name">JavaScript</span>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="width: 71.492%;"></div></div>
                <span class="lang-percent">71.492%</span>
            </div>
            <!-- PowerShell -->
            <div class="lang-row">
                <span class="lang-name">PowerShell</span>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="width: 1.058%;"></div></div>
                <span class="lang-percent">1.058%</span>
            </div>
            <!-- Python -->
            <div class="lang-row">
                <span class="lang-name">Python</span>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="width: 7.652%;"></div></div>
                <span class="lang-percent">7.652%</span>
            </div>
            <!-- Ruby -->
            <div class="lang-row">
                <span class="lang-name">Ruby</span>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="width: 1.457%;"></div></div>
                <span class="lang-percent">1.457%</span>
            </div>
            <!-- Other -->
            <div class="lang-row">
                <span class="lang-name">Other</span>
                <div class="lang-bar-bg"><div class="lang-bar-fill" style="width: 1.141%;"></div></div>
                <span class="lang-percent">1.141%</span>
            </div>
        </div>
    </div>

    <!-- small GitHub stats (decorative) -->
    <div class="github-stats-placeholder">
        <div class="stat-card"><div class="number">17</div><div class="label">repos</div></div>
        <div class="stat-card"><div class="number">~ 1.2k</div><div class="label">commits</div></div>
        <div class="stat-card"><div class="number">8</div><div class="label">followers</div></div>
    </div>

    <hr class="divider" />

    <!-- footer -->
    <div class="footer-note">
        <i class="fas fa-crown"></i> Maibam Rakesh Singh · Mathematics &amp; Statistics · 
        <i class="fas fa-code"></i> with <i class="fas fa-heart" style="color: #39ff14;"></i> for science
    </div>

</div>
<!-- end container -->
</body>
</html>
