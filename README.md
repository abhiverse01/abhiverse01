<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abhishek Shah — GitHub README</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;500;600;700;800&family=Space+Mono:wght@400;700&family=Instrument+Serif:ital@0;1&display=swap" rel="stylesheet">
<style>
  :root {
    --void: #020408;
    --deep: #060d18;
    --panel: #0a1628;
    --surface: #0e1f38;
    --border: #1a3a6b;
    --glow: #1e5bff;
    --electric: #3b82f6;
    --cyan: #06d6ff;
    --aurora: #00ffcc;
    --plasma: #7c3aed;
    --gold: #f59e0b;
    --text: #e2eaf5;
    --muted: #6b8ab0;
    --dim: #2a4a7a;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--void);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    overflow-x: hidden;
    cursor: default;
  }

  /* ─── STAR FIELD ─── */
  #stars {
    position: fixed; inset: 0; z-index: 0; pointer-events: none;
    background:
      radial-gradient(1px 1px at 15% 25%, #fff6 0%, transparent 100%),
      radial-gradient(1px 1px at 72% 10%, #fff4 0%, transparent 100%),
      radial-gradient(1px 1px at 40% 80%, #fff5 0%, transparent 100%),
      radial-gradient(1px 1px at 88% 55%, #fff3 0%, transparent 100%),
      radial-gradient(1px 1px at 5%  90%, #fff4 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 60% 35%, #06d6ff33 0%, transparent 100%),
      radial-gradient(1.5px 1.5px at 30% 60%, #3b82f633 0%, transparent 100%);
  }

  /* ─── NEBULA BG ─── */
  .nebula {
    position: fixed; inset: 0; z-index: 0; pointer-events: none;
    background:
      radial-gradient(ellipse 80% 60% at 10% 20%, #1e5bff08 0%, transparent 60%),
      radial-gradient(ellipse 60% 40% at 90% 80%, #7c3aed08 0%, transparent 60%),
      radial-gradient(ellipse 40% 50% at 50% 50%, #06d6ff05 0%, transparent 70%);
  }

  .page {
    position: relative; z-index: 1;
    max-width: 900px;
    margin: 0 auto;
    padding: 0 24px 80px;
  }

  /* ─── HERO BANNER ─── */
  .hero {
    position: relative;
    margin-bottom: 60px;
    padding: 70px 0 50px;
    text-align: center;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, #1e5bff12 0%, #7c3aed10 50%, #06d6ff08 100%);
    border-bottom: 1px solid var(--border);
  }

  .hero-ring {
    position: absolute;
    border-radius: 50%;
    border: 1px solid;
    top: 50%; left: 50%;
    transform: translate(-50%, -50%);
    animation: pulse-ring 4s ease-in-out infinite;
  }
  .hero-ring:nth-child(1) { width: 300px; height: 300px; border-color: #1e5bff15; animation-delay: 0s; }
  .hero-ring:nth-child(2) { width: 500px; height: 500px; border-color: #1e5bff0d; animation-delay: 1s; }
  .hero-ring:nth-child(3) { width: 700px; height: 700px; border-color: #1e5bff08; animation-delay: 2s; }

  @keyframes pulse-ring {
    0%, 100% { opacity: 0.4; transform: translate(-50%, -50%) scale(1); }
    50% { opacity: 1; transform: translate(-50%, -50%) scale(1.03); }
  }

  .hero-eyebrow {
    font-size: 10px;
    letter-spacing: 6px;
    color: var(--cyan);
    text-transform: uppercase;
    margin-bottom: 18px;
    position: relative;
    animation: fadein 0.8s ease both;
  }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(42px, 8vw, 78px);
    font-weight: 800;
    line-height: 1;
    letter-spacing: -2px;
    position: relative;
    margin-bottom: 16px;
    animation: fadein 0.9s ease both 0.1s;
    background: linear-gradient(135deg, #e2eaf5 0%, #06d6ff 40%, #3b82f6 70%, #7c3aed 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .hero-title {
    font-size: 12px;
    letter-spacing: 4px;
    color: var(--muted);
    text-transform: uppercase;
    position: relative;
    margin-bottom: 28px;
    animation: fadein 1s ease both 0.2s;
  }

  .hero-title span {
    color: var(--aurora);
    -webkit-text-fill-color: var(--aurora);
  }

  .hero-quote {
    font-family: 'Instrument Serif', serif;
    font-style: italic;
    font-size: 16px;
    color: var(--muted);
    position: relative;
    max-width: 400px;
    margin: 0 auto 36px;
    animation: fadein 1.1s ease both 0.3s;
  }

  .hero-quote::before, .hero-quote::after {
    content: '"';
    color: var(--electric);
    font-size: 24px;
    line-height: 0;
    vertical-align: -6px;
  }

  .status-pill {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    background: linear-gradient(90deg, #1e5bff18, #06d6ff10);
    border: 1px solid var(--border);
    border-radius: 100px;
    padding: 8px 18px;
    font-size: 10px;
    letter-spacing: 2px;
    text-transform: uppercase;
    color: var(--cyan);
    position: relative;
    animation: fadein 1.2s ease both 0.4s;
  }

  .status-dot {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--aurora);
    box-shadow: 0 0 8px var(--aurora);
    animation: blink 1.5s ease-in-out infinite;
  }

  @keyframes blink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.3; }
  }

  @keyframes fadein {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* ─── SECTION HEADERS ─── */
  .section-header {
    display: flex;
    align-items: center;
    gap: 14px;
    margin-bottom: 28px;
    margin-top: 56px;
  }

  .section-header .label {
    font-family: 'Syne', sans-serif;
    font-size: 20px;
    font-weight: 700;
    color: var(--text);
    letter-spacing: -0.5px;
  }

  .section-header .tag {
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--cyan);
    padding: 3px 10px;
    border: 1px solid #06d6ff30;
    border-radius: 4px;
  }

  .section-line {
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ─── ABOUT GRID ─── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .about-card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 22px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, transform 0.3s;
  }

  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--glow), var(--cyan));
    opacity: 0;
    transition: opacity 0.3s;
  }

  .about-card:hover { border-color: var(--electric); transform: translateY(-2px); }
  .about-card:hover::before { opacity: 1; }

  .about-card .card-icon {
    font-size: 22px; margin-bottom: 10px;
  }

  .about-card .card-label {
    font-size: 9px;
    letter-spacing: 3px;
    text-transform: uppercase;
    color: var(--cyan);
    margin-bottom: 8px;
  }

  .about-card .card-value {
    font-size: 13px;
    color: var(--text);
    line-height: 1.6;
  }

  .about-card .card-value a {
    color: var(--electric);
    text-decoration: none;
    transition: color 0.2s;
  }
  .about-card .card-value a:hover { color: var(--cyan); }

  /* ─── CONNECT ROW ─── */
  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 20px;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 18px;
    border: 1px solid var(--border);
    border-radius: 8px;
    background: var(--panel);
    color: var(--muted);
    font-size: 11px;
    letter-spacing: 1px;
    text-decoration: none;
    transition: all 0.25s;
    font-family: 'Space Mono', monospace;
  }

  .connect-btn:hover {
    border-color: var(--electric);
    color: var(--electric);
    background: #1e5bff10;
    box-shadow: 0 0 16px #1e5bff20;
  }

  .connect-btn svg {
    width: 14px; height: 14px;
    fill: currentColor;
  }

  /* ─── SKILLS GRID ─── */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(88px, 1fr));
    gap: 12px;
  }

  .skill-cell {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px 8px;
    text-align: center;
    transition: all 0.25s;
    cursor: default;
  }

  .skill-cell:hover {
    border-color: var(--electric);
    background: var(--surface);
    transform: translateY(-3px);
    box-shadow: 0 8px 24px #1e5bff18;
  }

  .skill-cell img {
    width: 36px; height: 36px;
    object-fit: contain;
    margin-bottom: 8px;
    filter: brightness(0.9) saturate(1.1);
    transition: filter 0.25s;
  }

  .skill-cell:hover img { filter: brightness(1.1) saturate(1.3); }

  .skill-cell span {
    display: block;
    font-size: 9px;
    letter-spacing: 1px;
    color: var(--muted);
    text-transform: uppercase;
  }

  /* ─── LLM TAGS ─── */
  .llm-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }

  .llm-tag {
    padding: 8px 16px;
    border-radius: 8px;
    font-size: 11px;
    letter-spacing: 2px;
    text-transform: uppercase;
    font-weight: 700;
    border: 1px solid;
  }

  .llm-tag.blue { background: #1e5bff15; border-color: #1e5bff40; color: #60a5fa; }
  .llm-tag.purple { background: #7c3aed15; border-color: #7c3aed40; color: #a78bfa; }
  .llm-tag.green { background: #00ffcc10; border-color: #00ffcc30; color: #34d399; }
  .llm-tag.gold { background: #f59e0b10; border-color: #f59e0b30; color: #fbbf24; }
  .llm-tag.red { background: #ef444415; border-color: #ef444430; color: #f87171; }
  .llm-tag.cyan { background: #06d6ff10; border-color: #06d6ff30; color: #22d3ee; }

  /* ─── TECH PILLS ─── */
  .tech-cloud {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }

  .tech-pill {
    padding: 6px 14px;
    border-radius: 6px;
    font-size: 10px;
    letter-spacing: 1px;
    color: var(--muted);
    border: 1px solid var(--dim);
    background: #0a1628;
    transition: all 0.2s;
    text-transform: uppercase;
  }

  .tech-pill:hover {
    color: var(--text);
    border-color: var(--electric);
    background: #1e5bff12;
  }

  /* ─── STAT CARDS ─── */
  .stat-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
  }

  .stat-card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    padding: 6px;
  }

  .stat-card img {
    width: 100%;
    border-radius: 8px;
    display: block;
    filter: brightness(1.05) saturate(0.9) hue-rotate(10deg);
  }

  /* ─── TIMELINE ─── */
  .timeline {
    position: relative;
    padding-left: 28px;
  }

  .timeline::before {
    content: '';
    position: absolute;
    left: 6px; top: 6px; bottom: 6px;
    width: 1px;
    background: linear-gradient(to bottom, var(--glow), var(--plasma), transparent);
  }

  .timeline-item {
    position: relative;
    margin-bottom: 24px;
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 18px 20px;
    transition: border-color 0.25s;
  }

  .timeline-item:hover { border-color: var(--electric); }

  .timeline-item::before {
    content: '';
    position: absolute;
    left: -24px;
    top: 18px;
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--glow);
    box-shadow: 0 0 10px var(--glow);
    border: 2px solid var(--void);
  }

  .tl-title {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    font-size: 14px;
    color: var(--text);
    margin-bottom: 6px;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .tl-badge {
    font-size: 9px;
    letter-spacing: 2px;
    text-transform: uppercase;
    padding: 2px 8px;
    border-radius: 4px;
    border: 1px solid var(--border);
    color: var(--muted);
  }

  .tl-desc {
    font-size: 11px;
    color: var(--muted);
    line-height: 1.7;
  }

  /* ─── CERT GRID ─── */
  .cert-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
  }

  .cert-card {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 16px;
    transition: border-color 0.25s;
  }

  .cert-card:hover { border-color: var(--electric); }

  .cert-title {
    font-family: 'Syne', sans-serif;
    font-size: 12px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 6px;
  }

  .cert-meta {
    font-size: 10px;
    color: var(--muted);
    line-height: 1.6;
  }

  .cert-issuer {
    color: var(--electric);
    font-size: 10px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-top: 6px;
    display: inline-block;
  }

  /* ─── FOOTER ─── */
  .footer {
    margin-top: 70px;
    padding-top: 32px;
    border-top: 1px solid var(--border);
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-copy {
    font-size: 10px;
    color: var(--dim);
    letter-spacing: 2px;
    text-transform: uppercase;
  }

  .footer-copy span {
    color: var(--electric);
  }

  /* ─── SCROLLBAR ─── */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: var(--void); }
  ::-webkit-scrollbar-thumb { background: var(--border); border-radius: 4px; }

  /* ─── DIVIDER ─── */
  .divider {
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
    margin: 48px 0;
  }

  /* GITHUB STREAK embedded */
  .contrib-block {
    background: var(--panel);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 4px;
    overflow: hidden;
  }

  .contrib-block img {
    width: 100%;
    border-radius: 8px;
    filter: hue-rotate(10deg) brightness(1.1);
  }

  /* Scan line overlay */
  .scanlines {
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
    background: repeating-linear-gradient(
      0deg,
      transparent,
      transparent 2px,
      #00000008 2px,
      #00000008 4px
    );
  }

  /* Section number label */
  .sec-num {
    font-size: 9px;
    letter-spacing: 2px;
    color: var(--dim);
    margin-bottom: 4px;
    font-family: 'Space Mono', monospace;
  }
</style>
</head>
<body>

<div id="stars"></div>
<div class="nebula"></div>
<div class="scanlines"></div>

<div class="page">

  <!-- ═══ HERO ═══ -->
  <div class="hero">
    <div class="hero-ring"></div>
    <div class="hero-ring"></div>
    <div class="hero-ring"></div>
    <p class="hero-eyebrow">// system online — profile loaded</p>
    <h1 class="hero-name">Abhishek Shah</h1>
    <p class="hero-title">AI/ML Engineer &nbsp;·&nbsp; <span>Project Manager</span> &nbsp;·&nbsp; Explorer</p>
    <p class="hero-quote">Live, Become, Rise!</p>
    <div class="status-pill">
      <div class="status-dot"></div>
      Available for collaboration
    </div>
  </div>

  <!-- ═══ ABOUT ═══ -->
  <div class="sec-num">01 / 07</div>
  <div class="section-header">
    <span class="label">About Me</span>
    <span class="tag">Identity</span>
    <div class="section-line"></div>
  </div>

  <div class="about-grid">
    <div class="about-card">
      <div class="card-icon">🔭</div>
      <div class="card-label">Current Work</div>
      <div class="card-value">Agentic Research AI at <a href="https://papersupe.github.io/papersupe-web/index.html">PaperSupe</a> + Open Source Projects</div>
    </div>
    <div class="about-card">
      <div class="card-icon">🧪</div>
      <div class="card-label">Previous Work</div>
      <div class="card-value">RS Systems at <a href="https://inflancer.com">Inflancer Technology</a></div>
    </div>
    <div class="about-card">
      <div class="card-icon">🌱</div>
      <div class="card-label">Currently Learning</div>
      <div class="card-value">Advanced AI Engineering & MLOps</div>
    </div>
    <div class="about-card">
      <div class="card-icon">👯</div>
      <div class="card-label">Collaboration</div>
      <div class="card-value">Python · R · Django · Flask · AI · ML · NLP · LLMs</div>
    </div>
    <div class="about-card">
      <div class="card-icon">👀</div>
      <div class="card-label">Interests</div>
      <div class="card-value">Artificial Intelligence · DevOps · Code · The Cosmos</div>
    </div>
    <div class="about-card">
      <div class="card-icon">🤖</div>
      <div class="card-label">Robotics Org</div>
      <div class="card-value"><a href="https://github.com/abhiverse-org">abhiverse-robotics</a> — autonomous systems, RPA & simulations</div>
    </div>
  </div>

  <!-- Connect -->
  <div class="connect-row">
    <a class="connect-btn" href="https://github.com/abhiverse01?tab=repositories">
      <svg viewBox="0 0 24 24"><path d="M12 .5C5.37.5 0 5.87 0 12.5c0 5.31 3.44 9.8 8.21 11.4.6.1.82-.26.82-.58 0-.28-.01-1.02-.02-2-3.34.72-4.05-1.61-4.05-1.61-.55-1.39-1.34-1.76-1.34-1.76-1.09-.74.08-.73.08-.73 1.2.08 1.84 1.24 1.84 1.24 1.07 1.83 2.8 1.3 3.49 1 .11-.78.42-1.3.76-1.6-2.67-.3-5.47-1.33-5.47-5.93 0-1.31.47-2.38 1.24-3.22-.14-.3-.54-1.52.1-3.18 0 0 1.01-.32 3.3 1.23a11.5 11.5 0 0 1 3-.4 11.5 11.5 0 0 1 3 .4c2.28-1.55 3.3-1.23 3.3-1.23.64 1.66.24 2.88.12 3.18.77.84 1.23 1.91 1.23 3.22 0 4.61-2.81 5.63-5.48 5.92.43.37.81 1.1.81 2.22 0 1.6-.01 2.9-.01 3.29 0 .32.21.69.82.57C20.56 22.3 24 17.8 24 12.5 24 5.87 18.63.5 12 .5z"/></svg>
      GitHub
    </a>
    <a class="connect-btn" href="https://linkedin.com/in/theabhishekshah">
      <svg viewBox="0 0 24 24"><path d="M20.45 20.45h-3.55v-5.57c0-1.33-.03-3.04-1.85-3.04-1.86 0-2.14 1.45-2.14 2.95v5.66H9.35V9h3.41v1.56h.05a3.74 3.74 0 0 1 3.37-1.85c3.6 0 4.27 2.37 4.27 5.45v6.29zM5.34 7.43a2.06 2.06 0 1 1 0-4.12 2.06 2.06 0 0 1 0 4.12zm1.78 13.02H3.56V9h3.56v11.45zM22.23 0H1.77C.8 0 0 .77 0 1.73v20.54C0 23.23.8 24 1.77 24h20.46C23.2 24 24 23.23 24 22.27V1.73C24 .77 23.2 0 22.23 0z"/></svg>
      LinkedIn
    </a>
    <a class="connect-btn" href="https://medium.com/@abhiverse01">
      <svg viewBox="0 0 24 24"><path d="M13.54 12a6.8 6.8 0 0 1-6.77 6.82A6.8 6.8 0 0 1 0 12a6.8 6.8 0 0 1 6.77-6.82A6.8 6.8 0 0 1 13.54 12zm7.42 0c0 3.54-1.51 6.42-3.38 6.42s-3.39-2.88-3.39-6.42 1.52-6.42 3.39-6.42 3.38 2.88 3.38 6.42M24 12c0 3.17-.53 5.75-1.19 5.75-.66 0-1.19-2.58-1.19-5.75s.53-5.75 1.19-5.75C23.47 6.25 24 8.83 24 12z"/></svg>
      Medium
    </a>
    <a class="connect-btn" href="https://abhishekshah.vercel.app">
      <svg viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 17.93c-3.95-.49-7-3.85-7-7.93 0-.62.08-1.21.21-1.79L9 15v1c0 1.1.9 2 2 2v1.93zm6.9-2.54c-.26-.81-1-1.39-1.9-1.39h-1v-3c0-.55-.45-1-1-1H8v-2h2c.55 0 1-.45 1-1V7h2c1.1 0 2-.9 2-2v-.41c2.93 1.19 5 4.06 5 7.41 0 2.08-.8 3.97-2.1 5.39z"/></svg>
      Portfolio
    </a>
    <a class="connect-btn" href="mailto:abhishekshah007@gmail.com">
      <svg viewBox="0 0 24 24"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.909 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
      Email
    </a>
    <a class="connect-btn" href="https://abhishekshahhtmlresume.vercel.app">
      <svg viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8l-6-6zm4 18H6V4h7v5h5v11z"/></svg>
      Resume
    </a>
  </div>

  <div class="divider"></div>

  <!-- ═══ TOOLS ═══ -->
  <div class="sec-num">02 / 07</div>
  <div class="section-header">
    <span class="label">Languages & Tools</span>
    <span class="tag">Stack</span>
    <div class="section-line"></div>
  </div>

  <div class="skills-grid">
    <div class="skill-cell"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" /><span>Python</span></div>
    <div class="skill-cell"><img src="https://www.vectorlogo.zone/logos/pytorch/pytorch-icon.svg" /><span>PyTorch</span></div>
    <div class="skill-cell"><img src="https://www.vectorlogo.zone/logos/tensorflow/tensorflow-icon.svg" /><span>TensorFlow</span></div>
    <div class="skill-cell"><img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" /><span>Sklearn</span></div>
    <div class="skill-cell"><img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" /><span>Pandas</span></div>
    <div class="skill-cell"><img src="https://seaborn.pydata.org/_images/logo-mark-lightbg.svg" /><span>Seaborn</span></div>
    <div class="skill-cell"><img src="https://www.vectorlogo.zone/logos/opencv/opencv-icon.svg" /><span>OpenCV</span></div>
    <div class="skill-cell"><img src="https://cdn.worldvectorlogo.com/logos/django.svg" /><span>Django</span></div>
    <div class="skill-cell"><img src="https://www.vectorlogo.zone/logos/pocoo_flask/pocoo_flask-icon.svg" /><span>Flask</span></div>
    <div class="skill-cell"><img src="https://www.vectorlogo.zone/logos/google_cloud/google_cloud-icon.svg" /><span>GCP</span></div>
    <div class="skill-cell"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" /><span>MySQL</span></div>
    <div class="skill-cell"><img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" /><span>C++</span></div>
  </div>

  <!-- ═══ LLMs ═══ -->
  <div class="section-header" style="margin-top:36px;">
    <span class="label">LLMs Worked With</span>
    <span class="tag">AI</span>
    <div class="section-line"></div>
  </div>

  <div class="llm-tags">
    <span class="llm-tag blue">Llama</span>
    <span class="llm-tag cyan">DistilBERT</span>
    <span class="llm-tag gold">Flan-T5</span>
    <span class="llm-tag red">GroQ</span>
    <span class="llm-tag purple">Salesforce</span>
    <span class="llm-tag green">TinyLlama</span>
  </div>

  <!-- ═══ TECH ═══ -->
  <div class="section-header" style="margin-top:36px;">
    <span class="label">Technologies Mastered</span>
    <span class="tag">Ecosystem</span>
    <div class="section-line"></div>
  </div>

  <div class="tech-cloud">
    <span class="tech-pill">JavaScript</span>
    <span class="tech-pill">React</span>
    <span class="tech-pill">Node.js</span>
    <span class="tech-pill">Redux</span>
    <span class="tech-pill">Vite</span>
    <span class="tech-pill">TailwindCSS</span>
    <span class="tech-pill">FastAPI</span>
    <span class="tech-pill">GraphQL</span>
    <span class="tech-pill">MongoDB</span>
    <span class="tech-pill">PostgreSQL</span>
    <span class="tech-pill">Docker</span>
    <span class="tech-pill">Git</span>
    <span class="tech-pill">GitHub Actions</span>
    <span class="tech-pill">Nginx</span>
    <span class="tech-pill">Cloudflare</span>
    <span class="tech-pill">DigitalOcean</span>
    <span class="tech-pill">Netlify</span>
    <span class="tech-pill">Keras</span>
    <span class="tech-pill">NumPy</span>
    <span class="tech-pill">Matplotlib</span>
    <span class="tech-pill">Sequelize</span>
    <span class="tech-pill">JWT</span>
    <span class="tech-pill">Figma</span>
    <span class="tech-pill">Adobe Illustrator</span>
    <span class="tech-pill">Premiere Pro</span>
    <span class="tech-pill">Photoshop</span>
    <span class="tech-pill">Jira</span>
    <span class="tech-pill">GitLab</span>
  </div>

  <div class="divider"></div>

  <!-- ═══ STATS ═══ -->
  <div class="sec-num">03 / 07</div>
  <div class="section-header">
    <span class="label">GitHub Stats</span>
    <span class="tag">Metrics</span>
    <div class="section-line"></div>
  </div>

  <div class="stat-row">
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api/top-langs?username=abhiverse01&locale=en&hide_title=false&layout=compact&card_width=320&hide_border=true&theme=github_dark&bg_color=0a1628&title_color=3b82f6&text_color=6b8ab0" alt="Top Languages" />
    </div>
    <div class="stat-card">
      <img src="https://github-readme-stats.vercel.app/api?username=abhiverse01&hide_title=false&hide_rank=false&show_icons=true&count_private=true&disable_animations=false&locale=en&hide_border=true&theme=github_dark&bg_color=0a1628&title_color=3b82f6&icon_color=06d6ff&text_color=6b8ab0" alt="GitHub Stats" />
    </div>
  </div>

  <div style="margin-top: 16px;" class="contrib-block">
    <img src="https://streak-stats.demolab.com?user=abhiverse01&card_width=860&hide_border=true&theme=github-dark-blue&background=0a1628&ring=3b82f6&fire=06d6ff&currStreakLabel=3b82f6" alt="GitHub Streak" />
  </div>

  <div class="divider"></div>

  <!-- ═══ HIGHLIGHTS ═══ -->
  <div class="sec-num">04 / 07</div>
  <div class="section-header">
    <span class="label">Achievements & Highlights</span>
    <span class="tag">Timeline</span>
    <div class="section-line"></div>
  </div>

  <div class="timeline">
    <div class="timeline-item">
      <div class="tl-title">🏆 ACES-Deltathon 2023 <span class="tl-badge">Hackathon</span></div>
      <div class="tl-desc">Participated in a national-level software hackathon, showcasing problem-solving and innovation skills.</div>
    </div>
    <div class="timeline-item">
      <div class="tl-title">🦸 AI/ML Bootcamp 2023 <span class="tl-badge">Mentorship</span></div>
      <div class="tl-desc">Served as ML Sub-Mentor — trained the next generation of AI/ML enthusiasts at the AI/ML Bootcamp.</div>
    </div>
    <div class="timeline-item">
      <div class="tl-title">🏗️ Delta Afterevents <span class="tl-badge">Kaggle</span></div>
      <div class="tl-desc">Hosted a data science competition on Kaggle, encouraging participation and learning in the data science community.</div>
    </div>
    <div class="timeline-item">
      <div class="tl-title">📦 Project Mirror <span class="tl-badge">Android</span></div>
      <div class="tl-desc">Developed an Android package for screen mirroring on desktops, addressing key user needs in the tech community.</div>
    </div>
    <div class="timeline-item">
      <div class="tl-title">📕 ML Learning Resource Repo <span class="tl-badge">Open Source</span></div>
      <div class="tl-desc">Building and upgrading an ML resource repository on GitHub — covering concepts, projects, and tips for beginners and experts.</div>
    </div>
    <div class="timeline-item">
      <div class="tl-title">🌍 Open Source Contributions <span class="tl-badge">Community</span></div>
      <div class="tl-desc">Actively contributing to several open-source projects, continuously learning, and giving back to the community.</div>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ═══ CERTIFICATIONS ═══ -->
  <div class="sec-num">05 / 07</div>
  <div class="section-header">
    <span class="label">Licenses & Certifications</span>
    <span class="tag">Credentials</span>
    <div class="section-line"></div>
  </div>

  <div class="cert-grid">
    <div class="cert-card">
      <div class="cert-title">🧠 PSYCH101: Intro to Psychology</div>
      <div class="cert-meta">Credential ID: 8173289785AS</div>
      <span class="cert-issuer">Saylor Academy · Aug 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">⚙️ Apache Kafka Basics</div>
      <div class="cert-meta">Apache Kafka · Stream Processing</div>
      <span class="cert-issuer">Great Learning · Jul 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">💡 ChatGPT Prompt Engineering for Devs</div>
      <div class="cert-meta">Prompt Engineering · AI Prompting</div>
      <span class="cert-issuer">DeepLearning.AI · Jul 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">🧠 NLP Project-based Learning</div>
      <div class="cert-meta">NLP · Machine Learning · Statistical Analysis</div>
      <span class="cert-issuer">Great Learning · Jul 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">💻 CS302: Software Engineering</div>
      <div class="cert-meta">SDLC · Software Engineering Practices</div>
      <span class="cert-issuer">Saylor Academy · Jun 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">🚀 Cohort Member</div>
      <div class="cert-meta">Machine Learning · Software Engineering</div>
      <span class="cert-issuer">Buildspace · Jun 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">🤖 Applied Machine Learning Algorithms</div>
      <div class="cert-meta">SVM · KNN · Random Forest · Decision Trees</div>
      <span class="cert-issuer">Great Learning · May 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">🐍 CS250: Python for Data Science</div>
      <div class="cert-meta">NumPy · Pandas · Matplotlib</div>
      <span class="cert-issuer">Saylor Academy · May 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">📊 Google Analytics IQ</div>
      <div class="cert-meta">Analytical Skills · Data Analysis</div>
      <span class="cert-issuer">Google Analytics 4 · May 2024</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">🧠 Introduction to Generative AI</div>
      <div class="cert-meta">LLMs · Large Language Models · Generative AI</div>
      <span class="cert-issuer">Coursera · Oct 2023</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">🤖 Fine-Tuning Large Language Models</div>
      <div class="cert-meta">LLM · Fine Tuning</div>
      <span class="cert-issuer">DeepLearning.AI · 2022</span>
    </div>
    <div class="cert-card">
      <div class="cert-title">🤖 AI/ML Mentorship Recognition</div>
      <div class="cert-meta">NumPy · AI · Pandas · NLP · Machine Learning</div>
      <span class="cert-issuer">ACES · Jan 2024</span>
    </div>
  </div>

  <div class="divider"></div>

  <!-- ═══ FOOTER ═══ -->
  <div class="footer">
    <div class="footer-copy">© <span>Abhishek Shah</span> · 2026 · Pātan, Nepal</div>
    <div class="footer-copy" style="color: var(--dim);">Built with 🧠 + ☕</div>
  </div>

</div>

<script>
  // Subtle parallax on scroll
  window.addEventListener('scroll', () => {
    const y = window.scrollY;
    document.querySelector('.nebula').style.transform = `translateY(${y * 0.08}px)`;
  });
</script>
</body>
</html>
