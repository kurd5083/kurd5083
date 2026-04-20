<svg width="100%" height="280" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="neonGradient" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" stop-color="#00ffff"/>
      <stop offset="50%" stop-color="#ff00ff"/>
      <stop offset="100%" stop-color="#00ffff"/>
    </linearGradient>
    <filter id="glow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>
  </defs>
  
  <foreignObject width="100%" height="100%">
    <div xmlns="http://www.w3.org/1999/xhtml">
      <style>
        * {
          margin: 0;
          padding: 0;
          box-sizing: border-box;
        }
        body {
          background: linear-gradient(135deg, #0a0f1e 0%, #03050b 100%);
          font-family: 'Courier New', 'Fira Code', monospace;
          padding: 2rem;
          border-radius: 24px;
          border: 1px solid rgba(0, 255, 255, 0.4);
          box-shadow: 0 0 30px rgba(0, 255, 255, 0.2);
        }
        .glitch {
          font-size: 3rem;
          font-weight: bold;
          background: linear-gradient(135deg, #fff, #0ff, #f0f);
          -webkit-background-clip: text;
          background-clip: text;
          color: transparent;
          animation: glitch 2s infinite;
          text-align: center;
        }
        @keyframes glitch {
          0%, 100% { text-shadow: -2px 0 red, 2px 0 cyan; }
          25% { text-shadow: -3px 0 cyan, 3px 0 red; }
          50% { text-shadow: 2px 0 red, -2px 0 blue; }
          75% { text-shadow: -2px 0 lime, 2px 0 magenta; }
        }
        .subtitle {
          text-align: center;
          color: #0ff;
          font-size: 1.2rem;
          margin: 1rem 0;
          letter-spacing: 2px;
          animation: pulse 1.5s infinite alternate;
        }
        @keyframes pulse {
          from { text-shadow: 0 0 2px cyan; opacity: 0.8; }
          to { text-shadow: 0 0 15px cyan; opacity: 1; }
        }
        .stats {
          display: flex;
          justify-content: center;
          gap: 2rem;
          margin-top: 1.5rem;
          flex-wrap: wrap;
        }
        .stat {
          background: rgba(0, 255, 255, 0.1);
          border: 1px solid cyan;
          border-radius: 40px;
          padding: 0.5rem 1.2rem;
          font-size: 0.85rem;
          color: #0ff;
        }
        .code-line {
          text-align: center;
          color: #6c7a9e;
          font-size: 0.75rem;
          margin-top: 1rem;
        }
        .code-line::before {
          content: ">";
          color: #0ff;
          margin-right: 8px;
        }
      </style>
      
      <div class="glitch">⚡ НИКИТА КУРДИЯШКО ⚡</div>
      <div class="subtitle">Middle Frontend Developer · React · Next.js · TypeScript</div>
      
      <div class="stats">
        <div class="stat">📊 3 года 10 месяцев</div>
        <div class="stat">🚀 90+ Lighthouse</div>
        <div class="stat">💻 30+ проектов</div>
        <div class="stat">🎨 Telegram Mini Apps</div>
      </div>
      
      <div class="code-line">system.status = "READY" | profile.optimized = true</div>
    </div>
  </foreignObject>
</svg>
