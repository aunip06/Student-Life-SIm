<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Student Life Simulator — Flow & Features</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Syne:wght@400;700;800&display=swap');

  :root {
    --bg: #0a0a0f;
    --surface: #111118;
    --border: #2a2a3a;
    --accent: #00ff88;
    --accent2: #ff3864;
    --accent3: #ffbe00;
    --accent4: #4f8ef7;
    --dim: #444466;
    --text: #d0d0e8;
    --muted: #666688;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Space Mono', monospace;
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* NOISE OVERLAY */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 9999;
    opacity: 0.4;
  }

  header {
    padding: 3rem 2rem 1.5rem;
    text-align: center;
    border-bottom: 1px solid var(--border);
    position: relative;
  }

  header::after {
    content: '';
    position: absolute;
    bottom: -1px;
    left: 50%;
    transform: translateX(-50%);
    width: 200px;
    height: 2px;
    background: var(--accent);
    box-shadow: 0 0 20px var(--accent);
  }

  .title {
    font-family: 'Syne', sans-serif;
    font-size: clamp(1.6rem, 4vw, 3rem);
    font-weight: 800;
    letter-spacing: -0.02em;
    color: #fff;
  }

  .title span { color: var(--accent); }

  .subtitle {
    font-size: 0.72rem;
    color: var(--muted);
    margin-top: 0.5rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
  }

  /* TABS */
  .tabs {
    display: flex;
    gap: 0;
    padding: 1.5rem 2rem 0;
    max-width: 1400px;
    margin: 0 auto;
  }

  .tab {
    padding: 0.6rem 1.4rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    cursor: pointer;
    border: 1px solid var(--border);
    background: transparent;
    color: var(--muted);
    transition: all 0.2s;
    border-bottom: none;
  }

  .tab:first-child { border-radius: 6px 0 0 0; }
  .tab:last-child { border-radius: 0 6px 0 0; }

  .tab.active {
    background: var(--surface);
    color: var(--accent);
    border-color: var(--accent);
  }

  .tab:hover:not(.active) { color: var(--text); border-color: var(--dim); }

  /* PANELS */
  .panel { display: none; }
  .panel.active { display: block; }

  .container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 2rem;
  }

  /* FLOWCHART */
  .flow-wrap {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0;
    padding: 1rem 0;
  }

  .node {
    position: relative;
    border: 1px solid var(--border);
    background: var(--surface);
    border-radius: 8px;
    padding: 1rem 1.5rem;
    text-align: center;
    width: min(520px, 90vw);
    transition: border-color 0.3s, box-shadow 0.3s;
    cursor: default;
  }

  .node:hover {
    box-shadow: 0 0 24px rgba(0,255,136,0.1);
    border-color: var(--dim);
  }

  .node.start {
    border-color: var(--accent);
    background: rgba(0,255,136,0.04);
    box-shadow: 0 0 30px rgba(0,255,136,0.08);
  }

  .node.decision {
    border-color: var(--accent3);
    background: rgba(255,190,0,0.04);
    clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
    width: min(360px, 85vw);
    height: 120px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .node.decision .node-label { font-size: 0.72rem; }

  .node.action {
    border-color: var(--accent4);
    background: rgba(79,142,247,0.04);
  }

  .node.bad {
    border-color: var(--accent2);
    background: rgba(255,56,100,0.04);
  }

  .node.end {
    border-color: var(--accent2);
    box-shadow: 0 0 30px rgba(255,56,100,0.1);
    background: rgba(255,56,100,0.05);
  }

  .node-label {
    font-family: 'Syne', sans-serif;
    font-size: 0.9rem;
    font-weight: 700;
    color: #fff;
    line-height: 1.3;
  }

  .node-irony {
    font-size: 0.62rem;
    color: var(--muted);
    margin-top: 0.35rem;
    font-style: italic;
    letter-spacing: 0.02em;
  }

  .node-code {
    font-size: 0.6rem;
    color: var(--accent);
    margin-top: 0.25rem;
    letter-spacing: 0.08em;
  }

  /* ARROWS */
  .arrow {
    width: 2px;
    height: 36px;
    background: var(--dim);
    position: relative;
    flex-shrink: 0;
  }

  .arrow::after {
    content: '▼';
    position: absolute;
    bottom: -8px;
    left: 50%;
    transform: translateX(-50%);
    color: var(--dim);
    font-size: 0.65rem;
  }

  .arrow-label {
    position: absolute;
    left: 14px;
    top: 50%;
    transform: translateY(-50%);
    font-size: 0.6rem;
    color: var(--accent3);
    white-space: nowrap;
    letter-spacing: 0.06em;
  }

  .branch {
    display: flex;
    gap: 2rem;
    align-items: flex-start;
    width: 100%;
    max-width: 1100px;
    justify-content: center;
  }

  .branch-arm {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0;
    flex: 1;
    max-width: 340px;
  }

  .branch-label {
    font-size: 0.6rem;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 0.2rem 0.8rem;
    border-radius: 20px;
    margin-bottom: 0;
  }

  .branch-label.yes { background: rgba(0,255,136,0.1); color: var(--accent); border: 1px solid rgba(0,255,136,0.3); }
  .branch-label.no  { background: rgba(255,56,100,0.1); color: var(--accent2); border: 1px solid rgba(255,56,100,0.3); }
  .branch-label.match  { background: rgba(79,142,247,0.1); color: var(--accent4); border: 1px solid rgba(79,142,247,0.3); }
  .branch-label.mismatch  { background: rgba(255,190,0,0.1); color: var(--accent3); border: 1px solid rgba(255,190,0,0.3); }

  .h-line {
    width: 100%;
    height: 1px;
    background: var(--dim);
    margin: 0;
  }

  /* FEATURES GRID */
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.2rem;
  }

  .feat-card {
    border: 1px solid var(--border);
    background: var(--surface);
    border-radius: 10px;
    padding: 1.4rem;
    transition: all 0.25s;
    position: relative;
    overflow: hidden;
  }

  .feat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 3px;
    height: 100%;
  }

  .feat-card.green::before { background: var(--accent); }
  .feat-card.red::before { background: var(--accent2); }
  .feat-card.yellow::before { background: var(--accent3); }
  .feat-card.blue::before { background: var(--accent4); }

  .feat-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 30px rgba(0,0,0,0.4);
  }

  .feat-title {
    font-family: 'Syne', sans-serif;
    font-size: 0.95rem;
    font-weight: 700;
    color: #fff;
    margin-bottom: 0.4rem;
    display: flex;
    align-items: center;
    gap: 0.5rem;
  }

  .feat-tag {
    font-size: 0.55rem;
    padding: 0.15rem 0.5rem;
    border-radius: 20px;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-weight: 700;
  }

  .feat-tag.green { background: rgba(0,255,136,0.15); color: var(--accent); }
  .feat-tag.red { background: rgba(255,56,100,0.15); color: var(--accent2); }
  .feat-tag.yellow { background: rgba(255,190,0,0.15); color: var(--accent3); }
  .feat-tag.blue { background: rgba(79,142,247,0.15); color: var(--accent4); }

  .feat-desc {
    font-size: 0.7rem;
    color: var(--muted);
    line-height: 1.65;
    margin-bottom: 0.6rem;
  }

  .feat-irony {
    font-size: 0.65rem;
    color: var(--accent3);
    font-style: italic;
    border-top: 1px solid var(--border);
    padding-top: 0.6rem;
    line-height: 1.5;
  }

  .feat-irony::before {
    content: '☞ ';
    color: var(--accent2);
  }

  .feat-code {
    font-size: 0.6rem;
    background: rgba(0,0,0,0.4);
    border-radius: 4px;
    padding: 0.5rem 0.75rem;
    margin: 0.5rem 0;
    color: var(--accent);
    border-left: 2px solid var(--accent);
    overflow-x: auto;
    white-space: pre;
  }

  /* CASES TABLE */
  .cases-section { display: flex; flex-direction: column; gap: 1.5rem; }

  .case-block {
    border: 1px solid var(--border);
    background: var(--surface);
    border-radius: 10px;
    overflow: hidden;
  }

  .case-header {
    padding: 0.9rem 1.4rem;
    display: flex;
    align-items: center;
    gap: 1rem;
    border-bottom: 1px solid var(--border);
  }

  .case-num {
    font-family: 'Syne', sans-serif;
    font-size: 1.3rem;
    font-weight: 800;
    opacity: 0.3;
    min-width: 2rem;
  }

  .case-title {
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 700;
    color: #fff;
  }

  .case-body {
    padding: 1rem 1.4rem;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  @media (max-width: 600px) { .case-body { grid-template-columns: 1fr; } }

  .case-what, .case-irony-block {
    font-size: 0.7rem;
    line-height: 1.75;
  }

  .case-what strong { color: var(--accent4); display: block; font-size: 0.6rem; letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 0.3rem; }
  .case-irony-block strong { color: var(--accent2); display: block; font-size: 0.6rem; letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 0.3rem; }
  .case-irony-block { color: var(--accent3); font-style: italic; }

  /* STAT TABLE */
  .stat-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 0.7rem;
  }

  .stat-table th {
    text-align: left;
    padding: 0.7rem 1rem;
    border-bottom: 1px solid var(--border);
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    font-size: 0.6rem;
    font-weight: 400;
  }

  .stat-table td {
    padding: 0.75rem 1rem;
    border-bottom: 1px solid rgba(42,42,58,0.5);
    vertical-align: top;
    line-height: 1.6;
  }

  .stat-table tr:last-child td { border-bottom: none; }

  .stat-table tr:hover td { background: rgba(255,255,255,0.02); }

  .plus { color: var(--accent); }
  .minus { color: var(--accent2); }

  .action-icon {
    font-size: 1.1rem;
    margin-right: 0.4rem;
  }

  /* SCORE SECTION */
  .formula-box {
    background: rgba(0,0,0,0.5);
    border: 1px solid var(--accent3);
    border-radius: 8px;
    padding: 1.5rem;
    font-size: 0.75rem;
    line-height: 2;
    margin-bottom: 1.5rem;
    text-align: center;
  }

  .formula {
    font-family: 'Syne', sans-serif;
    font-size: 1.1rem;
    font-weight: 700;
    color: var(--accent3);
    letter-spacing: 0.05em;
  }

  .endings-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 1rem;
  }

  .ending-card {
    border-radius: 8px;
    padding: 1.2rem;
    border: 1px solid;
  }

  .ending-card.weapon { border-color: var(--accent); background: rgba(0,255,136,0.05); }
  .ending-card.panic  { border-color: var(--accent2); background: rgba(255,56,100,0.05); }
  .ending-card.surv   { border-color: var(--accent3); background: rgba(255,190,0,0.05); }

  .ending-name {
    font-family: 'Syne', sans-serif;
    font-size: 1rem;
    font-weight: 800;
    margin-bottom: 0.5rem;
  }

  .ending-card.weapon .ending-name { color: var(--accent); }
  .ending-card.panic .ending-name  { color: var(--accent2); }
  .ending-card.surv .ending-name   { color: var(--accent3); }

  .ending-cond {
    font-size: 0.65rem;
    color: var(--muted);
    margin-bottom: 0.5rem;
  }

  .ending-irony {
    font-size: 0.65rem;
    font-style: italic;
    color: var(--accent3);
  }

  /* SECTION HEADER */
  .section-head {
    font-family: 'Syne', sans-serif;
    font-size: 0.7rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--muted);
    margin: 2rem 0 1rem;
    padding-bottom: 0.5rem;
    border-bottom: 1px solid var(--border);
  }

  /* SCROLLBAR */
  ::-webkit-scrollbar { width: 6px; height: 6px; }
  ::-webkit-scrollbar-track { background: var(--bg); }
  ::-webkit-scrollbar-thumb { background: var(--dim); border-radius: 3px; }

  /* PULSE ANIMATION */
  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  .live-dot {
    width: 6px; height: 6px;
    background: var(--accent);
    border-radius: 50%;
    display: inline-block;
    animation: pulse 2s infinite;
    margin-right: 0.4rem;
    box-shadow: 0 0 6px var(--accent);
  }

  .flow-section-label {
    font-size: 0.6rem;
    letter-spacing: 0.15em;
    color: var(--muted);
    text-transform: uppercase;
    margin: 0.5rem 0 0;
  }

  .node.mini {
    width: min(280px, 80vw);
    padding: 0.7rem 1rem;
  }

  .node.mini .node-label { font-size: 0.75rem; }

  .bugs-list {
    display: flex;
    flex-direction: column;
    gap: 0.7rem;
  }

  .bug-item {
    display: flex;
    gap: 1rem;
    align-items: flex-start;
    padding: 0.9rem 1.2rem;
    border: 1px solid var(--border);
    border-radius: 8px;
    background: var(--surface);
    font-size: 0.7rem;
    line-height: 1.65;
  }

  .bug-icon {
    font-size: 1.1rem;
    flex-shrink: 0;
    margin-top: 0.05rem;
  }

  .bug-name {
    font-family: 'Syne', sans-serif;
    font-weight: 700;
    color: var(--accent2);
    font-size: 0.8rem;
    margin-bottom: 0.2rem;
  }

  .bug-irony {
    color: var(--accent3);
    font-style: italic;
    margin-top: 0.3rem;
    font-size: 0.65rem;
  }

  .connector-h {
    display: flex;
    align-items: center;
    gap: 0;
    width: 100%;
    max-width: 700px;
  }

  .h-arrow {
    flex: 1;
    height: 1px;
    background: var(--dim);
    position: relative;
  }

  .h-arrow::after {
    content: '▶';
    position: absolute;
    right: -6px;
    top: 50%;
    transform: translateY(-50%);
    color: var(--dim);
    font-size: 0.6rem;
  }

  .h-arrow.left::after {
    content: '◀';
    right: auto;
    left: -6px;
  }
</style>
</head>
<body>

<header>
  <div class="title">STUDENT LIFE SIM <span>— DECODED</span></div>
  <div class="subtitle"><span class="live-dot"></span>Full Program Flow · Features · Irony Factor · Bugs</div>
</header>

<div class="tabs">
  <button class="tab active" onclick="switchTab('flow')">📊 Full Flow</button>
  <button class="tab" onclick="switchTab('features')">⚙️ Features</button>
  <button class="tab" onclick="switchTab('cases')">🔀 Cases</button>
  <button class="tab" onclick="switchTab('actions')">🎮 Actions & Stats</button>
  <button class="tab" onclick="switchTab('score')">🏆 Score & Endings</button>
  <button class="tab" onclick="switchTab('bugs')">🐛 Bugs & Irony</button>
</div>

<!-- ══════════════ TAB: FLOW ══════════════ -->
<div class="panel active" id="panel-flow">
<div class="container">
<div class="flow-wrap">

  <!-- START -->
  <div class="node start">
    <div class="node-label">🚀 Program Starts → main()</div>
    <div class="node-irony">The journey begins. Your GPA hasn't suffered yet.</div>
    <div class="node-code">clear_screen() · srand(time(0)) · print title</div>
  </div>

  <div class="arrow"></div>

  <div class="node action">
    <div class="node-label">👤 Player Enters Name</div>
    <div class="node-irony">scanf("%s") — spaces in your name? Doesn't exist.</div>
    <div class="node-code">scanf("%s", current_name)</div>
  </div>

  <div class="arrow"></div>

  <div class="node action">
    <div class="node-label">📂 fopen(SAVE_FILE, "r")</div>
    <div class="node-irony">The moment of truth. Does "student_data.txt" exist?</div>
    <div class="node-code">file = fopen("student_data.txt", "r")</div>
  </div>

  <div class="arrow"></div>

  <!-- DECISION: File Exists? -->
  <div class="node decision">
    <div class="node-label">file == NULL?</div>
  </div>

  <div style="display:flex; flex-direction:column; align-items:center; width:100%; max-width:900px;">
    <!-- Branch row -->
    <div style="display:flex; width:100%; justify-content:center; position:relative; height:20px;">
      <div style="position:absolute; left:50%; top:0; width:300px; height:1px; background:var(--dim); transform:translateX(-50%)"></div>
    </div>

    <div class="branch">
      <!-- LEFT: YES - new game -->
      <div class="branch-arm">
        <div class="branch-label yes">YES → New Game</div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">🆕 Welcome New Player</div>
          <div class="node-irony">No baggage. No save. No trauma. Yet.</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">🎮 Pick Mode</div>
          <div class="node-irony">1=Speedrun · 2=Realism (24hr suffering)</div>
        </div>
      </div>

      <!-- RIGHT: NO - file exists -->
      <div class="branch-arm">
        <div class="branch-label no">NO → File Exists</div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">📖 fscanf → saved_name</div>
          <div class="node-irony">Reading who this save belongs to.</div>
        </div>
        <div class="arrow"></div>
        <div class="node decision" style="height:100px; width:min(240px,80vw)">
          <div class="node-label" style="font-size:0.65rem;">strcmp match?</div>
        </div>
        <div class="arrow"></div>
        <div class="branch">
          <div class="branch-arm">
            <div class="branch-label match">MATCH</div>
            <div class="arrow"></div>
            <div class="node mini action">
              <div class="node-label">✅ Load All Stats</div>
              <div class="node-irony">Day, energy, stress, history — all restored.</div>
            </div>
            <div class="arrow"></div>
            <div class="node mini action">
              <div class="node-label">⏱️ Cooldown Check</div>
              <div class="node-irony">difftime() — did you wait 24hrs?</div>
            </div>
          </div>
          <div class="branch-arm">
            <div class="branch-label mismatch">MISMATCH</div>
            <div class="arrow"></div>
            <div class="node mini bad">
              <div class="node-label">🚨 Identity Alert</div>
              <div class="node-irony">"ALERT: File belongs to X, but you are Y."</div>
            </div>
            <div class="arrow"></div>
            <div class="node mini action">
              <div class="node-label">Delete & Restart or Exit</div>
              <div class="node-irony">Congrats on wiping your roommate's save.</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="arrow"></div>

  <!-- GAME OVER CHECK -->
  <div class="node decision">
    <div class="node-label">day > 5?</div>
  </div>

  <div style="display:flex; width:100%; max-width:800px; justify-content:center;">
    <div class="branch">
      <div class="branch-arm">
        <div class="branch-label yes">YES → Game Over</div>
        <div class="arrow"></div>
        <div class="node mini end">
          <div class="node-label">📊 Print ASCII Graph</div>
          <div class="node-irony">5 days of productivity in hashtags.</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini end">
          <div class="node-label">🧮 Regret Formula</div>
          <div class="node-irony">(100-productivity) + stress - (happiness/2)</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini end">
          <div class="node-label">🏅 Print Identity + Exit</div>
          <div class="node-irony">Academic Weapon / Panic Master / Survivor</div>
        </div>
      </div>

      <div class="branch-arm">
        <div class="branch-label no">NO → Play Today</div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">🖥️ Print Day Stats</div>
          <div class="node-irony">Mood, Energy, Theme, System Analysis</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">⚡ Energy Check</div>
          <div class="node-irony">energy ≤ 0 → forced sleep. No input for you.</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">🎮 Show Action Menu</div>
          <div class="node-irony">Study / Reels / Game / Sleep / Hangout / Exit</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">💥 Streak Bonus Check</div>
          <div class="node-irony">Studied yesterday too? +10 bonus, nerd.</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">📈 Apply switch() Effects</div>
          <div class="node-irony">Stats change. No clamps. Chaos possible.</div>
        </div>
        <div class="arrow"></div>
        <div class="node mini action">
          <div class="node-label">💾 Save to File + day++</div>
          <div class="node-irony">fprintf() — overwrites everything. See you tomorrow.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="arrow"></div>
  <div class="node end">
    <div class="node-label">return 0</div>
    <div class="node-irony">One terminal run = one day of the student's life.</div>
  </div>

</div>
</div>
</div>

<!-- ══════════════ TAB: FEATURES ══════════════ -->
<div class="panel" id="panel-features">
<div class="container">
<div class="features-grid">

  <div class="feat-card green">
    <div class="feat-title">💾 Save / Load System <span class="feat-tag green">Core</span></div>
    <div class="feat-desc">Persists game state in a plain text file <code>student_data.txt</code>. Every stat — day, energy, happiness, productivity, stress, last action, timestamp, mode, and both history arrays — is written via <code>fprintf</code> and read back with <code>fscanf</code> in the exact same order.</div>
    <div class="feat-code">fprintf(file, "%s %d %d %d %d %d %d %ld %d\n",
  name, day, energy, happiness,
  productivity, stress, last_action,
  current_time, cooldown_mode);</div>
    <div class="feat-irony">A plain .txt file guarding your entire academic career. Cloud backup? Never heard of her.</div>
  </div>

  <div class="feat-card blue">
    <div class="feat-title">👤 Name Authentication <span class="feat-tag blue">Security</span></div>
    <div class="feat-desc">Reads the saved name from the file and compares it to the entered name using <code>strcmp()</code>. If they don't match, it triggers an "IDENTITY ALERT" and forces the user to either wipe the old save or exit entirely.</div>
    <div class="feat-code">if (strcmp(current_name, saved_name) == 0)
  // Identity verified → load
else
  // ALERT: Who are you??</div>
    <div class="feat-irony">Military-grade authentication: just type a name. Your entire save is protected by the honor system.</div>
  </div>

  <div class="feat-card yellow">
    <div class="feat-title">⏱️ Real-Time Cooldown <span class="feat-tag yellow">Realism</span></div>
    <div class="feat-desc">In Realism mode, the game checks <code>difftime(current_time, last_played_time)</code>. If less than 86400 seconds (24 hrs) have passed since last session, you're blocked — or you can skip with cheat option 2.</div>
    <div class="feat-code">double secs = difftime(time(0), last_played_time);
if (cooldown_mode == 1 && secs < 86400)
  // Block player
  // Or let them cheat with option 2</div>
    <div class="feat-irony">The game simulates waiting to play… by making you actually wait. The cheat skip is literally labeled "for examiner."</div>
  </div>

  <div class="feat-card blue">
    <div class="feat-title">📊 5-Stat System <span class="feat-tag blue">Gameplay</span></div>
    <div class="feat-desc">Five core stats drive everything: Energy (physical capacity), Happiness (mood/morale), Productivity (academic output), Stress (burden level). All start at set values and change based on daily actions. No clamping — any stat can go negative or absurdly high.</div>
    <div class="feat-irony">Stress can go below zero. Apparently anti-stress exists if you sleep enough. Happiness can exceed 100. The student is... transcendent?</div>
  </div>

  <div class="feat-card green">
    <div class="feat-title">🔥 Study Streak Bonus <span class="feat-tag green">Mechanic</span></div>
    <div class="feat-desc">If you study (choice 1) two days in a row, you earn +10 extra productivity before the switch applies its base +20. Tracked via <code>last_action</code> saved to file each session.</div>
    <div class="feat-code">if(choice == 1 && last_action == 1)
  productivity += 10; // Streak bonus FIRST
// Then switch adds another +20</div>
    <div class="feat-irony">The only mechanic that rewards consistency. One skipped day and poof — your streak evaporates like your will to study.</div>
  </div>

  <div class="feat-card red">
    <div class="feat-title">💀 Exhaustion Auto-Skip <span class="feat-tag red">Punishment</span></div>
    <div class="feat-desc">If <code>energy ≤ 0</code>, the player literally cannot choose anything. The game auto-assigns choice 4 (Sleep), adds 50 energy, reduces stress by 10, and skips the turn entirely.</div>
    <div class="feat-code">if (energy <= 0) {
  printf("You passed out!\n");
  energy = 50;
  stress -= 10;
  choice = 4; // Forced sleep
}</div>
    <div class="feat-irony">The game force-sleeps you. Your character passes out. This is the only mechanic with realistic consequences for bad decisions.</div>
  </div>

  <div class="feat-card yellow">
    <div class="feat-title">🧠 System Analysis <span class="feat-tag yellow">Flavour</span></div>
    <div class="feat-desc">Prints a "personality diagnosis" each day based on stat combinations. Four possible states: Burnout Imminent, Procrastinator, Vibing, or Balanced.</div>
    <div class="feat-code">if (productivity > 50 && stress > 60)
  → "Burnout Imminent"
else if (energy > 70 && productivity < 10)
  → "Procrastinator"
else if (happiness > 80)
  → "Vibing"
else → "Balanced"</div>
    <div class="feat-irony">A 4-state personality analyzer. Real psychology uses decades of research. This uses two if-statements. Eerily accurate.</div>
  </div>

  <div class="feat-card green">
    <div class="feat-title">📈 ASCII Bar Graph <span class="feat-tag green">Viz</span></div>
    <div class="feat-desc">At game end, prints a terminal productivity graph using nested loops. Inner loop runs <code>hist_prod[i]/10</code> times, printing one <code>#</code> per 10 productivity points.</div>
    <div class="feat-code">for(int j=0; j < hist_prod[i]/10; j++)
  printf("#");</div>
    <div class="feat-irony">A bar chart made of hashtags, in 2024. No matplotlib. No Chart.js. Just raw hash symbols and pride.</div>
  </div>

  <div class="feat-card blue">
    <div class="feat-title">🎮 Dual Mode System <span class="feat-tag blue">Design</span></div>
    <div class="feat-desc">Two play modes. Speedrun: no cooldown, play as many days per real-time session as you want. Realism: 24hr real-world wait between days, simulating actual student time passage.</div>
    <div class="feat-irony">Realism mode makes you wait a full day between turns. Playing a student simulator is, itself, more realistic than studying.</div>
  </div>

  <div class="feat-card red">
    <div class="feat-title">🚪 Seamless Exit (No Save) <span class="feat-tag red">Secret</span></div>
    <div class="feat-desc">Choice 6 exits the program with <code>return 0</code> BEFORE saving. Nothing is written to disk. Day doesn't advance. Your stats from this session vanish completely.</div>
    <div class="feat-code">if (choice == 6) {
  printf("Exiting seamlessly...\n");
  return 0; // No save, nothing
}</div>
    <div class="feat-irony">It's marketed as "Seamless Exit" but it's actually just closing the app and pretending nothing happened. Very student energy.</div>
  </div>

  <div class="feat-card yellow">
    <div class="feat-title">🏅 3-Ending System <span class="feat-tag yellow">Narrative</span></div>
    <div class="feat-desc">Three final identities based on productivity and regret score. Academic Weapon (productivity ≥ 80), Panic Master (regret ≥ 70), or Survivor (everyone else). Checked in priority order.</div>
    <div class="feat-irony">You either win hard, fail dramatically, or just... existed for 5 days. The human condition, quantified in a single variable called "regret."</div>
  </div>

  <div class="feat-card red">
    <div class="feat-title">🗑️ Save Wipe on Exit <span class="feat-tag red">Nuclear</span></div>
    <div class="feat-desc">After the final report, choice 1 calls <code>remove(SAVE_FILE)</code> which deletes <code>student_data.txt</code> from disk permanently. No confirmation beyond the single menu option.</div>
    <div class="feat-code">if(wipe == 1) remove(SAVE_FILE);</div>
    <div class="feat-irony">Five days of your virtual life. One keystroke. Gone. The file system has no "are you sure?" dialog. Neither does regret.</div>
  </div>

</div>
</div>
</div>

<!-- ══════════════ TAB: CASES ══════════════ -->
<div class="panel" id="panel-cases">
<div class="container">
<div class="cases-section">

  <div class="case-block">
    <div class="case-header" style="border-left:3px solid var(--accent)">
      <div class="case-num" style="color:var(--accent)">01</div>
      <div class="case-title">Brand New Player — No Save File</div>
    </div>
    <div class="case-body">
      <div class="case-what">
        <strong>What Happens</strong>
        fopen() returns NULL. Program prints "New System Detected." Player picks mode (Speedrun or Realism). All stats use hardcoded defaults: energy=80, happiness=50, productivity=0, stress=10, day=1. No file is read. New game begins from scratch.
      </div>
      <div class="case-irony-block">
        <strong>Irony Factor</strong>
        The "New System Detected" message makes it sound like military onboarding. You are not enrolling in a special program. You just don't have a .txt file yet.
      </div>
    </div>
  </div>

  <div class="case-block">
    <div class="case-header" style="border-left:3px solid var(--accent4)">
      <div class="case-num" style="color:var(--accent4)">02</div>
      <div class="case-title">Returning Player — Same Name, Speedrun Mode</div>
    </div>
    <div class="case-body">
      <div class="case-what">
        <strong>What Happens</strong>
        fopen() succeeds. fscanf reads saved_name. strcmp matches. All 8 stats + 10 history values loaded. cooldown_mode = 1 not triggered (it's 0/Speedrun). "Identity Verified. Welcome back!" printed. Player immediately enters today's session. No waiting.
      </div>
      <div class="case-irony-block">
        <strong>Irony Factor</strong>
        "Identity Verified" — like a bank. Your identity is verified by typing the same first name you typed last time. Biometrics? No. A single scanf? Yes.
      </div>
    </div>
  </div>

  <div class="case-block">
    <div class="case-header" style="border-left:3px solid var(--accent3)">
      <div class="case-num" style="color:var(--accent3)">03</div>
      <div class="case-title">Returning Player — Same Name, Realism Mode, Within 24hrs</div>
    </div>
    <div class="case-body">
      <div class="case-what">
        <strong>What Happens</strong>
        Save loads. difftime() calculates seconds since last play. If &lt;86400 seconds have passed AND cooldown_mode == 1 (Realism), the remaining hours are shown. Player gets: 1=Exit (return 0), 2=Cheat Skip (continues). If they wait, the game blocks them completely.
      </div>
      <div class="case-irony-block">
        <strong>Irony Factor</strong>
        The game enforces rest. You chose Realism mode to simulate student life and now the simulation is telling you to go touch grass. The cheat is literally commented "Cheat for Examiner" in the source code.
      </div>
    </div>
  </div>

  <div class="case-block">
    <div class="case-header" style="border-left:3px solid var(--accent2)">
      <div class="case-num" style="color:var(--accent2)">04</div>
      <div class="case-title">Returning Player — Wrong Name (Identity Mismatch)</div>
    </div>
    <div class="case-body">
      <div class="case-what">
        <strong>What Happens</strong>
        fopen() succeeds. saved_name read. strcmp FAILS. "ALERT: Saved file belongs to X, but you are Y." Two options: (1) Delete old save, start fresh as new player, pick new mode. (2) Exit. If choice 1, fclose() called, day reset to 1, variables stay default.
      </div>
      <div class="case-irony-block">
        <strong>Irony Factor</strong>
        The entire "security system" can be bypassed by just typing someone else's name. To steal their save: type their name. There is no password. The game calls it an "ALERT." It's just an if-statement.
      </div>
    </div>
  </div>

  <div class="case-block">
    <div class="case-header" style="border-left:3px solid var(--accent)">
      <div class="case-num" style="color:var(--accent)">05</div>
      <div class="case-title">Energy Collapse — Player is at 0 Energy</div>
    </div>
    <div class="case-body">
      <div class="case-what">
        <strong>What Happens</strong>
        Before showing the menu, energy is checked. If ≤ 0: "You passed out!" is printed, energy resets to 50, stress decreases by 10, and choice is force-set to 4 (Sleep). The switch still runs with choice=4, adding another +30 energy and -10 stress. Player never sees the menu.
      </div>
      <div class="case-irony-block">
        <strong>Irony Factor</strong>
        The only time the game takes control away from you is when you've destroyed yourself. Free will exists until it doesn't. Very realistic college experience.
      </div>
    </div>
  </div>

  <div class="case-block">
    <div class="case-header" style="border-left:3px solid var(--accent3)">
      <div class="case-num" style="color:var(--accent3)">06</div>
      <div class="case-title">Day 6 Launch — Game Over Sequence</div>
    </div>
    <div class="case-body">
      <div class="case-what">
        <strong>What Happens</strong>
        If saved day > 5 on load, entire play section is skipped. ASCII graph prints using hist_prod[] array. Regret formula calculated. Identity printed. Option to wipe file with remove() or just exit with return 0. The game is permanently over unless the save is wiped.
      </div>
      <div class="case-irony-block">
        <strong>Irony Factor</strong>
        Five days of college. The entire academic career of this student fits in a .txt file smaller than a meme image. "Total Regret Score" is a real variable. The programmers knew.
      </div>
    </div>
  </div>

  <div class="case-block">
    <div class="case-header" style="border-left:3px solid var(--dim)">
      <div class="case-num">07</div>
      <div class="case-title">Seamless Exit — Choice 6</div>
    </div>
    <div class="case-body">
      <div class="case-what">
        <strong>What Happens</strong>
        Player picks 6 from action menu. Program prints "Exiting seamlessly... See you later!" and hits return 0. Absolutely nothing is saved. Day doesn't increment. Stats don't change. The save file retains whatever was there before. Next launch = same day replayed.
      </div>
      <div class="case-irony-block">
        <strong>Irony Factor</strong>
        "Seamless exit" is just... quitting without consequences. In real life this would be skipping class. In the simulator, it literally is skipping class. Accidentally discovered infinite day glitch.
      </div>
    </div>
  </div>

</div>
</div>
</div>

<!-- ══════════════ TAB: ACTIONS ══════════════ -->
<div class="panel" id="panel-actions">
<div class="container">

  <p class="section-head">What each action actually does to your stats</p>

  <table class="stat-table">
    <thead>
      <tr>
        <th>Action</th>
        <th>Energy</th>
        <th>Happiness</th>
        <th>Productivity</th>
        <th>Stress</th>
        <th>Net Verdict</th>
        <th>Irony</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><span class="action-icon">📚</span><strong>Study</strong></td>
        <td class="minus">−20</td>
        <td class="minus">−5</td>
        <td class="plus">+20 (+10 streak)</td>
        <td class="minus" style="color:var(--accent2)">+10 ⚠️</td>
        <td>The only way to win. Also the only way to suffer.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Good grades require unhappiness. The simulation is painfully accurate.</td>
      </tr>
      <tr>
        <td><span class="action-icon">📱</span><strong>Reels</strong></td>
        <td class="minus">−10</td>
        <td class="plus">+10</td>
        <td>—</td>
        <td class="minus" style="color:var(--accent2)">+5 ⚠️</td>
        <td>Feels good. Gets worse. Zero output.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Even doom-scrolling increases stress. The programmer knew about doomscrolling anxiety.</td>
      </tr>
      <tr>
        <td><span class="action-icon">🎮</span><strong>Game</strong></td>
        <td class="minus">−15</td>
        <td class="plus">+15</td>
        <td>—</td>
        <td class="plus">−5</td>
        <td>Best stress reliever. No academic value.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Gaming actually reduces stress unlike reels. The programmer is a gamer and it shows.</td>
      </tr>
      <tr>
        <td><span class="action-icon">😴</span><strong>Sleep</strong></td>
        <td class="plus">+30</td>
        <td>—</td>
        <td>—</td>
        <td class="plus">−10</td>
        <td>Pure recovery. No happiness. No work. Just rest.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Sleep gives you the most energy AND reduces most stress. Healthy habits simulator hidden inside student disaster simulator.</td>
      </tr>
      <tr>
        <td><span class="action-icon">🤝</span><strong>Hangout</strong></td>
        <td class="minus">−10</td>
        <td class="plus">+20</td>
        <td class="minus">−5 ⚠️</td>
        <td>—</td>
        <td>Maximum happiness. Costs you grades.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Having friends actively makes you dumber. Your GPA disagrees with your social life. As intended.</td>
      </tr>
      <tr>
        <td><span class="action-icon">🚪</span><strong>Exit App</strong></td>
        <td>—</td>
        <td>—</td>
        <td>—</td>
        <td>—</td>
        <td>return 0. Nothing changes. Day replays.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Infinite mulligan. Day 3 forever. The ultimate procrastination tool inside a procrastination simulator.</td>
      </tr>
    </tbody>
  </table>

  <p class="section-head" style="margin-top:2.5rem">The Mood Display Logic (Priority Order)</p>
  <table class="stat-table">
    <thead>
      <tr><th>Priority</th><th>Condition</th><th>Mood Shown</th><th>Irony</th></tr>
    </thead>
    <tbody>
      <tr>
        <td>1st</td>
        <td>stress > 60</td>
        <td>😰 STRESSED</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Stress overrides everything. Even if you're happy and energetic, high stress = you're STRESSED. Sounds right.</td>
      </tr>
      <tr>
        <td>2nd</td>
        <td>energy &lt; 20</td>
        <td>😴 TIRED</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">You can be happy and tired simultaneously but the game only shows one. It picks tired. Mood is not a boolean.</td>
      </tr>
      <tr>
        <td>3rd</td>
        <td>else</td>
        <td>😊 HAPPY</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Default mood is "happy." Optimistic default value in a game literally called Student Life Simulator.</td>
      </tr>
    </tbody>
  </table>

  <p class="section-head" style="margin-top:2.5rem">System Analysis Diagnoses</p>
  <table class="stat-table">
    <thead>
      <tr><th>Condition</th><th>Diagnosis</th><th>Irony</th></tr>
    </thead>
    <tbody>
      <tr>
        <td>productivity > 50 AND stress > 60</td>
        <td>🔥 Burnout Imminent</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Working hard but dying inside. The game notices this. Your advisor does not.</td>
      </tr>
      <tr>
        <td>energy > 70 AND productivity &lt; 10</td>
        <td>💤 Procrastinator</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Full energy, zero output. The simulator calls you out by name.</td>
      </tr>
      <tr>
        <td>happiness > 80</td>
        <td>🎉 Vibing</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">"Grades might drop but you're happy." The most honest line in the entire program.</td>
      </tr>
      <tr>
        <td>everything else</td>
        <td>⚖️ Balanced</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Not happy enough to be Vibing. Not hard-working enough for Burnout. The median student experience: vaguely okay.</td>
      </tr>
    </tbody>
  </table>

</div>
</div>

<!-- ══════════════ TAB: SCORE ══════════════ -->
<div class="panel" id="panel-score">
<div class="container">

  <div class="formula-box">
    <div style="font-size:0.65rem; color:var(--muted); letter-spacing:0.15em; text-transform:uppercase; margin-bottom:0.75rem">The Regret Formula</div>
    <div class="formula">REGRET = (100 − productivity) + stress − (happiness ÷ 2)</div>
    <div style="font-size:0.7rem; color:var(--muted); margin-top:1rem; line-height:1.8">
      if regret &lt; 0 → clamped to 0 &nbsp;|&nbsp; not clamped at max &nbsp;|&nbsp; theoretical max ≈ 100+60−0 = 160
    </div>
  </div>

  <div style="background:var(--surface); border:1px solid var(--border); border-radius:8px; padding:1.4rem; margin-bottom:1.5rem; font-size:0.72rem; line-height:1.9;">
    <div style="font-family:'Syne',sans-serif; font-weight:700; font-size:0.85rem; color:#fff; margin-bottom:0.75rem;">How Each Term Affects You</div>
    <div><span class="minus">● (100 − productivity)</span> — If you did zero work, this contributes a full 100 points to regret. Every study session chips away at this.</div>
    <div><span style="color:var(--accent2)">● + stress</span> — Stress directly adds to regret. Studying hard but stressing about it makes regret worse, not better.</div>
    <div><span class="plus">● − (happiness ÷ 2)</span> — Happiness halved because it's a weak buffer. Maximum happiness (say 100) only offsets 50 regret points.</div>
    <div style="margin-top:0.5rem; color:var(--accent3); font-style:italic;">The irony: studying raises productivity (lowers regret) but also raises stress (raises regret). You can't win cleanly.</div>
  </div>

  <p class="section-head">The Three Endings</p>
  <div class="endings-grid">

    <div class="ending-card weapon">
      <div class="ending-name">⚔️ Academic Weapon</div>
      <div class="ending-cond">Requires: productivity ≥ 80</div>
      <div style="font-size:0.68rem; color:var(--muted); margin-bottom:0.6rem; line-height:1.7;">
        Must study 4 out of 5 days (4×20=80). With streak bonuses, achievable in 3+. Checked first — even high regret players get this if productivity hits 80.
      </div>
      <div class="ending-irony">The only ending with no irony. You just grinded. Congratulations. You are the reason grade curves exist.</div>
    </div>

    <div class="ending-card panic">
      <div class="ending-name">😱 Panic Master</div>
      <div class="ending-cond">Requires: regret ≥ 70 (and productivity &lt; 80)</div>
      <div style="font-size:0.68rem; color:var(--muted); margin-bottom:0.6rem; line-height:1.7;">
        High stress + low productivity = high regret. Achievable by scrolling reels all week. The stress alone from reels (+5/day × 5 = 25) can push you here.
      </div>
      <div class="ending-irony">You mastered panic. Not studying. Not relaxing. Just the panic itself. This should be on a resume.</div>
    </div>

    <div class="ending-card surv">
      <div class="ending-name">🛡️ Survivor</div>
      <div class="ending-cond">Requires: everything else</div>
      <div style="font-size:0.68rem; color:var(--muted); margin-bottom:0.6rem; line-height:1.7;">
        Didn't grind hard enough for Academic Weapon. Didn't fail hard enough for Panic Master. Middle ground. Balanced. Boring. Sustainable.
      </div>
      <div class="ending-irony">The default ending for people who did "okay." The median. You survived. The bar was existence. You cleared it.</div>
    </div>

  </div>

  <p class="section-head" style="margin-top:2.5rem">Optimal Day-by-Day Strategy</p>
  <table class="stat-table">
    <thead>
      <tr><th>Day</th><th>Best Action</th><th>Why</th><th>Irony</th></tr>
    </thead>
    <tbody>
      <tr>
        <td>Day 1</td>
        <td>📚 Study</td>
        <td>Sets up streak for Day 2 bonus. Energy starts high at 80.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">First day motivation. Rarest of all student phenomena.</td>
      </tr>
      <tr>
        <td>Day 2</td>
        <td>📚 Study</td>
        <td>+30 productivity (20 base + 10 streak). Compounding start.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Still going. Two days in a row. Peak academic performance.</td>
      </tr>
      <tr>
        <td>Day 3</td>
        <td>😴 Sleep</td>
        <td>Energy at ~40 now. Recharge before final push. Streak breaks but stress relief is worth it.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Strategic retreat. Real students call this "self-care." It's just sleep.</td>
      </tr>
      <tr>
        <td>Day 4</td>
        <td>📚 Study</td>
        <td>+20 productivity. Rested and ready. Stress manageable.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">Back on the grind. The sleep actually worked. Who knew.</td>
      </tr>
      <tr>
        <td>Day 5</td>
        <td>📚 Study</td>
        <td>+30 (streak back if Day 4 was study). Hits 80 productivity → Academic Weapon.</td>
        <td style="font-style:italic; color:var(--accent3); font-size:0.65rem;">DEADLINE PANIC theme day. You're not panicking. You planned. You are the anomaly.</td>
      </tr>
    </tbody>
  </table>

</div>
</div>

<!-- ══════════════ TAB: BUGS & IRONY ══════════════ -->
<div class="panel" id="panel-bugs">
<div class="container">
<div class="bugs-list">

  <div class="bug-item">
    <div class="bug-icon">📊</div>
    <div>
      <div class="bug-name">No Stat Clamping</div>
      <div style="color:var(--muted)">Stats like happiness, stress, energy have no min/max bounds. Study 5 days: stress = 10+50 = 60. Scroll reels 5 days: happiness could theoretically be capped only by... nothing. Productivity can also go negative if you hangout every day (−5/day).</div>
      <div class="bug-irony">A student's stress having no upper bound is, honestly, the most realistic design choice in the entire program. Unintentional documentary.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">👻</div>
    <div>
      <div class="bug-name">Dead Variable: `event`</div>
      <div style="color:var(--muted)"><code>int event;</code> is declared at the top. It is never assigned. It is never used. It is never referenced. It exists solely in the variable declaration and nowhere else. A ghost variable from a feature that was planned and never implemented.</div>
      <div class="bug-irony">The variable is called "event." The game has no random events. The variable is a memorial to the game that could have been.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">📝</div>
    <div>
      <div class="bug-name">Buffer Overflow Risk in scanf</div>
      <div style="color:var(--muted)"><code>scanf("%s", current_name)</code> reads into a 50-char buffer with no length limit. A name longer than 49 characters writes past the array into adjacent memory — classic C buffer overflow. <code>scanf("%49s", current_name)</code> would fix it.</div>
      <div class="bug-irony">Your student's name is protected by absolutely nothing. Type 200 characters and watch adjacent variables get overwritten. Stack smashing as character customization.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">🔄</div>
    <div>
      <div class="bug-name">Infinite Day Exploit via Exit App</div>
      <div style="color:var(--muted)">Choice 6 returns 0 without saving. The day never increments. You can replay Day 3 (or any day) infinitely by always picking Exit App after seeing your stats. Combined with the streak bonus, this could be used to study, check result, exit if unsatisfied, repeat.</div>
      <div class="bug-irony">A "Seamless Exit" feature accidentally creates a save-scum exploit in a game about a student who probably save-scums real life decisions too.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">🏷️</div>
    <div>
      <div class="bug-name">No Themes for Days 2, 3, 4</div>
      <div style="color:var(--muted)">Only Day 1 ("Monday Blues") and Day 5 ("DEADLINE PANIC") have themes. Days 2, 3, and 4 print nothing for theme. The code has two separate <code>if</code> statements (not if-else), so nothing covers the middle days.</div>
      <div class="bug-irony">Days 2, 3, 4 have no identity. Just like the actual middle of a semester — a blur of vague obligation and postponed decisions.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">🔐</div>
    <div>
      <div class="bug-name">Authentication Security Theatre</div>
      <div style="color:var(--muted)">The entire "identity verification" system is defeated by knowing another player's name — which is stored in plaintext in student_data.txt, readable by anyone with file access. Type their name → full access. The "ALERT" message is cosmetic.</div>
      <div class="bug-irony">ALERT: The alert is not an alert. It is a printf. There is no lock. The save file is a .txt document sitting in the working directory. Security through ambiguity — they hid it by calling it student_data.txt instead of passwords.txt.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">💤</div>
    <div>
      <div class="bug-name">Double Sleep Recovery on Exhaustion</div>
      <div style="color:var(--muted)">When energy ≤ 0, the code sets energy = 50, stress −= 10, and choice = 4. Then the switch ALSO runs case 4 (Sleep), adding +30 energy and −10 more stress. So exhaustion gives you 80 energy and −20 stress. Passing out is the best recovery option.</div>
      <div class="bug-irony">Collapsing from exhaustion gives you more energy recovery than voluntarily sleeping. The optimal strategy is to run yourself into the ground. This is the college experience.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">🎲</div>
    <div>
      <div class="bug-name">srand() Called but rand() Never Used</div>
      <div style="color:var(--muted)"><code>srand(time(0))</code> seeds the random number generator at startup. <code>rand()</code> is never called anywhere in the program. The dead <code>event</code> variable was probably meant to hold a random daily event. Both are relics of a scrapped feature.</div>
      <div class="bug-irony">The game seeds randomness and then decides everything deterministically. Like a student who buys a planner and never opens it. The chaos was ready. It was never needed.</div>
    </div>
  </div>

  <div class="bug-item">
    <div class="bug-icon">📅</div>
    <div>
      <div class="bug-name">Productivity Graph Uses Stale Data</div>
      <div style="color:var(--muted)">hist_prod[day-1] is set to productivity at the END of each day. But productivity is a cumulative total, not a per-day value. So Day 3's bar shows total productivity after 3 days, not just Day 3's contribution. The graph represents a running total, not daily output.</div>
      <div class="bug-irony">The "productivity per day" graph is actually a "productivity so far" graph. The student's greatest achievement: a chart that looks like an upward trend even when you did nothing on Day 4.</div>
    </div>
  </div>

</div>
</div>
</div>

<script>
function switchTab(name) {
  document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
  document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
  document.querySelector(`[onclick="switchTab('${name}')"]`).classList.add('active');
  document.getElementById(`panel-${name}`).classList.add('active');
  window.scrollTo({top: 0, behavior: 'smooth'});
}
</script>

</body>
</html>
