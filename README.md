<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="National & international logistics, climate-controlled storage network, and secure document control services." />
  <title>Logistics • Climate-Controlled Storage • Document Control</title>

  <!--
    Cloudflare Pages / Static Hosting Notes
    - Upload this single file as index.html (or keep name and set routing).
    - No build step required.
  -->

  <style>
    :root{
      --bg:#070707;
      --panel:#0f0f0f;
      --panel2:#121212;
      --text:#f3f3f3;
      --muted:#b8b8b8;
      --yellow:#ffd400;
      --yellow2:#ffea66;
      --border:rgba(255,212,0,.18);
      --shadow: 0 18px 55px rgba(0,0,0,.55);
      --shadow2: 0 10px 28px rgba(0,0,0,.45);
      --ring: 0 0 0 3px rgba(255,212,0,.28);
      --radius: 18px;
      --radius2: 26px;
      --max: 1120px;
    }

    *{ box-sizing:border-box; }
    html,body{ height:100%; }
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      background:
        radial-gradient(900px 380px at 18% 10%, rgba(255,212,0,.18), transparent 60%),
        radial-gradient(700px 330px at 85% 12%, rgba(255,212,0,.10), transparent 62%),
        radial-gradient(900px 430px at 50% 100%, rgba(255,212,0,.08), transparent 55%),
        var(--bg);
      color:var(--text);
      line-height:1.4;
    }

    a{ color:inherit; text-decoration:none; }
    .container{ width:min(var(--max), calc(100% - 40px)); margin-inline:auto; }

    /* Header */
    header{
      position:sticky;
      top:0;
      z-index:50;
      backdrop-filter: blur(10px);
      background: rgba(7,7,7,.72);
      border-bottom:1px solid rgba(255,255,255,.06);
    }

    .nav{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:14px;
      padding:16px 0;
    }

    .brand{
      display:flex;
      align-items:center;
      gap:12px;
      font-weight:800;
      letter-spacing:.2px;
    }

    .mark{
      width:38px;
      height:38px;
      border-radius:12px;
      background: linear-gradient(135deg, var(--yellow), #ffb800);
      box-shadow: 0 10px 18px rgba(255,212,0,.18);
      position:relative;
      overflow:hidden;
    }

    .mark:before{
      content:"";
      position:absolute;
      inset:-35% -35% auto auto;
      width:75px;
      height:75px;
      background: rgba(0,0,0,.18);
      transform: rotate(20deg);
      border-radius:18px;
    }

    .brand span{ color:var(--yellow); }

    nav ul{
      list-style:none;
      display:flex;
      gap:18px;
      margin:0;
      padding:0;
      align-items:center;
    }

    nav a{
      color: var(--muted);
      font-weight:600;
      font-size: 14px;
      padding:10px 10px;
      border-radius: 12px;
      transition: all .18s ease;
    }

    nav a:hover{ color: var(--text); background: rgba(255,255,255,.05); }

    .cta{
      display:flex;
      gap:10px;
      align-items:center;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
      font-weight:800;
      border-radius: 14px;
      padding: 11px 14px;
      border: 1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.04);
      color: var(--text);
      transition: transform .15s ease, background .15s ease, border-color .15s ease;
      cursor:pointer;
      user-select:none;
      white-space:nowrap;
    }

    .btn:hover{ transform: translateY(-1px); background: rgba(255,255,255,.06); border-color: rgba(255,255,255,.12); }
    .btn:focus{ outline:none; box-shadow: var(--ring); }

    .btn.primary{
      background: linear-gradient(135deg, var(--yellow), #ffb800);
      color:#0a0a0a;
      border-color: rgba(255,212,0,.55);
      box-shadow: 0 12px 26px rgba(255,212,0,.16);
    }

    .btn.primary:hover{ background: linear-gradient(135deg, #ffde33, #ffb800); }

    .mobile-toggle{
      display:none;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(255,255,255,.04);
      border-radius: 14px;
      padding: 10px 12px;
      color: var(--text);
    }

    /* Hero */
    .hero{
      padding: 44px 0 22px;
    }

    .hero-grid{
      display:grid;
      grid-template-columns: 1.15fr .85fr;
      gap: 22px;
      align-items:stretch;
    }

    .hero-card{
      border:1px solid rgba(255,255,255,.08);
      background: linear-gradient(180deg, rgba(255,255,255,.05), rgba(255,255,255,.02));
      border-radius: var(--radius2);
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
    }

    .hero-card:before{
      content:"";
      position:absolute;
      inset:auto -20% -45% -20%;
      height: 320px;
      background: radial-gradient(circle at 50% 50%, rgba(255,212,0,.22), transparent 65%);
      filter: blur(1px);
      pointer-events:none;
    }

    .hero-inner{ padding: 30px; position:relative; }

    .kicker{
      display:inline-flex;
      align-items:center;
      gap:10px;
      padding: 8px 12px;
      border-radius: 999px;
      border:1px solid rgba(255,212,0,.22);
      background: rgba(255,212,0,.08);
      color: var(--yellow2);
      font-weight:800;
      letter-spacing:.2px;
      font-size: 13px;
    }

    .k-dot{ width:10px; height:10px; border-radius:999px; background: var(--yellow); box-shadow: 0 0 0 6px rgba(255,212,0,.12); }

    h1{
      margin: 14px 0 12px;
      font-size: clamp(30px, 4.2vw, 46px);
      line-height: 1.05;
      letter-spacing: -0.6px;
    }

    .lead{
      margin: 0 0 18px;
      color: rgba(243,243,243,.80);
      font-size: 16px;
      max-width: 60ch;
    }

    .hero-actions{ display:flex; flex-wrap:wrap; gap: 10px; margin-top: 14px; }

    .micro{
      display:flex;
      flex-wrap:wrap;
      gap: 12px 16px;
      margin-top: 18px;
      color: rgba(243,243,243,.72);
      font-weight: 600;
      font-size: 13px;
    }

    .micro .pill{
      display:inline-flex;
      align-items:center;
      gap:8px;
      padding: 8px 10px;
      border-radius: 999px;
      background: rgba(255,255,255,.04);
      border:1px solid rgba(255,255,255,.08);
    }

    .icon{
      width:18px;
      height:18px;
      display:inline-block;
      color: var(--yellow);
    }

    /* Side panel */
    .side{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius2);
      box-shadow: var(--shadow2);
      overflow:hidden;
      position:relative;
    }

    .side-header{
      padding: 18px 18px 12px;
      border-bottom: 1px solid rgba(255,255,255,.06);
      display:flex;
      align-items:flex-start;
      justify-content:space-between;
      gap: 10px;
    }

    .side-title{
      font-weight: 900;
      letter-spacing: .1px;
      font-size: 15px;
    }

    .badge{
      font-size: 12px;
      font-weight: 900;
      padding: 7px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255,212,0,.28);
      background: rgba(255,212,0,.10);
      color: var(--yellow2);
      white-space:nowrap;
    }

    .side-body{ padding: 16px 18px 18px; }

    .stat-grid{
      display:grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap: 12px;
    }

    .stat{
      padding: 14px;
      border-radius: 16px;
      border: 1px solid rgba(255,255,255,.08);
      background: rgba(0,0,0,.22);
    }

    .stat .num{
      font-weight: 950;
      font-size: 20px;
      letter-spacing: -0.3px;
      color: var(--yellow);
    }

    .stat .lbl{ color: rgba(243,243,243,.72); font-weight:700; font-size: 12px; margin-top: 6px; }

    .side-list{
      margin: 14px 0 0;
      padding: 0;
      list-style: none;
      display:grid;
      gap: 10px;
    }

    .side-list li{
      display:flex;
      gap: 10px;
      align-items:flex-start;
      padding: 12px 12px;
      border-radius: 16px;
      border: 1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
    }

    .side-list strong{ display:block; font-size: 13px; letter-spacing: .1px; }
    .side-list p{ margin: 2px 0 0; color: rgba(243,243,243,.72); font-size: 12px; }

    /* Sections */
    section{ padding: 20px 0; }

    .section-head{
      display:flex;
      align-items:flex-end;
      justify-content:space-between;
      gap: 14px;
      margin-bottom: 14px;
    }

    .section-head h2{
      margin:0;
      font-size: 20px;
      letter-spacing: -0.2px;
    }

    .section-head .sub{
      margin:0;
      color: rgba(243,243,243,.70);
      font-weight: 600;
      font-size: 13px;
      max-width: 62ch;
    }

    .cards{
      display:grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 14px;
    }

    .card{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius);
      padding: 16px;
      box-shadow: 0 8px 22px rgba(0,0,0,.32);
      position:relative;
      overflow:hidden;
    }

    .card:before{
      content:"";
      position:absolute;
      inset:auto -35% -50% -35%;
      height: 240px;
      background: radial-gradient(circle at 50% 40%, rgba(255,212,0,.16), transparent 65%);
      pointer-events:none;
    }

    .card > *{ position:relative; }

    .card h3{
      margin: 10px 0 8px;
      font-size: 16px;
      letter-spacing: -0.1px;
    }

    .card p{
      margin: 0;
      color: rgba(243,243,243,.75);
      font-size: 13px;
    }

    .card ul{
      margin: 12px 0 0;
      padding: 0 0 0 18px;
      color: rgba(243,243,243,.75);
      font-size: 13px;
    }

    .card li{ margin: 6px 0; }

    /* Capabilities */
    .cap-grid{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
    }

    .cap{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius);
      padding: 16px;
    }

    .cap h3{ margin: 0 0 10px; font-size: 16px; }

    .cap .tags{ display:flex; flex-wrap:wrap; gap:8px; }

    .tag{
      font-size: 12px;
      font-weight: 800;
      padding: 8px 10px;
      border-radius: 999px;
      border:1px solid rgba(255,255,255,.08);
      background: rgba(0,0,0,.22);
      color: rgba(243,243,243,.82);
    }

    .tag.yellow{
      border-color: rgba(255,212,0,.26);
      background: rgba(255,212,0,.10);
      color: var(--yellow2);
    }

    /* Network */
    .network{
      display:grid;
      grid-template-columns: 1.1fr .9fr;
      gap: 14px;
      align-items:stretch;
    }

    .map{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius2);
      overflow:hidden;
      box-shadow: var(--shadow2);
    }

    .map-head{
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap: 10px;
      padding: 14px 16px;
      border-bottom:1px solid rgba(255,255,255,.06);
    }

    .map-head strong{ font-size: 14px; }
    .map-head small{ color: rgba(243,243,243,.70); font-weight: 650; }

    .map-body{ padding: 14px 16px 18px; }

    .svg-wrap{
      width:100%;
      aspect-ratio: 16/9;
      border-radius: 18px;
      border:1px dashed rgba(255,212,0,.22);
      background:
        linear-gradient(180deg, rgba(0,0,0,.35), rgba(255,255,255,.02));
      display:flex;
      align-items:center;
      justify-content:center;
      position:relative;
      overflow:hidden;
    }

    .svg-wrap:before{
      content:"";
      position:absolute;
      inset: -40% -40% -40% -40%;
      background: radial-gradient(circle at 35% 40%, rgba(255,212,0,.18), transparent 55%);
      transform: rotate(-6deg);
      pointer-events:none;
    }

    .svg-wrap svg{ width: 88%; max-width: 720px; height:auto; position:relative; }

    .locator{
      fill: var(--yellow);
      stroke: rgba(0,0,0,.55);
      stroke-width: 2;
    }

    .pulse{
      fill: rgba(255,212,0,.22);
      animation: pulse 2.2s ease-in-out infinite;
      transform-origin: center;
    }

    @keyframes pulse{
      0%{ transform: scale(.86); opacity: .62; }
      55%{ transform: scale(1.12); opacity: .10; }
      100%{ transform: scale(.86); opacity: .62; }
    }

    .map-note{ margin: 12px 0 0; color: rgba(243,243,243,.72); font-size: 13px; }

    .map-note a{ color: var(--yellow2); font-weight: 800; text-decoration: underline; text-decoration-color: rgba(255,212,0,.35); }

    .quote{
      border:1px solid rgba(255,212,0,.22);
      background: rgba(255,212,0,.07);
      border-radius: var(--radius2);
      padding: 18px;
      height:100%;
      box-shadow: 0 10px 28px rgba(0,0,0,.42);
      display:flex;
      flex-direction:column;
      justify-content:space-between;
      gap: 12px;
    }

    .quote p{ margin:0; color: rgba(243,243,243,.84); font-weight: 650; }
    .quote .by{ color: rgba(243,243,243,.72); font-size: 13px; }

    /* Contact */
    .contact{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(255,255,255,.03);
      border-radius: var(--radius2);
      overflow:hidden;
      box-shadow: var(--shadow2);
    }

    .contact-grid{
      display:grid;
      grid-template-columns: 1fr 1fr;
    }

    .contact-left{ padding: 18px; border-right: 1px solid rgba(255,255,255,.06); }
    .contact-right{ padding: 18px; }

    .contact h3{ margin: 0 0 10px; }
    .contact p{ margin: 0 0 12px; color: rgba(243,243,243,.74); font-size: 13px; }

    form{ display:grid; gap: 10px; }

    label{ font-size: 12px; font-weight: 850; color: rgba(243,243,243,.78); }

    input, textarea, select{
      width:100%;
      padding: 11px 12px;
      border-radius: 14px;
      border:1px solid rgba(255,255,255,.10);
      background: rgba(0,0,0,.25);
      color: var(--text);
      font-weight: 650;
      outline:none;
      transition: box-shadow .15s ease, border-color .15s ease;
    }

    input:focus, textarea:focus, select:focus{ box-shadow: var(--ring); border-color: rgba(255,212,0,.35); }

    textarea{ min-height: 110px; resize: vertical; }

    .grid2{ display:grid; grid-template-columns: 1fr 1fr; gap: 10px; }

    .fine{
      font-size: 12px;
      color: rgba(243,243,243,.65);
      margin-top: 10px;
    }

    /* Footer */
    footer{
      padding: 24px 0 34px;
      color: rgba(243,243,243,.65);
      font-size: 13px;
      border-top: 1px solid rgba(255,255,255,.06);
      margin-top: 22px;
    }

    .foot{
      display:flex;
      gap: 14px;
      align-items:center;
      justify-content:space-between;
      flex-wrap:wrap;
    }

    .foot a{ color: rgba(243,243,243,.72); font-weight: 800; }
    .foot a:hover{ color: var(--yellow2); }

    /* Responsive */
    @media (max-width: 980px){
      .hero-grid{ grid-template-columns: 1fr; }
      .network{ grid-template-columns: 1fr; }
      .cards{ grid-template-columns: 1fr; }
      .cap-grid{ grid-template-columns: 1fr; }
      .contact-grid{ grid-template-columns: 1fr; }
      .contact-left{ border-right: none; border-bottom: 1px solid rgba(255,255,255,.06); }
      nav ul{ display:none; }
      .mobile-toggle{ display:inline-flex; }
      .cta .btn{ display:none; }
      .cta .btn.primary{ display:inline-flex; }
    }

    /* Mobile menu */
    .mobile-menu{
      display:none;
      border-top:1px solid rgba(255,255,255,.06);
      padding: 10px 0 14px;
    }
    .mobile-menu.open{ display:block; }
    .mobile-menu a{ display:block; padding: 10px 0; color: rgba(243,243,243,.82); font-weight: 800; }
    .mobile-menu a small{ display:block; color: rgba(243,243,243,.62); font-weight: 650; margin-top: 2px; }
  </style>
</head>

<body>
  <header>
    <div class="container">
      <div class="nav">
        <a class="brand" href="#top" aria-label="Home">
          <div class="mark" aria-hidden="true"></div>
          <div>
            <div>JTD<span> Group</span> </div>
            <div style="font-size:12px;color:rgba(243,243,243,.62);font-weight:650;margin-top:2px;">Freight • Storage • Document Control</div>
          </div>
        </a>

        <nav aria-label="Primary">
          <ul>
            <li><a href="#logistics">Logistics</a></li>
            <li><a href="#storage">Climate Storage</a></li>
            <li><a href="#documents">Document Control</a></li>
            <li><a href="#network">Network</a></li>
            <li><a href="#contact">Contact</a></li>
          </ul>
        </nav>

        <div class="cta">
          <button class="mobile-toggle" id="mobileToggle" aria-expanded="false" aria-controls="mobileMenu" type="button">
            ☰ Menu
          </button>
          <a class="btn" href="#contact">Request a Quote</a>
          <a class="btn primary" href="#contact">Talk to an Expert</a>
        </div>
      </div>

      <div class="mobile-menu" id="mobileMenu" aria-label="Mobile">
        <a href="#logistics">Logistics <small>Domestic + international forwarding</small></a>
        <a href="#storage">Climate Storage <small>Temperature + humidity controlled</small></a>
        <a href="#documents">Document Control <small>Secure handling + governance</small></a>
        <a href="#network">Network <small>Nationwide coverage</small></a>
        <a href="#contact">Contact <small>Quotes + onboarding</small></a>
      </div>
    </div>
  </header>

  <main id="top" class="container">
    <!-- HERO -->
    <div class="hero">
      <div class="hero-grid">
        <div class="hero-card">
          <div class="hero-inner">
            <div class="kicker"><span class="k-dot" aria-hidden="true"></span> National & International Logistics + Secure Storage</div>
            <h1>Move freight faster. Store it safer. Control documents end‑to‑end.</h1>
            <p class="lead">
              A unified network for freight forwarding, climate‑controlled warehousing, and secure document control.
              Built for regulated industries, high‑value cargo, and audit‑ready operations.
            </p>
            <div class="hero-actions">
              <a class="btn primary" href="#contact">Get a quote</a>
              <a class="btn" href="#network">Explore the network</a>
              <a class="btn" href="#documents">Compliance & controls</a>
            </div>

            <div class="micro" aria-label="Highlights">
              <div class="pill"> 
                <span class="icon" aria-hidden="true">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M3 7h18M6 7v13a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V7" stroke="currentColor" stroke-width="2" stroke-linecap="round"/><path d="M8 7l1-3h6l1 3" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
                </span>
                Climate‑controlled storage
              </div>
              <div class="pill">
                <span class="icon" aria-hidden="true">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M4 12l4-4 4 4 8-8" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/><path d="M4 20h16" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
                </span>
                SLA‑driven logistics
              </div>
              <div class="pill">
                <span class="icon" aria-hidden="true">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12 3l7 4v6c0 5-3 8-7 8s-7-3-7-8V7l7-4z" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/><path d="M9 12l2 2 4-5" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
                </span>
                Secure chain‑of‑custody
              </div>
              <div class="pill">
                <span class="icon" aria-hidden="true">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12 2v20M2 12h20" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
                </span>
                Single provider, end‑to‑end
              </div>
            </div>
          </div>
        </div>

        <aside class="side" aria-label="Service snapshot">
          <div class="side-header">
            <div>
              <div class="side-title">Service Snapshot</div>
              <div style="color:rgba(243,243,243,.68);font-weight:650;font-size:12px;margin-top:3px;">Replace placeholders with your actual network numbers.</div>
            </div>
            <div class="badge">24/7 Operations</div>
          </div>
          <div class="side-body">
            <div class="stat-grid">
              <div class="stat"><div class="num">48–72h</div><div class="lbl">Typical domestic lane turnaround</div></div>
              <div class="stat"><div class="num">2–8°C</div><div class="lbl">Cold chain storage band</div></div>
              <div class="stat"><div class="num">15–25°C</div><div class="lbl">Controlled ambient storage band</div></div>
              <div class="stat"><div class="num">99.9%</div><div class="lbl">Inventory accuracy target</div></div>
            </div>

            <ul class="side-list">
              <li>
                <span class="icon" aria-hidden="true">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M3 7h11l4 4h3v8a2 2 0 0 1-2 2H6a3 3 0 0 1-3-3V7z" stroke="currentColor" stroke-width="2" stroke-linejoin="round"/><path d="M7 20a2 2 0 1 0 0-4 2 2 0 0 0 0 4zm12 0a2 2 0 1 0 0-4 2 2 0 0 0 0 4z" stroke="currentColor" stroke-width="2"/></svg>
                </span>
                <div>
                  <strong>Freight Forwarding</strong>
                  <p>Road, air, ocean, and multimodal — customs support included.</p>
                </div>
              </li>
              <li>
                <span class="icon" aria-hidden="true">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M4 7h16v13H4V7z" stroke="currentColor" stroke-width="2"/><path d="M8 7V4h8v3" stroke="currentColor" stroke-width="2"/><path d="M7 11h10M7 14h6" stroke="currentColor" stroke-width="2" stroke-linecap="round"/></svg>
                </span>
                <div>
                  <strong>Document Control</strong>
                  <p>Secure intake, indexing, retention, and controlled access workflows.</p>
                </div>
              </li>
              <li>
                <span class="icon" aria-hidden="true">
                  <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M6 10a6 6 0 0 1 12 0v10H6V10z" stroke="currentColor" stroke-width="2"/><path d="M9 20v-6a3 3 0 0 1 6 0v6" stroke="currentColor" stroke-width="2"/></svg>
                </span>
                <div>
                  <strong>Secure Storage</strong>
                  <p>Access control, monitoring, and auditable chain‑of‑custody.</p>
                </div>
              </li>
            </ul>
          </div>
        </aside>
      </div>
    </div>

    <!-- SERVICES -->
    <section id="logistics">
      <div class="section-head">
        <div>
          <h2>National & International Logistics</h2>
          <p class="sub">Lane planning, forwarding, and execution with SLA visibility and exception management.</p>
        </div>
      </div>

      <div class="cards">
        <article class="card">
          <div class="kicker" style="padding:6px 10px;font-size:12px;">Freight Forwarding</div>
          <h3>Domestic lanes & cross‑border moves</h3>
          <p>From LTL/FTL to expedited air — aligned to time, cost, and risk profiles.</p>
          <ul>
            <li>Road, air, ocean, multimodal</li>
            <li>Customs documentation & broker coordination</li>
            <li>Visibility checkpoints & proactive ETA updates</li>
          </ul>
        </article>

        <article class="card">
          <div class="kicker" style="padding:6px 10px;font-size:12px;">Execution</div>
          <h3>Control tower operations</h3>
          <p>One team for booking, tracking, exceptions, and final‑mile confirmation.</p>
          <ul>
            <li>Milestone tracking and alerting</li>
            <li>Proof of delivery & close‑out</li>
            <li>Claims support and incident documentation</li>
          </ul>
        </article>

        <article class="card">
          <div class="kicker" style="padding:6px 10px;font-size:12px;">Special Handling</div>
          <h3>High‑value & regulated shipments</h3>
          <p>Documented handling requirements, controlled transfers, and audit‑ready records.</p>
          <ul>
            <li>Chain‑of‑custody handoffs</li>
            <li>Temperature and security requirements</li>
            <li>Specialist cross border advisors</li>
          </ul>
        </article>
      </div>
    </section>

    <section id="storage">
      <div class="section-head">
        <div>
          <h2>Climate‑Controlled Storage Network</h2>
          <p class="sub">A nationwide footprint for cold chain, controlled ambient, and secure warehousing.</p>
        </div>
      </div>

      <div class="cap-grid">
        <div class="cap">
          <h3>Storage modes</h3>
          <div class="tags">
            <span class="tag yellow">Cold chain (2–8°C)</span>
            <span class="tag">Chilled (8–15°C)</span>
            <span class="tag yellow">Controlled ambient (15–25°C)</span>
            <span class="tag">Low humidity</span>
            <span class="tag">Secure cages</span>
            <span class="tag">Pick/pack</span>
          </div>
          <p style="margin-top:12px;color:rgba(243,243,243,.74);font-size:13px;">
            Temperature and humidity monitoring, calibrated SOPs, and documented excursions handling.
          </p>
        </div>

        <div class="cap">
          <h3>Warehouse controls</h3>
          <div class="tags">
            <span class="tag">Access control</span>
            <span class="tag yellow">CCTV + audit logs</span>
            <span class="tag">Cycle counts</span>
            <span class="tag">Lot/batch tracking</span>
            <span class="tag yellow">FEFO/FIFO policies</span>
            <span class="tag">Kitting</span>
          </div>
          <p style="margin-top:12px;color:rgba(243,243,243,.74);font-size:13px;">
            Inventory governance and traceability designed for high‑assurance storage requirements.
          </p>
        </div>
      </div>
    </section>

    <section id="documents">
      <div class="section-head">
        <div>
          <h2>Secure Document Control Services</h2>
          <p class="sub">Governance, retention, controlled access, and defensible audit trails for physical and digital records.</p>
        </div>
      </div>

      <div class="cards">
        <article class="card">
          <div class="kicker" style="padding:6px 10px;font-size:12px;">Intake</div>
          <h3>Secure receiving & indexing</h3>
          <p>Structured intake with standardized metadata, barcoding, and chain‑of‑custody.</p>
          <ul>
            <li>Document classification and labeling</li>
            <li>Controlled access zones</li>
            <li>Exception tracking for missing/duplicate items</li>
          </ul>
        </article>

        <article class="card">
          <div class="kicker" style="padding:6px 10px;font-size:12px;">Retention</div>
          <h3>Retention schedules & governance</h3>
          <p>Policy‑driven retention with review workflows and defensible disposition.</p>
          <ul>
            <li>Role‑based access and approvals</li>
            <li>Audit logs for every action</li>
            <li>Legal hold support</li>
          </ul>
        </article>

        <article class="card">
          <div class="kicker" style="padding:6px 10px;font-size:12px;">Delivery</div>
          <h3>Secure retrieval & distribution</h3>
          <p>Time‑bound access, tracked release, and documented return/destruction.</p>
          <ul>
            <li>Controlled check‑out/check‑in</li>
            <li>Encrypted digital delivery options</li>
            <li>Certificate of destruction available</li>
          </ul>
        </article>
      </div>
    </section>

    <!-- NETWORK -->
    <section id="network">
      <div class="section-head">
        <div>
          <h2>Nationwide Coverage</h2>
          <p class="sub">A scalable facility network with standardized controls — ready for multi‑site rollouts and peak volumes.</p>
        </div>
      </div>

      <div class="network">
        <div class="map" aria-label="Network overview">
          <div class="map-head">
            <strong>Facility Network</strong>
            <small>Example visualization (replace with your real map)</small>
          </div>
          <div class="map-body">
            <div class="svg-wrap" role="img" aria-label="Stylized network map">
              <svg viewBox="0 0 860 480" xmlns="http://www.w3.org/2000/svg">
                <defs>
                  <linearGradient id="g" x1="0" y1="0" x2="1" y2="1">
                    <stop offset="0" stop-color="#ffd400" stop-opacity=".9"/>
                    <stop offset="1" stop-color="#ffb800" stop-opacity=".75"/>
                  </linearGradient>
                </defs>

                <!-- Stylized routes -->
                <g fill="none" stroke="url(#g)" stroke-opacity=".55" stroke-width="3" stroke-linecap="round">
                  <path d="M110 310 C 190 220, 310 210, 380 240 S 520 305, 610 260 S 740 140, 790 160"/>
                  <path d="M135 150 C 250 120, 330 140, 420 190 S 580 300, 720 330"/>
                  <path d="M210 410 C 300 330, 430 310, 520 335 S 670 410, 780 380"/>
                </g>

                <!-- Nodes (example cities/regions) -->
                <g>
                  <circle class="pulse" cx="140" cy="310" r="18"/>
                  <circle class="locator" cx="140" cy="310" r="6"/>

                  <circle class="pulse" cx="245" cy="175" r="16" style="animation-delay:.3s"/>
                  <circle class="locator" cx="245" cy="175" r="6"/>

                  <circle class="pulse" cx="380" cy="240" r="16" style="animation-delay:.6s"/>
                  <circle class="locator" cx="380" cy="240" r="6"/>

                  <circle class="pulse" cx="520" cy="335" r="16" style="animation-delay:.9s"/>
                  <circle class="locator" cx="520" cy="335" r="6"/>

                  <circle class="pulse" cx="610" cy="260" r="16" style="animation-delay:1.2s"/>
                  <circle class="locator" cx="610" cy="260" r="6"/>

                  <circle class="pulse" cx="755" cy="170" r="16" style="animation-delay:1.5s"/>
                  <circle class="locator" cx="755" cy="170" r="6"/>
                </g>

                <!-- Labels -->
                <g font-family="ui-sans-serif, system-ui" font-weight="800" font-size="14" fill="rgba(243,243,243,.82)">
                  <text x="156" y="314">West Hub</text>
                  <text x="260" y="178">North Hub</text>
                  <text x="396" y="244">Central Hub</text>
                  <text x="536" y="339">South Hub</text>
                  <text x="626" y="264">East Hub</text>
                  <text x="771" y="174">Intl Gateway</text>
                </g>
              </svg>
            </div>

            <p class="map-note">
             
            </p>
          </div>
        </div>

        <div class="quote" aria-label="Proof points">
          <div>
            <div class="kicker" style="margin-bottom:10px;">What customers get</div>
            <p>
              “A single accountable partner that can move goods nationally and internationally, keep inventory within spec,
              and maintain document governance that stands up to audits.”
            </p>
          </div>
          <div class="by">
            Typical outcomes:
            <ul style="margin:10px 0 0; padding-left:18px; color: rgba(243,243,243,.78);">
              <li>Fewer handoffs and clearer ownership</li>
              <li>Better on‑time performance via active exception control</li>
              <li>Reduced temperature excursions through monitored SOPs</li>
              <li>Document traceability with defensible audit trails</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="section-head">
        <div>
          <h2>Request a Quote / Start a Conversation</h2>
          <p class="sub">This form is a front‑end template. For production, connect it to your backend or a form service (Cloudflare Forms, email worker, etc.).</p>
        </div>
      </div>

      <div class="contact">
        <div class="contact-grid">
          <div class="contact-left">
            <h3>How we engage</h3>
            <p>
              Share your lanes, storage conditions, and document control requirements. We’ll respond with a proposed solution,
              SLA structure, and onboarding timeline.
            </p>

            <div class="cards" style="grid-template-columns:1fr;gap:10px;margin-top:14px;">
              <div class="card" style="padding:14px;">
                <h3 style="margin:0 0 6px;">Typical inputs</h3>
                <ul style="margin:0;padding-left:18px;">
                  <li>Origin / destination(s), frequency, and lead times</li>
                  <li>Commodity type, value, and handling constraints</li>
                  <li>Temperature/humidity ranges and monitoring needs</li>
                  <li>Document types, retention, and access model</li>
                </ul>
              </div>
              <div class="card" style="padding:14px;">
                <h3 style="margin:0 0 6px;">Assurance options</h3>
                <ul style="margin:0;padding-left:18px;">
                  <li>Role‑based access controls</li>
                  <li>Chain‑of‑custody handoffs</li>
                  <li>Incident reporting & corrective actions</li>
                  <li>Audit reporting packs</li>
                </ul>
              </div>
            </div>
          </div>

          <div class="contact-right">
            <form id="quoteForm" novalidate>
              <div class="grid2">
                <div>
                  <label for="name">Name</label>
                  <input id="name" name="name" autocomplete="name" placeholder="Jane Smith" required />
                </div>
                <div>
                  <label for="company">Company</label>
                  <input id="company" name="company" autocomplete="organization" placeholder="--------" required />
                </div>
              </div>

              <div class="grid2">
                <div>
                  <label for="email">Email</label>
                  <input id="email" name="email" type="email" autocomplete="email" placeholder="jane@company.com" required />
                </div>
                <div>
                  <label for="phone">Phone</label>
                  <input id="phone" name="phone" autocomplete="tel" placeholder="+44 (131) 123‑4567" />
                </div>
              </div>

              <div>
                <label for="service">Primary need</label>
                <select id="service" name="service">
                  <option value="Logistics">Logistics (national / international)</option>
                  <option value="Storage">Climate‑controlled storage</option>
                  <option value="DocumentControl">Secure document control</option>
                  <option value="EndToEnd" selected>End‑to‑end (all of the above)</option>
                </select>
              </div>

              <div>
                <label for="details">Project details</label>
                <textarea id="details" name="details" placeholder="Lanes, storage conditions, volumes, security requirements, timelines…" required></textarea>
              </div>

              <button class="btn primary" type="submit">Submit request</button>
              <div id="formMsg" class="fine" role="status" aria-live="polite"></div>

              <p class="fine">
                By submitting, you agree we may contact you regarding this request. If you need an NDA, mention it in the details.
              </p>
            </form>
          </div>
        </div>
      </div>
    </section>

    <footer>
      <div class="foot">
        <div>
          <div style="font-weight:900;color:rgba(243,243,243,.78);">JTD<span style="color:var(--yellow)"> Group</span> </div>
          <div style="margin-top:4px;">National & international logistics • Climate storage • Secure document control</div>
        </div>
        <div style="display:flex;gap:14px;flex-wrap:wrap;align-items:center;">
          <a href="#logistics">Services</a>
          <a href="#network">Network</a>
          <a href="#documents">Controls</a>
          <a href="#contact">Contact</a>
        </div>
      </div>

      <div style="margin-top:14px;color:rgba(243,243,243,.55);">
        © <span id="year"></span> JTD Group of Companies. All rights reserved. • Privacy • Terms
      </div>
    </footer>
  </main>

  <script>
    // Mobile menu
    const toggle = document.getElementById('mobileToggle');
    const menu = document.getElementById('mobileMenu');
    if (toggle && menu) {
      toggle.addEventListener('click', () => {
        const open = menu.classList.toggle('open');
        toggle.setAttribute('aria-expanded', String(open));
      });
      // Close menu on link click
      menu.querySelectorAll('a').forEach(a => a.addEventListener('click', () => {
        menu.classList.remove('open');
        toggle.setAttribute('aria-expanded', 'false');
      }));
    }

    // Faux submit (front-end only)
    const form = document.getElementById('quoteForm');
    const msg = document.getElementById('formMsg');

    if (form) {
      form.addEventListener('submit', (e) => {
        e.preventDefault();
        const required = form.querySelectorAll('[required]');
        let ok = true;
        required.forEach(el => {
          if (!el.value || String(el.value).trim().length === 0) {
            ok = false;
            el.style.borderColor = 'rgba(255,212,0,.45)';
          } else {
            el.style.borderColor = 'rgba(255,255,255,.10)';
          }
        });

        if (!ok) {
          msg.textContent = 'Please complete the required fields.';
          return;
        }

        // Replace this with a real integration (Cloudflare Workers, Forms, Zapier, etc.)
        msg.textContent = 'Thanks — your request is captured in this demo. Connect the form to your preferred backend to go live.';
        form.reset();
      });
    }

    // Year
    document.getElementById('year').textContent = String(new Date().getFullYear());
  </script>
</body>
</html>
