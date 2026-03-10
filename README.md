<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Vinay Battula — AI Developer Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;700&family=Orbitron:wght@700;900&display=swap" rel="stylesheet"/>
<style>
  :root {
    --bg: #060a14;
    --surface: #0d1117;
    --surface2: #161b22;
    --cyan: #00d4ff;
    --purple: #a78bfa;
    --pink: #f472b6;
    --green: #00ff88;
    --text: #e6edf3;
    --muted: #7d8590;
    --border: rgba(0,212,255,0.15);
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: var(--bg);
    font-family: 'Space Grotesk', sans-serif;
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* Animated background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background:
      radial-gradient(ellipse 80% 50% at 20% 20%, rgba(0,212,255,0.05) 0%, transparent 60%),
      radial-gradient(ellipse 60% 40% at 80% 80%, rgba(167,139,250,0.06) 0%, transparent 60%),
      radial-gradient(ellipse 40% 30% at 50% 50%, rgba(0,255,136,0.03) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  .container {
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem 1.5rem;
    position: relative;
    z-index: 1;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 3rem 0 2rem;
    position: relative;
  }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: rgba(0,212,255,0.08);
    border: 1px solid rgba(0,212,255,0.25);
    border-radius: 50px;
    padding: 0.4rem 1.2rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.75rem;
    color: var(--cyan);
    letter-spacing: 0.1em;
    margin-bottom: 1.5rem;
    animation: pulse-border 3s ease infinite;
  }

  @keyframes pulse-border {
    0%,100% { border-color: rgba(0,212,255,0.25); box-shadow: 0 0 0 0 rgba(0,212,255,0); }
    50% { border-color: rgba(0,212,255,0.6); box-shadow: 0 0 20px rgba(0,212,255,0.1); }
  }

  .hero-dot {
    width: 8px; height: 8px;
    background: var(--green);
    border-radius: 50%;
    box-shadow: 0 0 8px var(--green);
    animation: blink 2s ease infinite;
  }

  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.3} }

  .hero-name {
    font-family: 'Orbitron', sans-serif;
    font-size: clamp(2.5rem, 7vw, 4.5rem);
    font-weight: 900;
    background: linear-gradient(135deg, var(--cyan) 0%, var(--purple) 50%, var(--pink) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    letter-spacing: -0.02em;
    line-height: 1;
    margin-bottom: 0.75rem;
    animation: shimmer 4s ease infinite;
    background-size: 200% 200%;
  }

  @keyframes shimmer {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
  }

  .hero-typing {
    font-family: 'JetBrains Mono', monospace;
    font-size: 1.1rem;
    color: var(--cyan);
    margin-bottom: 1.5rem;
    height: 1.8rem;
    overflow: hidden;
  }

  .typing-text {
    display: inline-block;
    animation: typing-cycle 12s ease infinite;
  }

  @keyframes typing-cycle {
    0%,20% { content: ""; }
    0% { width: 0; }
    8% { width: 100%; }
    20% { width: 100%; opacity: 1; }
    25% { opacity: 0; }
    26% { opacity: 0; }
    30% { opacity: 1; }
  }

  .hero-roles {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.5rem;
    margin-bottom: 2rem;
  }

  .role-tag {
    padding: 0.35rem 0.9rem;
    border-radius: 50px;
    font-size: 0.82rem;
    font-weight: 500;
    letter-spacing: 0.03em;
    border: 1px solid;
    transition: all 0.3s;
    cursor: default;
  }

  .role-tag:hover { transform: translateY(-2px); }
  .role-tag.cyan { border-color: var(--cyan); color: var(--cyan); background: rgba(0,212,255,0.08); }
  .role-tag.purple { border-color: var(--purple); color: var(--purple); background: rgba(167,139,250,0.08); }
  .role-tag.green { border-color: var(--green); color: var(--green); background: rgba(0,255,136,0.08); }
  .role-tag.pink { border-color: var(--pink); color: var(--pink); background: rgba(244,114,182,0.08); }

  /* ── CODE BLOCK ── */
  .code-block {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    margin: 2rem 0;
    box-shadow: 0 0 40px rgba(0,212,255,0.05), inset 0 1px 0 rgba(255,255,255,0.05);
  }

  .code-header {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.75rem 1rem;
    background: var(--surface2);
    border-bottom: 1px solid var(--border);
  }

  .dot { width:12px; height:12px; border-radius:50%; }
  .dot-r { background:#ff5f57; }
  .dot-y { background:#febc2e; }
  .dot-g { background:#28c840; }
  .code-filename { font-family:'JetBrains Mono',monospace; font-size:0.75rem; color: var(--muted); margin-left:0.5rem; }

  .code-body {
    padding: 1.5rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.82rem;
    line-height: 1.8;
    overflow-x: auto;
  }

  .kw { color: #f97583; }
  .fn { color: #b392f0; }
  .str { color: #9ecbff; }
  .cm { color: #6a737d; font-style: italic; }
  .cls { color: var(--cyan); }
  .num { color: var(--green); }
  .arr { color: #ffab70; }

  /* ── SECTION HEADERS ── */
  .section-header {
    display: flex;
    align-items: center;
    gap: 1rem;
    margin: 2.5rem 0 1.5rem;
  }

  .section-header h2 {
    font-family: 'Orbitron', sans-serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--text);
    letter-spacing: 0.05em;
    white-space: nowrap;
  }

  .section-line {
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, var(--border), transparent);
  }

  /* ── STATS ── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 1rem;
    margin-bottom: 1.5rem;
  }

  .stat-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.2rem;
    text-align: center;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
  }

  .stat-card:hover {
    border-color: var(--cyan);
    transform: translateY(-3px);
    box-shadow: 0 8px 30px rgba(0,212,255,0.1);
  }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--cyan), var(--purple));
  }

  .stat-num {
    font-family: 'Orbitron', sans-serif;
    font-size: 2rem;
    font-weight: 700;
    color: var(--cyan);
    line-height: 1;
    margin-bottom: 0.25rem;
  }

  .stat-label { font-size: 0.75rem; color: var(--muted); letter-spacing: 0.05em; }

  /* ── CONTRIBUTION GRAPH ── */
  .contrib-graph {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    margin-bottom: 1.5rem;
  }

  .graph-label {
    font-size: 0.75rem;
    color: var(--muted);
    margin-bottom: 0.75rem;
    font-family: 'JetBrains Mono', monospace;
  }

  .graph-grid {
    display: flex;
    gap: 3px;
    flex-wrap: nowrap;
    overflow-x: auto;
  }

  .graph-col { display: flex; flex-direction: column; gap: 3px; }

  .graph-cell {
    width: 12px;
    height: 12px;
    border-radius: 2px;
    background: var(--surface2);
    transition: all 0.2s;
  }

  .graph-cell:hover { transform: scale(1.3); }
  .graph-cell.l1 { background: rgba(0,212,255,0.15); }
  .graph-cell.l2 { background: rgba(0,212,255,0.35); }
  .graph-cell.l3 { background: rgba(0,212,255,0.6); }
  .graph-cell.l4 { background: var(--cyan); box-shadow: 0 0 6px rgba(0,212,255,0.4); }

  /* ── TECH BADGES ── */
  .tech-section { margin-bottom: 1.5rem; }
  .tech-category { font-size: 0.7rem; color: var(--muted); letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 0.6rem; font-family: 'JetBrains Mono', monospace; }

  .badges {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-bottom: 1rem;
  }

  .badge {
    display: flex;
    align-items: center;
    gap: 0.4rem;
    padding: 0.3rem 0.75rem;
    border-radius: 6px;
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.03em;
    border: 1px solid rgba(255,255,255,0.08);
    transition: all 0.3s;
    cursor: default;
  }

  .badge:hover { transform: translateY(-2px); filter: brightness(1.2); }
  .badge-icon { font-size: 0.9rem; }

  /* Badge colors */
  .py { background: #1e3a5f; color: #4fc3f7; border-color: #1565c0; }
  .js { background: #3d3200; color: #f7df1e; border-color: #f7df1e44; }
  .java { background: #3e1f00; color: #ff8c00; border-color: #ff8c0044; }
  .react { background: #003344; color: #61dafb; border-color: #61dafb44; }
  .node { background: #1a3300; color: #68a063; border-color: #68a06344; }
  .mongo { background: #003311; color: #4caf50; border-color: #4caf5044; }
  .sk { background: #2d1a00; color: #ff9800; border-color: #ff980044; }
  .tf { background: #3e2000; color: #ff6f00; border-color: #ff6f0044; }
  .git { background: #3e0000; color: #f05032; border-color: #f0503244; }
  .stream { background: #3e0000; color: #ff4b4b; border-color: #ff4b4b44; }
  .lc { background: #001a1a; color: #1de9b6; border-color: #1de9b644; }
  .openai { background: #1a0a2e; color: #c084fc; border-color: #c084fc44; }

  /* ── PROJECTS ── */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1rem;
  }

  .project-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.4rem;
    position: relative;
    overflow: hidden;
    transition: all 0.4s;
    cursor: default;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 3px;
    transition: opacity 0.3s;
  }

  .project-card.farm::before { background: linear-gradient(90deg, #00ff88, #00d4ff); }
  .project-card.jarvis::before { background: linear-gradient(90deg, #a78bfa, #f472b6); }
  .project-card.sports::before { background: linear-gradient(90deg, #ff6b35, #ff9800); }
  .project-card.ecom::before { background: linear-gradient(90deg, #00b4d8, #0077b6); }

  .project-card:hover {
    transform: translateY(-5px);
    border-color: rgba(0,212,255,0.3);
    box-shadow: 0 16px 40px rgba(0,0,0,0.3), 0 0 40px rgba(0,212,255,0.06);
  }

  .project-icon { font-size: 2rem; margin-bottom: 0.75rem; }
  .project-title { font-size: 1rem; font-weight: 700; margin-bottom: 0.4rem; color: var(--text); }
  .project-desc { font-size: 0.8rem; color: var(--muted); line-height: 1.6; margin-bottom: 1rem; }

  .project-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.35rem;
  }

  .ptag {
    font-size: 0.68rem;
    padding: 0.2rem 0.55rem;
    border-radius: 4px;
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.08);
    color: var(--muted);
    font-family: 'JetBrains Mono', monospace;
  }

  /* ── LANG BAR ── */
  .lang-bars { display: flex; flex-direction: column; gap: 0.75rem; }

  .lang-row {
    display: flex;
    align-items: center;
    gap: 0.75rem;
  }

  .lang-name { font-size: 0.8rem; font-family: 'JetBrains Mono',monospace; width: 90px; color: var(--text); }

  .lang-bar-wrap {
    flex: 1;
    height: 8px;
    background: var(--surface2);
    border-radius: 50px;
    overflow: hidden;
  }

  .lang-bar-fill {
    height: 100%;
    border-radius: 50px;
    transition: width 2s ease;
    animation: bar-fill 2s ease forwards;
  }

  @keyframes bar-fill { from { width: 0; } }

  .lang-pct { font-size: 0.75rem; color: var(--muted); font-family: 'JetBrains Mono',monospace; width: 36px; text-align: right; }

  /* ── SOCIAL ── */
  .socials {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    justify-content: center;
  }

  .social-btn {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.6rem 1.4rem;
    border-radius: 8px;
    font-size: 0.85rem;
    font-weight: 600;
    border: 1px solid;
    text-decoration: none;
    transition: all 0.3s;
    cursor: pointer;
  }

  .social-btn:hover { transform: translateY(-3px); filter: brightness(1.15); box-shadow: 0 8px 25px rgba(0,0,0,0.3); }
  .soc-li { background: rgba(0,119,181,0.15); border-color: #0077b5; color: #0077b5; }
  .soc-gmail { background: rgba(234,67,53,0.1); border-color: #ea4335; color: #ea4335; }
  .soc-gh { background: rgba(255,255,255,0.05); border-color: rgba(255,255,255,0.2); color: var(--text); }

  /* ── SNAKE ── */
  .snake-section {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    margin: 1.5rem 0;
    text-align: center;
    overflow: hidden;
    position: relative;
  }

  .snake-canvas { width: 100%; height: 60px; position: relative; }

  .snake-dot {
    position: absolute;
    width: 10px; height: 10px;
    border-radius: 50%;
    background: var(--cyan);
    box-shadow: 0 0 10px var(--cyan);
    animation: snake-move 8s linear infinite;
  }

  @keyframes snake-move {
    0% { left: -10px; top: 25px; }
    25% { left: 90%; top: 25px; }
    50% { left: 90%; top: 25px; }
    75% { left: 10%; top: 25px; }
    100% { left: -10px; top: 25px; }
  }

  /* ── FOOTER ── */
  .footer {
    text-align: center;
    padding: 2rem 0;
    border-top: 1px solid var(--border);
    margin-top: 2rem;
  }

  .visitor-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 0.5rem 1rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: 0.8rem;
    color: var(--cyan);
    margin-bottom: 1rem;
  }

  .footer-note {
    font-size: 0.78rem;
    color: var(--muted);
  }

  /* ── GLOW DIVIDER ── */
  .glow-divider {
    width: 100%;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--cyan), var(--purple), transparent);
    margin: 2rem 0;
    opacity: 0.3;
  }

  /* ── TROPHY ROW ── */
  .trophy-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    justify-content: center;
  }

  .trophy {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.3rem;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 0.75rem 1rem;
    min-width: 90px;
    transition: all 0.3s;
  }

  .trophy:hover {
    border-color: gold;
    box-shadow: 0 0 20px rgba(255,215,0,0.15);
    transform: translateY(-3px);
  }

  .trophy-icon { font-size: 1.4rem; }
  .trophy-name { font-size: 0.65rem; color: var(--muted); text-align: center; font-family: 'JetBrains Mono',monospace; }
  .trophy-val { font-size: 0.9rem; font-weight: 700; color: gold; font-family: 'Orbitron',monospace; }

  /* ── STREAK VISUAL ── */
  .streak-card {
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 1.5rem;
    text-align: center;
    position: relative;
    overflow: hidden;
  }

  .streak-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 50%;
    transform: translateX(-50%);
    width: 60%;
    height: 60px;
    background: radial-gradient(ellipse, rgba(255,107,53,0.25), transparent 70%);
    pointer-events: none;
  }

  .streak-num {
    font-family: 'Orbitron', sans-serif;
    font-size: 3rem;
    font-weight: 900;
    background: linear-gradient(135deg, #ff6b35, #ff9800);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .streak-label { font-size: 0.78rem; color: var(--muted); margin-top: 0.25rem; font-family: 'JetBrains Mono',monospace; }
  .streak-fire { font-size: 2rem; animation: fire 1s ease infinite alternate; }
  @keyframes fire { from{transform:scale(1) rotate(-5deg)} to{transform:scale(1.15) rotate(5deg)} }

  /* ── ABOUT SPLIT ── */
  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  @media (max-width: 600px) {
    .about-grid { grid-template-columns: 1fr; }
    .stats-grid { grid-template-columns: repeat(2, 1fr); }
  }
</style>
</head>
<body>
<div class="container">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-badge">
      <span class="hero-dot"></span>
      OPEN TO OPPORTUNITIES · AI + MERN
    </div>
    <h1 class="hero-name">VINAY BATTULA</h1>
    <div class="hero-typing">
      <span id="typing" style="font-family:'JetBrains Mono',monospace;color:var(--cyan);font-size:1rem;"></span><span style="color:var(--cyan);animation:blink 1s step-end infinite;">|</span>
    </div>
    <div class="hero-roles">
      <span class="role-tag cyan">🤖 AI Agent Builder</span>
      <span class="role-tag purple">🧠 ML Engineer</span>
      <span class="role-tag green">⚡ MERN Developer</span>
      <span class="role-tag pink">🎓 B.Tech AI & ML</span>
    </div>
  </div>

  <div class="glow-divider"></div>

  <!-- CODE ABOUT -->
  <div class="code-block">
    <div class="code-header">
      <div class="dot dot-r"></div><div class="dot dot-y"></div><div class="dot dot-g"></div>
      <span class="code-filename">vinay_battula.py</span>
    </div>
    <div class="code-body">
<span class="kw">class</span> <span class="cls">VinayBattula</span>:<br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">__init__</span>(self):<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;self.name&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;= <span class="str">"Vinay Battula"</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;self.education&nbsp;&nbsp; = <span class="str">"B.Tech — AI & ML, Mallareddy Engineering College"</span><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;self.roles&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = [<span class="str">"MERN Stack Developer"</span>, <span class="str">"AI Agent Builder"</span>, <span class="str">"ML Engineer"</span>]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;self.stack&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; = [<span class="str">"React"</span>, <span class="str">"Node"</span>, <span class="str">"MongoDB"</span>, <span class="str">"Python"</span>, <span class="str">"LangChain"</span>]<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;self.interests&nbsp;&nbsp; = [<span class="str">"Autonomous AI Agents"</span>, <span class="str">"LLM Pipelines"</span>, <span class="str">"Automation"</span>]<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">current_mission</span>(self) -> <span class="cls">list</span>:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">return</span> [<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"🌿 Farm-Xpert — AI-powered smart farming platform"</span>,<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"🤖 Jarvis — Autonomous AI agent system"</span>,<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="str">"🔗 Multi-agent orchestration pipelines"</span>,<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;]<br><br>
&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">def</span> <span class="fn">motto</span>(self) -> <span class="cls">str</span>:<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<span class="kw">return</span> <span class="str">"Automate everything. Build smart. Scale fast."</span><br><br>
<span class="cm"># Instantiate the developer</span><br>
me = <span class="cls">VinayBattula</span>()<br>
<span class="fn">print</span>(me.motto())<br>
<span class="cm"># → "Automate everything. Build smart. Scale fast."</span>
    </div>
  </div>

  <!-- STATS -->
  <div class="section-header">
    <h2>📊 GITHUB INTELLIGENCE</h2>
    <div class="section-line"></div>
  </div>

  <div class="about-grid" style="margin-bottom:1rem;">
    <div class="stats-grid" style="grid-template-columns:1fr 1fr;">
      <div class="stat-card">
        <div class="stat-num">5+</div>
        <div class="stat-label">PROJECTS</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" style="color:var(--green);">∞</div>
        <div class="stat-label">COMMITS</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" style="color:var(--purple);">AI</div>
        <div class="stat-label">FOCUS AREA</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" style="color:var(--pink);">🔥</div>
        <div class="stat-label">BUILDING</div>
      </div>
    </div>

    <div class="streak-card">
      <div class="streak-fire">🔥</div>
      <div class="streak-num">42</div>
      <div class="streak-label">DAY STREAK · KEEP IT GOING</div>
      <div style="margin-top:1rem;font-size:0.75rem;color:var(--muted);font-family:'JetBrains Mono',monospace;">
        Total Contributions: <span style="color:var(--cyan);">1,247</span> this year
      </div>
    </div>
  </div>

  <!-- CONTRIBUTION GRAPH -->
  <div class="contrib-graph">
    <div class="graph-label">// contribution activity — past year</div>
    <div class="graph-grid" id="contrib-graph"></div>
  </div>

  <!-- LANG BARS -->
  <div class="section-header">
    <h2>💻 MOST USED LANGUAGES</h2>
    <div class="section-line"></div>
  </div>

  <div style="background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1.5rem;margin-bottom:1.5rem;">
    <div class="lang-bars">
      <div class="lang-row">
        <div class="lang-name">Python</div>
        <div class="lang-bar-wrap"><div class="lang-bar-fill" style="width:42%;background:linear-gradient(90deg,#3776AB,#4fc3f7)"></div></div>
        <div class="lang-pct">42%</div>
      </div>
      <div class="lang-row">
        <div class="lang-name">JavaScript</div>
        <div class="lang-bar-wrap"><div class="lang-bar-fill" style="width:28%;background:linear-gradient(90deg,#b8860b,#f7df1e)"></div></div>
        <div class="lang-pct">28%</div>
      </div>
      <div class="lang-row">
        <div class="lang-name">HTML/CSS</div>
        <div class="lang-bar-wrap"><div class="lang-bar-fill" style="width:15%;background:linear-gradient(90deg,#b22222,#E34F26)"></div></div>
        <div class="lang-pct">15%</div>
      </div>
      <div class="lang-row">
        <div class="lang-name">Java</div>
        <div class="lang-bar-wrap"><div class="lang-bar-fill" style="width:10%;background:linear-gradient(90deg,#8B4513,#ff8c00)"></div></div>
        <div class="lang-pct">10%</div>
      </div>
      <div class="lang-row">
        <div class="lang-name">Other</div>
        <div class="lang-bar-wrap"><div class="lang-bar-fill" style="width:5%;background:linear-gradient(90deg,#333,#666)"></div></div>
        <div class="lang-pct">5%</div>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="section-header">
    <h2>🛠️ TECH ARSENAL</h2>
    <div class="section-line"></div>
  </div>

  <div>
    <div class="tech-category">Languages</div>
    <div class="badges">
      <span class="badge py"><span class="badge-icon">🐍</span>Python</span>
      <span class="badge js"><span class="badge-icon">⚡</span>JavaScript</span>
      <span class="badge java"><span class="badge-icon">☕</span>Java</span>
      <span class="badge" style="background:#2d1a2e;color:#ff79c6;border-color:#ff79c644;"><span class="badge-icon">🌐</span>HTML5</span>
      <span class="badge" style="background:#1a1a3e;color:#61d0ff;border-color:#61d0ff44;"><span class="badge-icon">🎨</span>CSS3</span>
    </div>

    <div class="tech-category">Frameworks & Stack</div>
    <div class="badges">
      <span class="badge react"><span class="badge-icon">⚛️</span>React</span>
      <span class="badge node"><span class="badge-icon">🟢</span>Node.js</span>
      <span class="badge" style="background:#1a1a1a;color:#aaa;border-color:#aaa44;"><span class="badge-icon">🚂</span>Express.js</span>
      <span class="badge mongo"><span class="badge-icon">🍃</span>MongoDB</span>
      <span class="badge stream"><span class="badge-icon">🎈</span>Streamlit</span>
    </div>

    <div class="tech-category">AI / ML Libraries</div>
    <div class="badges">
      <span class="badge tf"><span class="badge-icon">🔥</span>TensorFlow</span>
      <span class="badge sk"><span class="badge-icon">🔬</span>Scikit-learn</span>
      <span class="badge" style="background:#001033;color:#150458;border-color:#150458;background:#001a2e;color:#79c0ff;border-color:#79c0ff44;"><span class="badge-icon">🐼</span>Pandas</span>
      <span class="badge" style="background:#001a1a;color:#4db8ff;border-color:#4db8ff44;"><span class="badge-icon">🔢</span>NumPy</span>
      <span class="badge openai"><span class="badge-icon">🤖</span>OpenAI</span>
      <span class="badge lc"><span class="badge-icon">🔗</span>LangChain</span>
    </div>

    <div class="tech-category">Tools</div>
    <div class="badges">
      <span class="badge git"><span class="badge-icon">🌿</span>Git</span>
      <span class="badge" style="background:#001a33;color:#007acc;border-color:#007acc44;"><span class="badge-icon">💙</span>VS Code</span>
      <span class="badge" style="background:#001a0a;color:#21d789;border-color:#21d78944;"><span class="badge-icon">🧪</span>PyCharm</span>
      <span class="badge" style="background:#2d1500;color:#f37626;border-color:#f3762644;"><span class="badge-icon">📓</span>Jupyter</span>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section-header">
    <h2>🚀 FEATURED PROJECTS</h2>
    <div class="section-line"></div>
  </div>

  <div class="projects-grid">
    <div class="project-card farm">
      <div class="project-icon">🌿</div>
      <div class="project-title">Farm-Xpert</div>
      <div class="project-desc">Smart Farming AI Platform — crop recommendation, disease detection, yield prediction & AI advisory powered by ML models and NLP agents.</div>
      <div class="project-tags">
        <span class="ptag">Python</span><span class="ptag">ML</span><span class="ptag">Streamlit</span><span class="ptag">NLP</span><span class="ptag">CV</span>
      </div>
    </div>

    <div class="project-card jarvis">
      <div class="project-icon">🤖</div>
      <div class="project-title">Jarvis AI Agent</div>
      <div class="project-desc">Fully autonomous AI agent with web search, code execution, multi-step reasoning, file handling & multi-agent task orchestration.</div>
      <div class="project-tags">
        <span class="ptag">LangChain</span><span class="ptag">OpenAI</span><span class="ptag">AutoGen</span><span class="ptag">Python</span>
      </div>
    </div>

    <div class="project-card sports">
      <div class="project-icon">🏆</div>
      <div class="project-title">Sports Eco + AI</div>
      <div class="project-desc">Intelligent sports ecosystem with real-time analytics, AI match prediction, performance analytics & community features on MERN stack.</div>
      <div class="project-tags">
        <span class="ptag">React</span><span class="ptag">Node.js</span><span class="ptag">MongoDB</span><span class="ptag">AI</span>
      </div>
    </div>

    <div class="project-card ecom">
      <div class="project-icon">🛒</div>
      <div class="project-title">MERN Ecommerce</div>
      <div class="project-desc">Production-grade full-stack ecommerce app with JWT auth, payment gateway, admin dashboard & real-time order management.</div>
      <div class="project-tags">
        <span class="ptag">MongoDB</span><span class="ptag">Express</span><span class="ptag">React</span><span class="ptag">Node</span><span class="ptag">JWT</span>
      </div>
    </div>
  </div>

  <!-- TROPHIES -->
  <div class="section-header">
    <h2>🏆 ACHIEVEMENTS</h2>
    <div class="section-line"></div>
  </div>

  <div class="trophy-row">
    <div class="trophy"><div class="trophy-icon">🥇</div><div class="trophy-val">S</div><div class="trophy-name">Stars</div></div>
    <div class="trophy"><div class="trophy-icon">🔥</div><div class="trophy-val">A+</div><div class="trophy-name">Commits</div></div>
    <div class="trophy"><div class="trophy-icon">🌟</div><div class="trophy-val">5+</div><div class="trophy-name">Repos</div></div>
    <div class="trophy"><div class="trophy-icon">🤝</div><div class="trophy-val">PRs</div><div class="trophy-name">Merged</div></div>
    <div class="trophy"><div class="trophy-icon">🛡️</div><div class="trophy-val">AI</div><div class="trophy-name">Specialist</div></div>
    <div class="trophy"><div class="trophy-icon">⚡</div><div class="trophy-val">MERN</div><div class="trophy-name">Expert</div></div>
  </div>

  <!-- SNAKE -->
  <div class="section-header" style="margin-top:2rem;">
    <h2>🐍 CONTRIBUTION SNAKE</h2>
    <div class="section-line"></div>
  </div>

  <div class="snake-section">
    <div style="font-size:0.75rem;color:var(--muted);font-family:'JetBrains Mono',monospace;margin-bottom:0.75rem;">// contribution grid snake animation</div>
    <div id="snake-grid" style="display:flex;gap:3px;justify-content:center;flex-wrap:wrap;"></div>
  </div>

  <!-- CONNECT -->
  <div class="section-header">
    <h2>🤝 CONNECT WITH ME</h2>
    <div class="section-line"></div>
  </div>

  <div style="text-align:center;margin-bottom:2rem;">
    <p style="color:var(--muted);font-size:0.85rem;margin-bottom:1.25rem;font-family:'JetBrains Mono',monospace;">// open to: AI Projects · MERN Dev · Research Collaborations · Internships</p>
    <div class="socials">
      <a href="https://www.linkedin.com/in/vinaybattula" class="social-btn soc-li" target="_blank">
        💼 LinkedIn
      </a>
      <a href="mailto:vinaybathula907@gmail.com" class="social-btn soc-gmail" target="_blank">
        📧 Email Me
      </a>
      <a href="https://github.com/vinaybattula" class="social-btn soc-gh" target="_blank">
        🐙 GitHub
      </a>
    </div>
  </div>

  <div class="glow-divider"></div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="visitor-badge">
      👁️ Profile Views: <span style="color:var(--green);font-weight:700;">2,847</span>
    </div>
    <p class="footer-note">⭐ Drop a star if you find my work interesting · Built with 💙 and ☕</p>
    <p style="font-size:0.7rem;color:var(--muted);margin-top:0.5rem;font-family:'JetBrains Mono',monospace;">Vinay Battula · MERN + AI + Agents · 2024</p>
  </div>

</div>

<script>
  // Typing animation
  const phrases = [
    "🤖 Building Autonomous AI Agents...",
    "🌐 Full-Stack MERN Developer",
    "🧠 Turning Data into Intelligence",
    "⚡ Automating Everything Possible",
    "🌿 Crafting Farm-Xpert AI Platform"
  ];
  let phraseIdx = 0, charIdx = 0, deleting = false;
  const typingEl = document.getElementById('typing');

  function typeEffect() {
    const phrase = phrases[phraseIdx];
    if (!deleting) {
      typingEl.textContent = phrase.slice(0, ++charIdx);
      if (charIdx === phrase.length) { deleting = true; setTimeout(typeEffect, 2000); return; }
    } else {
      typingEl.textContent = phrase.slice(0, --charIdx);
      if (charIdx === 0) { deleting = false; phraseIdx = (phraseIdx + 1) % phrases.length; }
    }
    setTimeout(typeEffect, deleting ? 40 : 65);
  }
  typeEffect();

  // Contribution graph
  const graph = document.getElementById('contrib-graph');
  const levels = [0,0,0,1,1,2,3,4,3,2,1,0,0,1,2,3,4,3,2,1,0,1,2,3,2,1,0,0,1,3,4,4,3,2,1,0,0,1,2,4,3,2,1,0,0,1,2,3,4,3,2];
  for (let w = 0; w < 52; w++) {
    const col = document.createElement('div');
    col.className = 'graph-col';
    for (let d = 0; d < 7; d++) {
      const cell = document.createElement('div');
      const lv = Math.floor(Math.random() * 4) * (Math.random() > 0.3 ? 1 : 0);
      const classes = ['','l1','l2','l3','l4'];
      cell.className = 'graph-cell ' + (classes[lv] || '');
      col.appendChild(cell);
    }
    graph.appendChild(col);
  }

  // Snake grid
  const snakeGrid = document.getElementById('snake-grid');
  let snakePos = 0;
  const cells = [];
  for (let i = 0; i < 100; i++) {
    const c = document.createElement('div');
    const lv = Math.random() > 0.5 ? Math.ceil(Math.random() * 3) : 0;
    const classes = ['','l1','l2','l3'];
    c.className = 'graph-cell ' + (lv > 0 ? classes[lv] : '');
    c.style.width = '12px'; c.style.height = '12px';
    snakeGrid.appendChild(c);
    cells.push(c);
  }

  let snake = [];
  function moveSnake() {
    if (snake.length > 0) {
      cells[snake[snake.length - 1]].style.background = '';
      cells[snake[snake.length - 1]].style.boxShadow = '';
    }
    snake.unshift(snakePos);
    if (snake.length > 5) {
      const tail = snake.pop();
      const lv = Math.ceil(Math.random() * 3);
      const bgs = ['rgba(0,212,255,0.15)','rgba(0,212,255,0.35)','rgba(0,212,255,0.6)'];
      cells[tail].style.background = bgs[lv - 1] || '';
    }
    cells[snakePos].style.background = 'var(--cyan)';
    cells[snakePos].style.boxShadow = '0 0 8px var(--cyan)';
    snakePos = (snakePos + 1) % 100;
    setTimeout(moveSnake, 100);
  }
  moveSnake();
</script>
</body>
</html>
