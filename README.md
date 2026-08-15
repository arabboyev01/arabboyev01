<!-- HEADER SECTION -->
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Abbosbek Arabboyev — Architect &amp; Full-Stack Engineer</title>
<meta name="description" content="Abbosbek Arabboyev — Senior Full-Stack Engineer &amp; AI Systems Developer. Engineering high-availability cloud platforms and clean UI ecosystems.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Sans:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0D1117;
    --surface:#141B26;
    --surface-2:#1B2432;
    --line:#26303F;
    --ink:#ECEDEE;
    --ink-dim:#8B94A3;
    --gold:#E8A33D;
    --blue:#5B8DEF;
    --radius:2px;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--bg);
    background-image:
      linear-gradient(var(--line) 1px, transparent 1px),
      linear-gradient(90deg, var(--line) 1px, transparent 1px);
    background-size:48px 48px;
    background-position:-1px -1px;
    color:var(--ink);
    font-family:'IBM Plex Sans', sans-serif;
    line-height:1.6;
  }

  a{color:inherit;}
  ::selection{background:var(--gold);color:#0D1117;}

  a:focus-visible, button:focus-visible{
    outline:2px solid var(--gold);
    outline-offset:3px;
  }

  .wrap{max-width:1080px;margin:0 auto;padding:0 28px;}

  .eyebrow{
    font-family:'IBM Plex Mono', monospace;
    font-size:12px;
    letter-spacing:.14em;
    text-transform:uppercase;
    color:var(--gold);
  }

  h1,h2,h3{
    font-family:'Space Grotesk', sans-serif;
    font-weight:600;
    margin:0;
    letter-spacing:-0.01em;
  }

  /* ---------- NAV ---------- */
  header{
    position:sticky;top:0;z-index:50;
    background:rgba(13,17,23,.86);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--line);
  }
  nav.wrap{
    display:flex;align-items:center;justify-content:space-between;
    height:64px;
  }
  .brand{
    font-family:'IBM Plex Mono', monospace;
    font-size:14px;font-weight:500;
    display:flex;align-items:center;gap:8px;
  }
  .brand .dot{width:8px;height:8px;background:var(--gold);border-radius:50%;
    box-shadow:0 0 0 4px rgba(232,163,61,.15);
  }
  .navlinks{display:flex;gap:28px;font-size:14px;color:var(--ink-dim);}
  .navlinks a{text-decoration:none;transition:color .2s ease;}
  .navlinks a:hover{color:var(--gold);}
  @media (max-width:640px){.navlinks{display:none;}}

  /* ---------- HERO / SCHEMATIC ---------- */
  .hero{padding:96px 0 72px;position:relative;}
  .hero-grid{
    display:grid;
    grid-template-columns:1.1fr .9fr;
    gap:48px;
    align-items:center;
  }
  @media (max-width:860px){.hero-grid{grid-template-columns:1fr;}}

  .hero h1{font-size:clamp(38px,5.4vw,64px);line-height:1.04;}
  .hero h1 .accent{color:var(--gold);}
  .hero .role{
    font-family:'IBM Plex Mono', monospace;
    color:var(--blue);
    font-size:15px;
    margin-top:14px;
  }
  .hero p.lede{
    color:var(--ink-dim);
    max-width:46ch;
    margin-top:20px;
    font-size:16px;
  }
  .hero-actions{display:flex;gap:14px;margin-top:32px;flex-wrap:wrap;}
  .btn{
    font-family:'IBM Plex Mono', monospace;
    font-size:13px;
    padding:12px 20px;
    border-radius:var(--radius);
    text-decoration:none;
    border:1px solid var(--line);
    transition:border-color .2s ease, transform .15s ease, background .2s ease;
    display:inline-flex;align-items:center;gap:8px;
  }
  .btn-primary{background:var(--gold);color:#0D1117;border-color:var(--gold);font-weight:600;}
  .btn-primary:hover{transform:translateY(-2px);}
  .btn-ghost:hover{border-color:var(--gold);color:var(--gold);transform:translateY(-2px);}

  /* schematic svg */
  .schematic{width:100%;height:auto;}
  .schematic .node-circle{fill:var(--surface-2);stroke:var(--line);stroke-width:1.5;}
  .schematic .node-circle.center{stroke:var(--gold);}
  .schematic text{
    font-family:'IBM Plex Mono', monospace;
    fill:var(--ink-dim);
    font-size:11px;
  }
  .schematic text.center-label{fill:var(--ink);font-size:12px;font-weight:600;}
  .schematic .link{
    fill:none;stroke:var(--blue);stroke-width:1.4;opacity:.55;
    stroke-dasharray:340;stroke-dashoffset:340;
    animation:draw 1.6s ease forwards;
  }
  .schematic .pulse{
    fill:var(--gold);
    animation:pulse 2.6s ease-in-out infinite;
  }
  @keyframes draw{to{stroke-dashoffset:0;}}
  @keyframes pulse{
    0%,100%{opacity:.25;r:2.2;}
    50%{opacity:1;r:3.4;}
  }
  @media (prefers-reduced-motion: reduce){
    .schematic .link{animation:none;stroke-dashoffset:0;}
    .schematic .pulse{animation:none;opacity:.8;}
  }

  /* ---------- SECTION SHELL ---------- */
  section{padding:64px 0;border-top:1px solid var(--line);}
  .section-head{display:flex;align-items:baseline;justify-content:space-between;gap:16px;margin-bottom:36px;flex-wrap:wrap;}
  .section-head h2{font-size:28px;}
  .section-head .count{font-family:'IBM Plex Mono', monospace;color:var(--ink-dim);font-size:13px;}

  /* ---------- ABOUT / TERMINAL ---------- */
  .about-grid{display:grid;grid-template-columns:1fr 1fr;gap:36px;}
  @media (max-width:800px){.about-grid{grid-template-columns:1fr;}}

  .terminal{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:6px;
    overflow:hidden;
  }
  .terminal-bar{
    display:flex;align-items:center;gap:6px;
    padding:10px 14px;
    background:var(--surface-2);
    border-bottom:1px solid var(--line);
  }
  .terminal-bar span{width:10px;height:10px;border-radius:50%;background:var(--line);}
  .terminal-bar .fname{
    margin-left:8px;font-family:'IBM Plex Mono',monospace;font-size:12px;color:var(--ink-dim);
  }
  .terminal-body{
    padding:20px;
    font-family:'IBM Plex Mono', monospace;
    font-size:13px;
    color:var(--ink-dim);
  }
  .terminal-body .k{color:var(--blue);}
  .terminal-body .v{color:var(--ink);}
  .terminal-body .comment{color:#5C6472;}
  .terminal-body p{margin:0 0 8px;}

  .about-copy p{color:var(--ink-dim);margin-bottom:16px;}
  .stat-row{display:flex;gap:28px;margin-top:24px;flex-wrap:wrap;}
  .stat{}
  .stat .num{font-family:'Space Grotesk',sans-serif;font-size:26px;font-weight:600;color:var(--gold);}
  .stat .lbl{font-family:'IBM Plex Mono', monospace;font-size:11px;color:var(--ink-dim);text-transform:uppercase;letter-spacing:.08em;}

  /* ---------- STACK ---------- */
  .stack-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
    gap:1px;
    background:var(--line);
    border:1px solid var(--line);
  }
  .stack-item{
    background:var(--surface);
    padding:20px 16px;
    text-align:center;
    transition:background .2s ease;
  }
  .stack-item:hover{background:var(--surface-2);}
  .stack-item .glyph{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;color:var(--blue);
    display:block;margin-bottom:8px;
  }
  .stack-item .name{font-size:14px;}

  /* ---------- PROJECTS ---------- */
  .proj-list{display:flex;flex-direction:column;border:1px solid var(--line);border-radius:6px;overflow:hidden;}
  .proj-row{
    display:grid;
    grid-template-columns:28px 1fr auto auto;
    gap:18px;
    align-items:center;
    padding:18px 20px;
    background:var(--surface);
    border-top:1px solid var(--line);
    text-decoration:none;
    color:var(--ink);
    transition:background .2s ease, padding-left .2s ease;
  }
  .proj-row:first-child{border-top:none;}
  .proj-row:hover{background:var(--surface-2);padding-left:26px;}
  .proj-idx{font-family:'IBM Plex Mono',monospace;color:var(--ink-dim);font-size:12px;}
  .proj-main .proj-name{font-family:'Space Grotesk',sans-serif;font-weight:600;font-size:16px;}
  .proj-main .proj-tag{font-size:12px;color:var(--ink-dim);margin-top:2px;}
  .proj-lang{
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;color:var(--ink-dim);
    display:flex;align-items:center;gap:6px;
    white-space:nowrap;
  }
  .lang-dot{width:8px;height:8px;border-radius:50%;}
  .proj-star{font-family:'IBM Plex Mono',monospace;font-size:12px;color:var(--gold);white-space:nowrap;}
  @media (max-width:640px){
    .proj-row{grid-template-columns:1fr;gap:6px;}
    .proj-idx{display:none;}
  }

  /* ---------- ACHIEVEMENTS ---------- */
  .badge-row{display:flex;gap:14px;flex-wrap:wrap;}
  .badge{
    display:flex;align-items:center;gap:10px;
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:999px;
    padding:9px 16px 9px 10px;
    font-size:13px;
  }
  .badge .ic{
    width:26px;height:26px;border-radius:50%;
    background:var(--surface-2);
    display:flex;align-items:center;justify-content:center;
    font-size:13px;
  }
  .badge .x{color:var(--gold);font-family:'IBM Plex Mono',monospace;font-size:12px;}

  /* ---------- CONTACT / FOOTER ---------- */
  .contact{
    background:var(--surface);
    border:1px solid var(--line);
    border-radius:10px;
    padding:48px;
    text-align:center;
  }
  @media (max-width:640px){.contact{padding:32px 20px;}}
  .contact h2{font-size:30px;margin-bottom:10px;}
  .contact p{color:var(--ink-dim);margin-bottom:28px;}
  .link-grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
    gap:12px;
    max-width:680px;margin:0 auto;
    text-align:left;
  }
  .link-card{
    display:flex;align-items:center;gap:10px;
    padding:14px 16px;
    border:1px solid var(--line);
    border-radius:6px;
    text-decoration:none;
    color:var(--ink);
    font-size:13px;
    transition:border-color .2s ease, transform .15s ease;
  }
  .link-card:hover{border-color:var(--gold);transform:translateY(-2px);}
  .link-card .k{color:var(--gold);font-family:'IBM Plex Mono',monospace;font-size:11px;display:block;}

  footer{
    padding:32px 0 48px;
    text-align:center;
    color:var(--ink-dim);
    font-family:'IBM Plex Mono',monospace;
    font-size:12px;
  }
</style>
</head>
<body>

<header>
  <nav class="wrap">
    <div class="brand"><span class="dot"></span> abbos.me</div>
    <div class="navlinks">
      <a href="#about">about</a>
      <a href="#stack">stack</a>
      <a href="#projects">projects</a>
      <a href="#contact">contact</a>
    </div>
  </nav>
</header>

<main>
  <section class="hero wrap" style="border-top:none;">
    <div class="hero-grid">
      <div>
        <p class="eyebrow">// system profile</p>
        <h1>Abbosbek<br>Arab<span class="accent">boyev</span></h1>
        <p class="role">ARCHITECT &amp; FULL-STACK ENGINEER — AI SYSTEMS</p>
        <p class="lede">Engineering high-availability cloud platforms and clean UI ecosystems, based in Uzbekistan.</p>
        <div class="hero-actions">
          <a class="btn btn-primary" href="#projects">View projects</a>
          <a class="btn btn-ghost" href="https://github.com/arabboyev01" target="_blank" rel="noopener">GitHub ↗</a>
          <a class="btn btn-ghost" href="#contact">Contact</a>
        </div>
      </div>

      <svg class="schematic" viewBox="0 0 420 360" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Diagram connecting Abbosbek to Frontend, Backend, Cloud, and AI Systems">
        <path class="link" d="M210,180 C170,140 130,110 90,80" style="animation-delay:.1s"/>
        <path class="link" d="M210,180 C255,140 300,110 340,70" style="animation-delay:.3s"/>
        <path class="link" d="M210,180 C170,220 120,250 80,290" style="animation-delay:.5s"/>
        <path class="link" d="M210,180 C260,220 310,250 350,300" style="animation-delay:.7s"/>

        <circle class="node-circle center" cx="210" cy="180" r="34"/>
        <text class="center-label" x="210" y="176" text-anchor="middle">ABBOS</text>
        <text x="210" y="192" text-anchor="middle" font-size="9">root</text>

        <circle class="node-circle" cx="90" cy="80" r="26"/>
        <text x="90" y="84" text-anchor="middle">Frontend</text>
        <circle class="pulse" cx="90" cy="80" r="2.5"/>

        <circle class="node-circle" cx="340" cy="70" r="26"/>
        <text x="340" y="74" text-anchor="middle">Backend</text>
        <circle class="pulse" cx="340" cy="70" r="2.5"/>

        <circle class="node-circle" cx="80" cy="290" r="26"/>
        <text x="80" y="294" text-anchor="middle">Cloud</text>
        <circle class="pulse" cx="80" cy="290" r="2.5"/>

        <circle class="node-circle" cx="350" cy="300" r="26"/>
        <text x="350" y="298" text-anchor="middle">AI</text>
        <text x="350" y="310" text-anchor="middle" font-size="9">Systems</text>
        <circle class="pulse" cx="350" cy="300" r="2.5"/>
      </svg>
    </div>
  </section>

  <section id="about">
    <div class="wrap about-grid">
      <div class="terminal">
        <div class="terminal-bar">
          <span></span><span></span><span></span>
          <span class="fname">profile.json</span>
        </div>
        <div class="terminal-body">
          <p><span class="comment">// resolved from github.com/arabboyev01</span></p>
          <p><span class="k">"name"</span>: <span class="v">"Abbosbek Arabboyev"</span></p>
          <p><span class="k">"role"</span>: <span class="v">"Software Engineer"</span></p>
          <p><span class="k">"location"</span>: <span class="v">"Uzbekistan"</span></p>
          <p><span class="k">"timezone"</span>: <span class="v">"UTC+05:00"</span></p>
          <p><span class="k">"contact"</span>: <span class="v">"contact@abbos.me"</span></p>
          <p><span class="k">"status"</span>: <span class="v">"available"</span></p>
        </div>
      </div>

      <div class="about-copy">
        <p class="eyebrow">// about</p>
        <h2 style="margin-top:10px;">Building systems that stay up.</h2>
        <p style="margin-top:16px;">Abbosbek works across the stack — from interfaces people touch every day to the cloud infrastructure that keeps them running. His focus sits at the intersection of clean UI engineering and high-availability backend architecture, with a growing line of work in AI systems.</p>
        <p>He ships publicly on GitHub, competes on LeetCode, and writes at <a href="https://abbos.me" target="_blank" rel="noopener" style="color:var(--gold);">abbos.me</a>.</p>
        <div class="stat-row">
          <div class="stat"><div class="num">15</div><div class="lbl">Repositories</div></div>
          <div class="stat"><div class="num">18</div><div class="lbl">Stars earned</div></div>
          <div class="stat"><div class="num">13</div><div class="lbl">Followers</div></div>
        </div>
      </div>
    </div>
  </section>

  <section id="stack">
    <div class="wrap">
      <div class="section-head">
        <h2>Stack</h2>
        <span class="count">languages seen across repos</span>
      </div>
      <div class="stack-grid">
        <div class="stack-item"><span class="glyph">TS</span><span class="name">TypeScript</span></div>
        <div class="stack-item"><span class="glyph">JS</span><span class="name">JavaScript</span></div>
        <div class="stack-item"><span class="glyph">&lt;/&gt;</span><span class="name">HTML</span></div>
        <div class="stack-item"><span class="glyph">{ }</span><span class="name">CSS</span></div>
      </div>
    </div>
  </section>

  <section id="projects">
    <div class="wrap">
      <div class="section-head">
        <h2>Popular repositories</h2>
        <span class="count">6 shown</span>
      </div>
      <div class="proj-list">
        <a class="proj-row" href="https://github.com/arabboyev01/Find-a-Country" target="_blank" rel="noopener">
          <span class="proj-idx">01</span>
          <span class="proj-main"><span class="proj-name">Find-a-Country</span><span class="proj-tag">Public</span></span>
          <span class="proj-lang"><span class="lang-dot" style="background:#563d7c"></span>CSS</span>
          <span class="proj-star">★ 1</span>
        </a>
        <a class="proj-row" href="https://github.com/arabboyev01/Skerio.v.1" target="_blank" rel="noopener">
          <span class="proj-idx">02</span>
          <span class="proj-main"><span class="proj-name">Skerio.v.1</span><span class="proj-tag">Forked from SayKham99/skerio</span></span>
          <span class="proj-lang"><span class="lang-dot" style="background:#f1e05a"></span>JavaScript</span>
          <span class="proj-star">★ 1</span>
        </a>
        <a class="proj-row" href="https://github.com/arabboyev01/IUL-Team" target="_blank" rel="noopener">
          <span class="proj-idx">03</span>
          <span class="proj-main"><span class="proj-name">IUL-Team</span><span class="proj-tag">Forked from Umidjon017/it-lead-team</span></span>
          <span class="proj-lang"><span class="lang-dot" style="background:#e34c26"></span>HTML</span>
          <span class="proj-star">★ 1</span>
        </a>
        <a class="proj-row" href="https://github.com/arabboyev01/medart_groupuz" target="_blank" rel="noopener">
          <span class="proj-idx">04</span>
          <span class="proj-main"><span class="proj-name">medart_groupuz</span><span class="proj-tag">Public</span></span>
          <span class="proj-lang"><span class="lang-dot" style="background:#f1e05a"></span>JavaScript</span>
          <span class="proj-star">★ 1</span>
        </a>
        <a class="proj-row" href="https://github.com/arabboyev01/trenajor-game" target="_blank" rel="noopener">
          <span class="proj-idx">05</span>
          <span class="proj-main"><span class="proj-name">trenajor-game</span><span class="proj-tag">Public</span></span>
          <span class="proj-lang"><span class="lang-dot" style="background:#3178c6"></span>TypeScript</span>
          <span class="proj-star">★ 1</span>
        </a>
        <a class="proj-row" href="https://github.com/arabboyev01/mitschool" target="_blank" rel="noopener">
          <span class="proj-idx">06</span>
          <span class="proj-main"><span class="proj-name">mitschool</span><span class="proj-tag">Public</span></span>
          <span class="proj-lang"><span class="lang-dot" style="background:#3178c6"></span>TypeScript</span>
          <span class="proj-star">★ 1</span>
        </a>
      </div>
    </div>
  </section>

  <section>
    <div class="wrap">
      <div class="section-head">
        <h2>Achievements</h2>
        <span class="count">github.com/arabboyev01?tab=achievements</span>
      </div>
      <div class="badge-row">
        <div class="badge"><span class="ic">🤝</span> Pair Extraordinaire <span class="x">×3</span></div>
        <div class="badge"><span class="ic">⚡</span> Quickdraw</div>
        <div class="badge"><span class="ic">🦈</span> Pull Shark <span class="x">×3</span></div>
        <div class="badge"><span class="ic">🎲</span> YOLO</div>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="wrap">
      <div class="contact">
        <p class="eyebrow">// connect</p>
        <h2>Let's build something reliable.</h2>
        <p>Open for full-stack, cloud, and AI systems work.</p>
        <div class="link-grid">
          <a class="link-card" href="mailto:contact@abbos.me"><div><span class="k">EMAIL</span>contact@abbos.me</div></a>
          <a class="link-card" href="https://abbos.me" target="_blank" rel="noopener"><div><span class="k">PORTFOLIO</span>abbos.me</div></a>
          <a class="link-card" href="https://github.com/arabboyev01" target="_blank" rel="noopener"><div><span class="k">GITHUB</span>@arabboyev01</div></a>
          <a class="link-card" href="https://linkedin.com/in/arabboev" target="_blank" rel="noopener"><div><span class="k">LINKEDIN</span>in/arabboev</div></a>
          <a class="link-card" href="https://leetcode.com/arabboyev_" target="_blank" rel="noopener"><div><span class="k">LEETCODE</span>arabboyev_</div></a>
          <a class="link-card" href="https://twitter.com/arabboyev_" target="_blank" rel="noopener"><div><span class="k">X / TWITTER</span>@arabboyev_</div></a>
          <a class="link-card" href="https://www.instagram.com/a.arabboev_" target="_blank" rel="noopener"><div><span class="k">INSTAGRAM</span>@a.arabboev_</div></a>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  © <span id="year"></span> Abbosbek Arabboyev — built from live GitHub profile data
</footer>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();
</script>

</body>
</html>
<!-- <div align="center">
  <samp>
    <b>ABBOSBEK ARABBOEV</b> • ARCHITECT & FULL-STACK ENGINEER
  </samp>
  <br />
  <p align="center">
    <a href="https://abbos.me">Portfolio</a> • 
    <a href="https://www.linkedin.com/in/arabboev">LinkedIn</a> • 
    <a href="https://leetcode.com/arabboyev_">LeetCode</a> • 
    <a href="https://twitter.com/arabboyev_">Twitter</a>
  </p>
  <img src="https://komarev.com/ghpvc/?username=arabboyev01&label=SYSTEM+ACCESSES&color=0F172A&style=flat-square" alt="Profile views" />
</div>

<br /> -->

<!-- TERMINAL / PROFILE BIO -->
```🚀
================================================================================
  PROFILE     :: Senior Full-Stack Engineer & AI Systems Developer
  LOCATION    :: Uzbekistan 🇺🇿
  CONTACT     :: contact@abbos.me
  MISSION     :: Engineering high-availability cloud platforms and clean UI ecosystems.
================================================================================
