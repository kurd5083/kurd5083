<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Никита Курдияшко · Киберпанк Frontend</title>
    <link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;600;800&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: radial-gradient(circle at 20% 30%, #0a0f1e, #03050b);
            font-family: 'JetBrains Mono', monospace;
            padding: 2rem;
            color: #ccd6f6;
            line-height: 1.5;
            animation: fadeIn 1.2s cubic-bezier(0.2, 0.9, 0.4, 1.1);
        }

        @keyframes fadeIn {
            0% { opacity: 0; transform: translateY(20px); filter: blur(8px); }
            100% { opacity: 1; transform: translateY(0); filter: blur(0); }
        }

        .glow-text {
            text-shadow: 0 0 5px #0ff, 0 0 10px #0ff, 0 0 20px #0ff;
            animation: pulseGlow 2s infinite alternate;
        }

        @keyframes pulseGlow {
            0% { text-shadow: 0 0 2px cyan, 0 0 5px cyan; }
            100% { text-shadow: 0 0 12px cyan, 0 0 25px #0ff; }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: rgba(10, 20, 30, 0.45);
            backdrop-filter: blur(12px);
            border-radius: 48px;
            padding: 2rem 2rem 3rem;
            border: 1px solid rgba(0, 255, 255, 0.3);
            box-shadow: 0 0 40px rgba(0, 255, 255, 0.2), inset 0 1px 0 rgba(255, 255, 255, 0.1);
            transition: all 0.3s;
        }

        h1, h2, h3 {
            font-weight: 800;
            letter-spacing: -0.02em;
        }

        h1 {
            font-size: 4.2rem;
            background: linear-gradient(135deg, #fff, #0ff, #f0f);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            animation: glitch 3s infinite;
        }

        @keyframes glitch {
            0%, 100% { text-shadow: -2px 0 red, 2px 0 cyan; }
            25% { text-shadow: -3px 0 cyan, 3px 0 red; }
            50% { text-shadow: 2px 0 red, -2px 0 blue; }
            75% { text-shadow: -2px 0 lime, 2px 0 magenta; }
        }

        .badge-pulse {
            display: inline-block;
            transition: transform 0.2s ease, box-shadow 0.2s;
        }
        .badge-pulse:hover {
            transform: scale(1.07) translateY(-3px);
            filter: drop-shadow(0 0 12px cyan);
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            margin: 1.5rem 0;
        }

        .terminal-card {
            background: #0b1018e0;
            border-left: 4px solid #0ff;
            padding: 1.2rem;
            border-radius: 24px;
            margin: 1.2rem 0;
            transition: 0.25s;
            backdrop-filter: blur(8px);
        }
        .terminal-card:hover {
            border-left-color: magenta;
            box-shadow: 0 0 20px rgba(255, 0, 255, 0.3);
            transform: translateX(8px);
        }

        .code-line::before {
            content: ">";
            color: #0ff;
            font-weight: bold;
            margin-right: 12px;
            font-size: 1.2rem;
        }

        .grid-stats {
            display: flex;
            gap: 2rem;
            justify-content: center;
            flex-wrap: wrap;
            margin: 2rem 0;
        }

        .stat-bubble {
            background: #00000066;
            border-radius: 80px;
            padding: 0.6rem 1.4rem;
            border: 1px solid cyan;
            font-weight: bold;
            backdrop-filter: blur(4px);
        }

        hr {
            border: none;
            height: 2px;
            background: linear-gradient(90deg, cyan, magenta, cyan);
            margin: 2rem 0;
        }

        a {
            color: #0ff;
            text-decoration: none;
            transition: 0.2s;
        }
        a:hover {
            color: magenta;
            text-shadow: 0 0 5px magenta;
        }

        .matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
            opacity: 0.15;
            font-family: monospace;
            font-size: 14px;
            white-space: pre;
            overflow: hidden;
        }
        button {
            background: none;
            border: none;
            color: cyan;
            cursor: pointer;
        }
        .footer-stats {
            text-align: center;
            margin-top: 2rem;
            font-size: 0.8rem;
            color: #6c7a9e;
        }
        .blinking-cursor {
            animation: blink 1s step-end infinite;
        }
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
    </style>
</head>
<body>

<div class="matrix-bg" id="matrixRain"></div>

<div class="container">
    
    <div align="center">
        <h1>✦ НИКИТА КУРДИЯШКО ✦</h1>
        <p style="font-size: 1.5rem; font-weight: 600; letter-spacing: 2px;">
            <span class="glow-text">⚡ Middle Frontend Developer ⚡</span><br>
            <span style="font-size: 1rem;">React · Next.js · TypeScript</span>
        </p>
        <p>📍 Ростов-на-Дону &nbsp;•&nbsp; 🎂 22 года &nbsp;•&nbsp; 
            <a href="https://t.me/kurdnika" target="_blank">📱 @kurdnika</a>
        </p>
        <br>
        <div class="tech-stack" style="justify-content: center;">
            <a href="https://t.me/kurdnika" target="_blank" class="badge-pulse"><img src="https://img.shields.io/badge/Telegram-@kurdnika-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" /></a>
            <a href="mailto:nikitakurdiasko@gmail.com" class="badge-pulse"><img src="https://img.shields.io/badge/Email-nikitakurdiasko@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" /></a>
            <a href="https://github.com/kurd5083" target="_blank" class="badge-pulse"><img src="https://img.shields.io/badge/GitHub-kurd5083-181717?style=for-the-badge&logo=github&logoColor=white" /></a>
            <a href="https://portfoliokurdnika.netlify.app/" target="_blank" class="badge-pulse"><img src="https://img.shields.io/badge/Портфолио-portfolio.kurdnika.netlify.app-FF6B6B?style=for-the-badge&logo=netlify&logoColor=white" /></a>
        </div>
    </div>

    <hr>

    <div class="terminal-card">
        <div class="code-line"><span style="color:cyan;">$</span> <span style="color:#fff;">cat experience.txt</span></div>
        <p style="font-size: 1.7rem; font-weight: 800; margin: 0.5rem 0;">📊 3 года 10 месяцев</p>
        <p>коммерческой разработки · high‑load интерфейсы · AI‑фичи · кибернетическая надёжность</p>
    </div>

    <h2 style="border-left: 6px solid cyan; padding-left: 20px;">🛠 ТЕХНОЛОГИЧЕСКИЙ СТЕК</h2>

    <div class="tech-stack">
        <span class="badge-pulse"><img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Zustand-764ABC?style=for-the-badge&logo=react&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Redux_Toolkit-764ABC?style=for-the-badge&logo=redux&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/TanStack_Query-FF4154?style=for-the-badge&logo=react-query&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/TailwindCSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Styled_Components-DB7093?style=for-the-badge&logo=styled-components&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Vitest-6E9F18?style=for-the-badge&logo=vitest&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white" /></span>
        <span class="badge-pulse"><img src="https://img.shields.io/badge/FSD-0A0A0A?style=for-the-badge&logo=codefactor&logoColor=white" /></span>
    </div>

    <div class="terminal-card">
        <div class="code-line"><span style="color:lime;">// NEON PROTOCOL //</span></div>
        <p>🎯 <strong>Обо мне</strong><br>
        Моя главная цель — <span style="color:#0ff;">углубляться в React и экосистему</span>, писать масштабируемый код как произведение искусства. 
        В работе ценю <strong>прозрачные процессы + свободу</strong>.<br>
        🔥 <em>«Надёжный, задаю неудобные вопросы, довожу до конца»</em> 🔥
        </p>
    </div>

    <h2 style="border-left: 6px solid magenta; padding-left: 20px;">📈 КИБЕР-СТАТИСТИКА</h2>
    <div class="grid-stats">
        <div class="stat-bubble">✅ 30+ коммерческих проектов</div>
        <div class="stat-bubble">⚡ 90+ Lighthouse</div>
        <div class="stat-bubble">📦 Telegram Mini Apps SDK</div>
        <div class="stat-bubble">🎨 Кастомная SVG-аналитика</div>
    </div>

    <div align="center">
        <img src="https://github-readme-stats.vercel.app/api?username=kurd5083&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=61DAFB&icon_color=61DAFB&border_radius=20" width="48%" />
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kurd5083&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=61DAFB&border_radius=20" width="40%" />
    </div>

    <div align="center" style="margin: 2rem 0;">
        <div style="background: #000000aa; padding: 0.7rem 1.8rem; border-radius: 60px; display: inline-block; backdrop-filter: blur(8px); border: 1px solid cyan;">
            🧬 <strong>$ whoami</strong>  —  «строю реактивные интерфейсы, управляю состоянием как неоновая схема» 🧬
        </div>
    </div>

    <div class="footer-stats">
        <span>⚡ deploy частота: CI/CD оптимизирован ⚡</span>&nbsp;&nbsp;|&nbsp;&nbsp;
        <span>🛸 <span id="visitorCounter">👁️ profile views: 1337</span> 🛸</span>&nbsp;&nbsp;|&nbsp;&nbsp;
        <span class="blinking-cursor">_</span>
    </div>
</div>

<script>
    // MATRIX ДОЖДЬ ИЗ СИМВОЛОВ (киберпанк)
    const canvas = document.createElement('canvas');
    const matrixDiv = document.querySelector('.matrix-bg');
    matrixDiv.appendChild(canvas);
    canvas.style.position = 'fixed';
    canvas.style.top = '0';
    canvas.style.left = '0';
    canvas.style.width = '100%';
    canvas.style.height = '100%';
    canvas.style.pointerEvents = 'none';
    const ctx = canvas.getContext('2d');

    function resizeCanvas() {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
    }
    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    const chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789@#$%^&*(){}[]<>/\\|~`";
    const fontSize = 14;
    let columns = Math.floor(canvas.width / fontSize);
    let drops = Array(columns).fill(1);

    function drawMatrix() {
        ctx.fillStyle = "rgba(3, 5, 11, 0.05)";
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = "#0f6";
        ctx.font = `${fontSize}px 'JetBrains Mono'`;
        for (let i = 0; i < drops.length; i++) {
            const text = chars[Math.floor(Math.random() * chars.length)];
            ctx.fillText(text, i * fontSize, drops[i] * fontSize);
            if (drops[i] * fontSize > canvas.height && Math.random() > 0.975) {
                drops[i] = 0;
            }
            drops[i]++;
        }
    }
    setInterval(drawMatrix, 55);

    // Анимация счётчика просмотров
    let counter = 2842;
    setInterval(() => {
        counter += Math.floor(Math.random() * 3);
        document.getElementById('visitorCounter').innerHTML = `👁️ profile views: ${counter}`;
    }, 8000);
</script>
</body>
</html>
