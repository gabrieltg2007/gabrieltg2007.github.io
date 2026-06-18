<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
  <title>BarberBot AI – Agente de IA para Barbearias</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet" />
  <style>
    /* ─── RESET & BASE ─────────────────────────────────── */
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; font-size: 16px; }

    :root {
      --ink:      #0c0a08;
      --surface:  #141210;
      --card:     #1c1814;
      --border:   #2c2620;
      --gold:     #c8922a;
      --gold-hi:  #e6b84a;
      --gold-dim: rgba(200,146,42,.15);
      --cream:    #f0ebe0;
      --muted:    #7a726a;
      --green:    #4ade80;
      --display:  'Bebas Neue', sans-serif;
      --body:     'Inter', system-ui, sans-serif;
      --w:        1440px;
      --pad-x:    clamp(20px, 5vw, 100px);
    }

    body {
      background: var(--ink);
      color: var(--cream);
      font-family: var(--body);
      line-height: 1.6;
      overflow-x: hidden;
      -webkit-font-smoothing: antialiased;
    }

    /* kill ALL anchor decoration — fixes ghost link icons from markdown parsers */
    a { text-decoration: none; color: inherit; }
    h1, h2, h3, h4 { font-weight: inherit; line-height: 1.1; }

    /* ─── LAYOUT ──────────────────────────────────────── */
    .wrap {
      max-width: var(--w);
      margin: 0 auto;
      padding-left: var(--pad-x);
      padding-right: var(--pad-x);
    }

    /* ─── TYPOGRAPHY SCALE ────────────────────────────── */
    .display {
      font-family: var(--display);
      letter-spacing: .03em;
      line-height: 1.0;
    }
    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 11px;
      font-weight: 600;
      letter-spacing: .14em;
      text-transform: uppercase;
      color: var(--gold);
      background: var(--gold-dim);
      border: 1px solid rgba(200,146,42,.3);
      padding: 5px 14px;
      border-radius: 99px;
    }
    .section-title {
      font-family: var(--display);
      font-size: clamp(36px, 4.5vw, 58px);
      letter-spacing: .02em;
      margin-top: 16px;
      margin-bottom: 16px;
    }
    .section-body {
      font-size: clamp(15px, 1.5vw, 17px);
      color: var(--muted);
      line-height: 1.75;
      max-width: 540px;
    }

    /* ─── BUTTONS ─────────────────────────────────────── */
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      font-family: var(--body);
      font-weight: 700;
      font-size: 15px;
      padding: 14px 28px;
      border-radius: 8px;
      border: none;
      cursor: pointer;
      transition: transform .2s ease, background .2s ease, box-shadow .2s ease;
      white-space: nowrap;
    }
    .btn:hover { transform: translateY(-2px); }
    .btn:active { transform: translateY(0); }
    .btn-gold {
      background: var(--gold);
      color: var(--ink);
      box-shadow: 0 4px 20px rgba(200,146,42,.25);
    }
    .btn-gold:hover {
      background: var(--gold-hi);
      box-shadow: 0 8px 28px rgba(200,146,42,.4);
    }
    .btn-outline {
      background: transparent;
      color: var(--cream);
      border: 1px solid rgba(240,235,224,.2);
    }
    .btn-outline:hover {
      border-color: var(--gold);
      background: var(--gold-dim);
      color: var(--gold-hi);
    }

    /* ─── NAV ─────────────────────────────────────────── */
    .nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 200;
      height: 64px;
      background: rgba(12,10,8,.85);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border-bottom: 1px solid rgba(200,146,42,.15);
      display: flex;
      align-items: center;
    }
    .nav-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
    }
    .nav-logo {
      font-family: var(--display);
      font-size: 28px;
      letter-spacing: .06em;
      color: #fff;
    }
    .nav-logo em { color: var(--gold); font-style: normal; }
    .nav-links {
      display: flex;
      align-items: center;
      gap: 36px;
      list-style: none;
    }
    .nav-links a {
      font-size: 14px;
      font-weight: 500;
      color: rgba(240,235,224,.7);
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--cream); }
    .nav-cta { padding: 9px 20px; font-size: 14px; }

    /* hamburger */
    .nav-burger {
      display: none;
      flex-direction: column;
      gap: 5px;
      cursor: pointer;
      padding: 4px;
      background: none;
      border: none;
    }
    .nav-burger span {
      display: block;
      width: 24px;
      height: 2px;
      background: var(--cream);
      border-radius: 2px;
      transition: transform .3s, opacity .3s;
    }
    .nav-burger.open span:nth-child(1) { transform: translateY(7px) rotate(45deg); }
    .nav-burger.open span:nth-child(2) { opacity: 0; }
    .nav-burger.open span:nth-child(3) { transform: translateY(-7px) rotate(-45deg); }

    .nav-mobile {
      display: none;
      position: fixed;
      top: 64px; left: 0; right: 0;
      background: rgba(12,10,8,.97);
      border-bottom: 1px solid var(--border);
      padding: 24px var(--pad-x) 32px;
      z-index: 199;
      flex-direction: column;
      gap: 20px;
    }
    .nav-mobile.open { display: flex; }
    .nav-mobile a {
      font-size: 18px;
      font-weight: 500;
      color: var(--cream);
      padding: 8px 0;
      border-bottom: 1px solid var(--border);
    }
    .nav-mobile a:last-child { border: none; }

    /* ─── HERO ────────────────────────────────────────── */
    .hero {
      padding-top: 140px;
      padding-bottom: 100px;
      position: relative;
      overflow: hidden;
    }
    /* ambient glow */
    .hero-glow {
      position: absolute;
      pointer-events: none;
      border-radius: 50%;
    }
    .hero-glow-1 {
      width: 700px; height: 700px;
      top: -200px; right: -100px;
      background: radial-gradient(circle, rgba(200,146,42,.1) 0%, transparent 70%);
      animation: floatA 8s ease-in-out infinite;
    }
    .hero-glow-2 {
      width: 400px; height: 400px;
      bottom: -100px; left: 5%;
      background: radial-gradient(circle, rgba(139,44,12,.08) 0%, transparent 70%);
      animation: floatB 11s ease-in-out infinite;
    }
    @keyframes floatA {
      0%, 100% { transform: translate(0, 0) scale(1); }
      50%       { transform: translate(-30px, 30px) scale(1.08); }
    }
    @keyframes floatB {
      0%, 100% { transform: translate(0, 0) scale(1); }
      50%       { transform: translate(20px, -20px) scale(1.05); }
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1fr 500px;
      gap: 80px;
      align-items: center;
      position: relative;
    }

    .hero-eyebrow { margin-bottom: 24px; }
    .hero-h1 {
      font-family: var(--display);
      font-size: clamp(56px, 7vw, 96px);
      letter-spacing: .02em;
      line-height: .97;
      margin-bottom: 28px;
    }
    .hero-h1 .accent { color: var(--gold); display: block; }
    .hero-sub {
      font-size: clamp(16px, 1.6vw, 19px);
      color: rgba(240,235,224,.7);
      max-width: 460px;
      line-height: 1.7;
      margin-bottom: 40px;
    }
    .hero-actions { display: flex; gap: 14px; flex-wrap: wrap; }
    .hero-trust {
      display: flex;
      gap: 24px;
      margin-top: 28px;
      flex-wrap: wrap;
    }
    .trust-item {
      display: flex;
      align-items: center;
      gap: 7px;
      font-size: 13px;
      color: var(--muted);
    }
    .trust-dot {
      width: 6px; height: 6px;
      border-radius: 50%;
      background: var(--gold);
      flex-shrink: 0;
    }

    /* ─── CHAT CARD ────────────────────────────────────── */
    .chat-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 20px;
      overflow: hidden;
      box-shadow: 0 32px 80px rgba(0,0,0,.6), 0 0 0 1px rgba(200,146,42,.08);
      animation: cardFloat 6s ease-in-out infinite;
    }
    @keyframes cardFloat {
      0%, 100% { transform: translateY(0); }
      50%       { transform: translateY(-10px); }
    }
    .chat-head {
      background: var(--border);
      padding: 16px 20px;
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .chat-avatar {
      width: 40px; height: 40px;
      border-radius: 50%;
      background: linear-gradient(135deg, var(--gold) 0%, #8b2c0c 100%);
      display: flex; align-items: center; justify-content: center;
      font-size: 20px;
      flex-shrink: 0;
    }
    .chat-name { font-size: 14px; font-weight: 600; color: #fff; }
    .chat-status { font-size: 11px; color: var(--gold); margin-top: 1px; }
    .chat-online {
      width: 9px; height: 9px;
      border-radius: 50%;
      background: var(--green);
      box-shadow: 0 0 0 2px var(--border), 0 0 8px var(--green);
      margin-left: auto;
      animation: blink 2.5s ease-in-out infinite;
    }
    @keyframes blink {
      0%,100% { box-shadow: 0 0 0 2px var(--border), 0 0 8px var(--green); }
      50%      { box-shadow: 0 0 0 2px var(--border), 0 0 18px var(--green); opacity:.6; }
    }

    .chat-body {
      padding: 20px;
      display: flex;
      flex-direction: column;
      gap: 14px;
    }
    .msg-row { display: flex; flex-direction: column; }
    .msg-row.out { align-items: flex-end; }
    .bubble {
      max-width: 82%;
      padding: 12px 16px;
      font-size: 14px;
      line-height: 1.55;
      border-radius: 18px;
    }
    .bubble-in {
      background: #2a2420;
      color: var(--cream);
      border-bottom-left-radius: 4px;
    }
    .bubble-out {
      background: linear-gradient(135deg, var(--gold), #a87520);
      color: var(--ink);
      font-weight: 500;
      border-bottom-right-radius: 4px;
    }
    .msg-time { font-size: 10px; color: var(--muted); margin-top: 4px; padding: 0 4px; }

    .chat-stat {
      border-top: 1px solid var(--border);
      padding: 14px 20px;
      display: flex;
      align-items: center;
      gap: 12px;
      background: rgba(200,146,42,.04);
    }
    .stat-num {
      font-family: var(--display);
      font-size: 36px;
      color: var(--gold);
      letter-spacing: .02em;
      line-height: 1;
    }
    .stat-label { font-size: 12px; color: var(--muted); line-height: 1.4; }

    /* ─── SECTIONS ────────────────────────────────────── */
    .section { padding: clamp(72px, 8vw, 112px) 0; }
    .section-alt { background: rgba(200,146,42,.03); border-top: 1px solid rgba(200,146,42,.1); border-bottom: 1px solid rgba(200,146,42,.1); }

    /* ─── PROBLEM CARDS ────────────────────────────────── */
    .problem-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 56px;
    }
    .p-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 36px 32px;
      transition: transform .3s ease, border-color .3s ease, box-shadow .3s ease;
    }
    .p-card:hover {
      transform: translateY(-6px);
      border-color: rgba(200,146,42,.35);
      box-shadow: 0 16px 40px rgba(0,0,0,.4);
    }
    .p-icon { font-size: 36px; margin-bottom: 20px; display: block; }
    .p-title {
      font-family: var(--display);
      font-size: 24px;
      letter-spacing: .03em;
      color: #fff;
      margin-bottom: 12px;
    }
    .p-body { font-size: 14px; color: var(--muted); line-height: 1.7; }
    .p-tag {
      display: inline-block;
      margin-top: 18px;
      font-size: 10px;
      font-weight: 700;
      letter-spacing: .12em;
      text-transform: uppercase;
      color: #e05555;
      background: rgba(224,85,85,.1);
      border: 1px solid rgba(224,85,85,.2);
      padding: 3px 10px;
      border-radius: 99px;
    }

    /* ─── STEPS ───────────────────────────────────────── */
    .steps-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 0;
      margin-top: 64px;
      position: relative;
    }
    .steps-grid::after {
      content: '';
      position: absolute;
      top: 28px;
      left: calc(100% / 6);
      right: calc(100% / 6);
      height: 1px;
      background: linear-gradient(to right, transparent, rgba(200,146,42,.3), rgba(200,146,42,.3), transparent);
      pointer-events: none;
    }
    .step {
      padding: 0 32px;
      position: relative;
    }
    .step:first-child { padding-left: 0; }
    .step:last-child { padding-right: 0; }
    .step-num {
      font-family: var(--display);
      font-size: 14px;
      letter-spacing: .1em;
      color: var(--gold);
      background: var(--gold-dim);
      border: 1px solid rgba(200,146,42,.3);
      width: 56px; height: 56px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 28px;
    }
    .step-title {
      font-family: var(--display);
      font-size: 24px;
      letter-spacing: .03em;
      color: #fff;
      margin-bottom: 12px;
    }
    .step-body { font-size: 14px; color: var(--muted); line-height: 1.7; }

    /* ─── AGENDA SPLIT ────────────────────────────────── */
    .split-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 80px;
      align-items: center;
    }
    .split-grid.reverse { direction: rtl; }
    .split-grid.reverse > * { direction: ltr; }

    .agenda-ui {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 20px 60px rgba(0,0,0,.5);
    }
    .agenda-ui-head {
      background: var(--border);
      padding: 14px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .agenda-ui-head span:first-child { font-size: 14px; font-weight: 600; }
    .agenda-ui-head span:last-child { font-size: 12px; color: var(--muted); }

    .slot {
      display: flex;
      align-items: stretch;
      border-bottom: 1px solid rgba(44,38,32,.8);
    }
    .slot:last-of-type { border-bottom: none; }
    .slot-time {
      padding: 14px 16px;
      font-size: 11px;
      font-family: monospace;
      color: var(--muted);
      min-width: 52px;
      border-right: 1px solid var(--border);
      display: flex;
      align-items: center;
    }
    .slot-info { padding: 12px 16px; flex: 1; }
    .slot-name { font-size: 13px; font-weight: 600; color: var(--cream); }
    .slot-svc { font-size: 11px; color: var(--muted); margin-top: 2px; }
    .slot-pill {
      display: inline-block;
      margin-top: 5px;
      font-size: 9px;
      font-weight: 700;
      letter-spacing: .08em;
      text-transform: uppercase;
      padding: 2px 8px;
      border-radius: 99px;
    }
    .pill-ai  { background: rgba(200,146,42,.12); color: var(--gold); }
    .pill-ok  { background: rgba(74,222,128,.1); color: var(--green); }
    .pill-man { background: rgba(129,140,248,.1); color: #a5b4fc; }

    .agenda-note {
      padding: 14px 20px;
      background: rgba(200,146,42,.04);
      border-top: 1px solid var(--border);
      font-size: 12px;
      color: var(--muted);
      line-height: 1.6;
    }
    .agenda-note strong { color: var(--cream); font-weight: 500; }

    .feat-list { display: flex; flex-direction: column; gap: 28px; }
    .feat {
      display: flex;
      gap: 18px;
      transition: transform .25s ease;
    }
    .feat:hover { transform: translateX(4px); }
    .feat-icon {
      width: 44px; height: 44px;
      border-radius: 10px;
      background: var(--gold-dim);
      border: 1px solid rgba(200,146,42,.2);
      display: flex; align-items: center; justify-content: center;
      font-size: 20px;
      flex-shrink: 0;
      transition: background .2s, transform .2s;
    }
    .feat:hover .feat-icon {
      background: rgba(200,146,42,.22);
      transform: scale(1.1);
    }
    .feat-title { font-size: 16px; font-weight: 600; color: #fff; margin-bottom: 4px; }
    .feat-body { font-size: 14px; color: var(--muted); line-height: 1.65; }

    /* ─── REMINDER ────────────────────────────────────── */
    .reminder-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 28px;
      box-shadow: 0 20px 60px rgba(0,0,0,.5);
    }
    .r-bubble-in {
      background: #2a2420;
      color: var(--cream);
      padding: 14px 18px;
      border-radius: 4px 16px 16px 16px;
      font-size: 14px;
      line-height: 1.6;
      margin-bottom: 12px;
    }
    .r-bubble-out {
      background: linear-gradient(135deg, var(--gold), #a87520);
      color: var(--ink);
      padding: 12px 18px;
      border-radius: 16px 4px 16px 16px;
      font-size: 14px;
      font-weight: 600;
      text-align: right;
    }
    .reminder-stat {
      margin-top: 20px;
      padding: 18px;
      background: var(--gold-dim);
      border: 1px solid rgba(200,146,42,.2);
      border-radius: 12px;
      text-align: center;
    }
    .reminder-stat-num {
      font-family: var(--display);
      font-size: 48px;
      color: var(--gold);
      line-height: 1;
    }
    .reminder-stat-label { font-size: 12px; color: var(--muted); margin-top: 4px; }

    .check-list { display: flex; flex-direction: column; gap: 16px; }
    .check-item {
      display: flex;
      align-items: flex-start;
      gap: 12px;
      font-size: 16px;
      color: var(--cream);
    }
    .check-icon {
      width: 22px; height: 22px;
      border-radius: 50%;
      background: var(--gold-dim);
      border: 1px solid rgba(200,146,42,.3);
      display: flex; align-items: center; justify-content: center;
      font-size: 11px;
      color: var(--gold);
      flex-shrink: 0;
      margin-top: 2px;
    }

    /* ─── PRICING ─────────────────────────────────────── */
    .price-card {
      max-width: 500px;
      margin: 56px auto 0;
      background: var(--card);
      border: 1px solid rgba(200,146,42,.3);
      border-top: 3px solid var(--gold);
      border-radius: 20px;
      padding: 52px 48px;
      position: relative;
      box-shadow: 0 24px 80px rgba(0,0,0,.5);
    }
    .price-badge {
      position: absolute;
      top: -14px; left: 50%;
      transform: translateX(-50%);
      background: var(--gold);
      color: var(--ink);
      font-size: 11px;
      font-weight: 700;
      letter-spacing: .1em;
      text-transform: uppercase;
      padding: 5px 18px;
      border-radius: 99px;
      white-space: nowrap;
    }
    .price-desc { font-size: 16px; color: var(--muted); margin-bottom: 32px; }
    .price-list { list-style: none; display: flex; flex-direction: column; gap: 14px; margin-bottom: 40px; }
    .price-list li {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 15px;
      color: var(--cream);
    }
    .price-check {
      width: 20px; height: 20px;
      border-radius: 50%;
      background: var(--gold-dim);
      border: 1px solid rgba(200,146,42,.3);
      display: flex; align-items: center; justify-content: center;
      font-size: 10px;
      color: var(--gold);
      flex-shrink: 0;
    }
    .price-note { font-size: 12px; color: var(--muted); text-align: center; margin-top: 16px; }

    /* ─── TESTIMONIALS ────────────────────────────────── */
    .depo-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 56px;
    }
    .depo-card {
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 32px 28px;
      position: relative;
      transition: transform .3s ease, border-color .3s ease;
    }
    .depo-card:hover {
      transform: translateY(-5px);
      border-color: rgba(200,146,42,.3);
    }
    .depo-quote {
      font-family: Georgia, serif;
      font-size: 72px;
      color: var(--gold-dim);
      line-height: .8;
      margin-bottom: 8px;
      user-select: none;
    }
    .depo-text { font-size: 15px; color: var(--cream); line-height: 1.75; margin-bottom: 24px; }
    .depo-name { font-size: 14px; font-weight: 700; color: #fff; }
    .depo-role { font-size: 12px; color: var(--muted); margin-top: 2px; }

    /* ─── FAQ ─────────────────────────────────────────── */
    .faq-wrap { max-width: 700px; margin: 52px auto 0; }
    .faq-item { border-bottom: 1px solid var(--border); }
    .faq-item:first-child { border-top: 1px solid var(--border); }
    .faq-btn {
      width: 100%;
      background: none;
      border: none;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 22px 4px;
      font-size: 16px;
      font-weight: 600;
      color: var(--cream);
      font-family: var(--body);
      text-align: left;
      gap: 16px;
      transition: color .2s;
    }
    .faq-btn:hover { color: var(--gold); }
    .faq-arrow {
      font-size: 20px;
      color: var(--gold);
      transition: transform .35s cubic-bezier(.22,.61,.36,1);
      flex-shrink: 0;
      line-height: 1;
    }
    .faq-item.open .faq-arrow { transform: rotate(180deg); }
    .faq-ans {
      overflow: hidden;
      max-height: 0;
      opacity: 0;
      transition: max-height .4s cubic-bezier(.22,.61,.36,1), opacity .35s ease, padding .3s ease;
      font-size: 15px;
      color: var(--muted);
      line-height: 1.75;
      padding: 0 4px;
    }
    .faq-item.open .faq-ans {
      max-height: 240px;
      opacity: 1;
      padding-bottom: 22px;
    }

    /* ─── CTA FINAL ────────────────────────────────────── */
    .cta-section {
      padding: clamp(80px, 10vw, 120px) 0;
      text-align: center;
      background: linear-gradient(180deg, transparent, rgba(200,146,42,.04));
    }
    .cta-badges {
      display: flex;
      gap: 24px;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 28px;
    }
    .cta-badge {
      display: flex;
      align-items: center;
      gap: 7px;
      font-size: 13px;
      color: var(--muted);
    }
    .cta-dot { width: 5px; height: 5px; border-radius: 50%; background: var(--gold); }

    /* ─── FOOTER ──────────────────────────────────────── */
    footer {
      border-top: 1px solid var(--border);
      padding: 40px 0;
    }
    .footer-inner {
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 16px;
    }
    .footer-logo {
      font-family: var(--display);
      font-size: 24px;
      letter-spacing: .05em;
      color: #fff;
    }
    .footer-logo em { color: var(--gold); font-style: normal; }
    .footer-links { display: flex; gap: 28px; }
    .footer-links a { font-size: 13px; color: var(--muted); transition: color .2s; }
    .footer-links a:hover { color: var(--gold); }
    .footer-copy { font-size: 12px; color: var(--muted); }

    /* ─── SCROLL REVEAL ───────────────────────────────── */
    /* Only activates after JS marks html with .js-on */
    .js-on [data-reveal] {
      opacity: 0;
      transform: translateY(30px);
      transition: opacity .65s cubic-bezier(.22,.61,.36,1), transform .65s cubic-bezier(.22,.61,.36,1);
    }
    .js-on [data-reveal="left"] { transform: translateX(-36px); }
    .js-on [data-reveal="right"] { transform: translateX(36px); }
    .js-on [data-reveal].visible {
      opacity: 1;
      transform: translate(0);
    }
    /* stagger for siblings */
    .js-on [data-reveal][data-delay="1"] { transition-delay: .1s; }
    .js-on [data-reveal][data-delay="2"] { transition-delay: .2s; }
    .js-on [data-reveal][data-delay="3"] { transition-delay: .3s; }

    /* ─── RESPONSIVE ──────────────────────────────────── */
    @media (max-width: 1100px) {
      .hero-grid { grid-template-columns: 1fr; gap: 56px; }
      .hero-grid > *:last-child { max-width: 540px; margin: 0 auto; width: 100%; }
      .split-grid { grid-template-columns: 1fr; gap: 48px; }
      .split-grid.reverse { direction: ltr; }
      .problem-grid { grid-template-columns: 1fr 1fr; }
      .steps-grid { grid-template-columns: 1fr; gap: 40px; }
      .steps-grid::after { display: none; }
      .step { padding: 0 !important; }
      .depo-grid { grid-template-columns: 1fr 1fr; }
    }

    @media (max-width: 700px) {
      :root { --pad-x: 20px; }
      .nav-links { display: none; }
      .nav-cta-desktop { display: none; }
      .nav-burger { display: flex; }
      .problem-grid { grid-template-columns: 1fr; }
      .depo-grid { grid-template-columns: 1fr; }
      .price-card { padding: 40px 24px; }
      .hero-actions { flex-direction: column; }
      .hero-actions .btn { width: 100%; justify-content: center; }
      .footer-inner { flex-direction: column; text-align: center; }
      .footer-links { justify-content: center; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { animation-duration: .01ms !important; transition-duration: .01ms !important; }
    }
  </style>
</head>
<body>

<!-- NAV -->
<nav class="nav">
  <div class="wrap nav-inner">
    <a href="#" class="nav-logo">Barber<em>Bot</em> AI</a>
    <ul class="nav-links">
      <li><a href="#problema">O Problema</a></li>
      <li><a href="#como-funciona">Como Funciona</a></li>
      <li><a href="#agenda">Agenda</a></li>
    </ul>
    <a href="#contato" class="btn btn-gold nav-cta nav-cta-desktop">Falar com Especialista</a>
    <button class="nav-burger" id="burger" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>
<div class="nav-mobile" id="nav-mobile">
  <a href="#problema" class="nav-mob-link">O Problema</a>
  <a href="#como-funciona" class="nav-mob-link">Como Funciona</a>
  <a href="#agenda" class="nav-mob-link">Agenda</a>
  <a href="#contato" class="btn btn-gold" style="margin-top:8px">Falar com Especialista</a>
</div>

<!-- HERO -->
<section class="hero">
  <div class="hero-glow hero-glow-1"></div>
  <div class="hero-glow hero-glow-2"></div>
  <div class="wrap">
    <div class="hero-grid">
      <div>
        <div class="hero-eyebrow" data-reveal>
          <span class="eyebrow">💈 IA disponível 24 horas por dia</span>
        </div>
        <h1 class="hero-h1" data-reveal data-delay="1">
          Sua barbearia<br>lotada,
          <span class="accent">sem esforço</span>
        </h1>
        <p class="hero-sub" data-reveal data-delay="2">
          O agente de IA que agenda cortes, tira dúvidas e confirma horários no WhatsApp — enquanto você foca na navalha.
        </p>
        <div class="hero-actions" data-reveal data-delay="3">
          <a href="#contato" class="btn btn-gold">💬 Falar com Especialista</a>
          <a href="#como-funciona" class="btn btn-outline">Ver como funciona →</a>
        </div>
        <div class="hero-trust" data-reveal data-delay="3">
          <span class="trust-item"><span class="trust-dot"></span>Fácil de configurar</span>
          <span class="trust-item"><span class="trust-dot"></span>Suporte em português</span>
          <span class="trust-item"><span class="trust-dot"></span>Cancele a qualquer hora</span>
        </div>
      </div>

      <div class="chat-card">
        <div class="chat-head">
          <div class="chat-avatar">💈</div>
          <div>
            <div class="chat-name">BarberBot AI — Barbearia do Pedro</div>
            <div class="chat-status">● Online agora</div>
          </div>
          <div class="chat-online"></div>
        </div>
        <div class="chat-body">
          <div class="msg-row">
            <div class="bubble bubble-in">Oi! Tem horário hoje pra corte e barba?</div>
            <span class="msg-time">10:23</span>
          </div>
          <div class="msg-row out">
            <div class="bubble bubble-out">Oi! Tem sim 💈 Hoje temos:<br><strong>14h</strong> com Rodrigo<br><strong>16h</strong> com Diego<br><br>Qual prefere?</div>
            <span class="msg-time">10:23</span>
          </div>
          <div class="msg-row">
            <div class="bubble bubble-in">Às 14h com o Rodrigo! Quanto fica?</div>
          </div>
          <div class="msg-row out">
            <div class="bubble bubble-out">Corte + barba: <strong>R$ 65</strong>.<br>Agendado! ✅ Te espero às 14h, rua XV, nº 210.</div>
            <span class="msg-time">10:24</span>
          </div>
        </div>
        <div class="chat-stat">
          <div class="stat-num" id="metric-counter">+43</div>
          <div class="stat-label">agendamentos<br>esta semana via IA</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- PROBLEMA -->
<section class="section" id="problema">
  <div class="wrap">
    <span class="eyebrow" data-reveal>O problema</span>
    <h2 class="section-title" data-reveal data-delay="1">Você perde dinheiro<br>toda vez que…</h2>
    <p class="section-body" data-reveal data-delay="2">Cada mensagem não respondida é um corte que vai parar na barbearia ao lado.</p>
    <div class="problem-grid">
      <div class="p-card" data-reveal data-delay="1">
        <span class="p-icon">📵</span>
        <div class="p-title">Não Atende na Hora</div>
        <p class="p-body">O cliente manda mensagem perguntando sobre horário. Você está com a tesoura na mão. Ele não espera e marca em outra barbearia.</p>
        <span class="p-tag">↑ Receita perdida</span>
      </div>
      <div class="p-card" data-reveal data-delay="2">
        <span class="p-icon">🪑</span>
        <div class="p-title">Cadeira Vazia</div>
        <p class="p-body">Você reservou o horário, preparou tudo — e o cliente não apareceu. Tempo perdido que virou prejuízo direto no caixa.</p>
        <span class="p-tag">↑ No-show</span>
      </div>
      <div class="p-card" data-reveal data-delay="3">
        <span class="p-icon">🌙</span>
        <div class="p-title">Depois do Expediente</div>
        <p class="p-body">Homens marcam à noite e no fim de semana. Se você não está online nesse momento, perde o cliente para quem está.</p>
        <span class="p-tag">↑ Clientes perdidos</span>
      </div>
    </div>
  </div>
</section>

<!-- COMO FUNCIONA -->
<section class="section section-alt" id="como-funciona">
  <div class="wrap">
    <span class="eyebrow" data-reveal>Solução</span>
    <h2 class="section-title" data-reveal data-delay="1">Configurado em 3 passos,<br>funcionando em minutos</h2>
    <p class="section-body" data-reveal data-delay="2">Não precisa saber de tecnologia. Se você usa WhatsApp, você usa o BarberBot AI.</p>
    <div class="steps-grid">
      <div class="step" data-reveal data-delay="1">
        <div class="step-num">01</div>
        <div class="step-title">Configure a Agenda</div>
        <p class="step-body">Defina seus barbeiros, horários e serviços (corte, barba, degradê…) em um painel simples.</p>
      </div>
      <div class="step" data-reveal data-delay="2">
        <div class="step-num">02</div>
        <div class="step-title">Treine a IA</div>
        <p class="step-body">Informe os preços, o endereço e as regras da sua barbearia. A IA aprende e responde como você responderia.</p>
      </div>
      <div class="step" data-reveal data-delay="3">
        <div class="step-num">03</div>
        <div class="step-title">Ative no WhatsApp</div>
        <p class="step-body">Leia o QR Code com o celular e pronto. O BarberBot AI assume as conversas e começa a lotar a agenda.</p>
      </div>
    </div>
  </div>
</section>

<!-- AGENDA -->
<section class="section" id="agenda">
  <div class="wrap">
    <div class="split-grid">
      <div class="agenda-ui" data-reveal="left">
        <div class="agenda-ui-head">
          <span>Agenda — Barbearia do Pedro</span>
          <span>Hoje, quarta-feira</span>
        </div>
        <div class="slot">
          <div class="slot-time">09:00</div>
          <div class="slot-info">
            <div class="slot-name">Carlos Mendes</div>
            <div class="slot-svc">Corte + Barba · Rodrigo</div>
            <span class="slot-pill pill-ai">Agendado via IA</span>
          </div>
        </div>
        <div class="slot">
          <div class="slot-time">10:30</div>
          <div class="slot-info">
            <div class="slot-name">Lucas Ferreira</div>
            <div class="slot-svc">Degradê · Diego</div>
            <span class="slot-pill pill-man">Presencial</span>
          </div>
        </div>
        <div class="slot">
          <div class="slot-time">11:00</div>
          <div class="slot-info">
            <div class="slot-name">Horário Livre</div>
            <div class="slot-svc">Rodrigo</div>
            <span class="slot-pill pill-ok">Disponível</span>
          </div>
        </div>
        <div class="slot">
          <div class="slot-time">14:00</div>
          <div class="slot-info">
            <div class="slot-name">André Lima</div>
            <div class="slot-svc">Barba completa · Rodrigo</div>
            <span class="slot-pill pill-ai">Agendado via IA</span>
          </div>
        </div>
        <div class="agenda-note">
          💬 Enviado automaticamente 2h antes:<br>
          <strong>"Oi André! Seu corte é hoje às 14h com o Rodrigo. Confirma? ✂️"</strong>
        </div>
      </div>

      <div data-reveal="right">
        <span class="eyebrow">Gestão completa</span>
        <h2 class="section-title">Uma agenda poderosa,<br>sem complicação</h2>
        <p class="section-body" style="margin-bottom:36px">Esqueça cadernos e WhatsApp desorganizado. Você e a equipe têm visão total de todos os horários.</p>
        <div class="feat-list">
          <div class="feat">
            <div class="feat-icon">✂️</div>
            <div>
              <div class="feat-title">Todos os Barbeiros</div>
              <p class="feat-body">Gerencie a agenda de cada profissional em um único painel, com horários individuais.</p>
            </div>
          </div>
          <div class="feat">
            <div class="feat-icon">🎙️</div>
            <div>
              <div class="feat-title">Entende Áudios do WhatsApp</div>
              <p class="feat-body">A IA transcreve e responde mensagens de voz. Seu cliente pode falar no áudio normalmente.</p>
            </div>
          </div>
          <div class="feat">
            <div class="feat-icon">🎯</div>
            <div>
              <div class="feat-title">Barbeiro Favorito</div>
              <p class="feat-body">Se o cliente pedir um profissional específico, a IA mostra só os horários disponíveis dele.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- LEMBRETES -->
<section class="section section-alt">
  <div class="wrap">
    <div class="split-grid reverse">
      <div data-reveal="left">
        <span class="eyebrow">Sem faltas</span>
        <h2 class="section-title">Lembretes que<br>garantem a presença</h2>
        <p class="section-body" style="margin-bottom:36px">Cliente que esquece é cadeira vazia. O BarberBot AI nunca esquece — manda lembrete automático e pede confirmação.</p>
        <div class="check-list">
          <div class="check-item">
            <div class="check-icon">✓</div>
            Reduza faltas em até 40%
          </div>
          <div class="check-item">
            <div class="check-icon">✓</div>
            Se o cliente cancelar, o horário é liberado na hora
          </div>
          <div class="check-item">
            <div class="check-icon">✓</div>
            Você foca no corte, a IA cuida do resto
          </div>
        </div>
      </div>

      <div class="reminder-card" data-reveal="right">
        <div class="r-bubble-in">
          💈 Oi, André! Seu corte é <strong>hoje às 14h</strong> com o Rodrigo, na Barbearia do Pedro.<br><br>
          Confirma presença? ✂️
        </div>
        <div class="r-bubble-out">Confirmado! Já tô saindo 👊</div>
        <div class="reminder-stat">
          <div class="reminder-stat-num" id="stat-counter">-40%</div>
          <div class="reminder-stat-label">redução de no-show com lembretes automáticos</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- INVESTIMENTO -->
<section class="section" id="preco">
  <div class="wrap" style="text-align:center">
    <span class="eyebrow" data-reveal>Investimento</span>
    <h2 class="section-title" data-reveal data-delay="1">Quanto custa um cliente perdido?</h2>
    <p class="section-body" style="margin:0 auto 0;max-width:480px" data-reveal data-delay="2">Se a IA recuperar <strong style="color:var(--gold)">1 cliente por mês</strong>, ela já se paga. Imagine recuperar dezenas.</p>
    <div class="price-card" data-reveal data-delay="1">
      <div class="price-badge">Mais popular</div>
      <p class="price-desc">Acesso completo. Sem surpresas.</p>
      <ul class="price-list">
        <li><span class="price-check">✓</span> Agendamentos ilimitados via WhatsApp</li>
        <li><span class="price-check">✓</span> Agenda visual para toda a equipe</li>
        <li><span class="price-check">✓</span> Lembretes automáticos e confirmação</li>
        <li><span class="price-check">✓</span> IA que entende áudios de WhatsApp</li>
        <li><span class="price-check">✓</span> Suporte por barbeiro específico</li>
        <li><span class="price-check">✓</span> Painel de gestão completo</li>
        <li><span class="price-check">✓</span> Suporte via WhatsApp</li>
      </ul>
      <a href="#contato" class="btn btn-gold" style="width:100%;justify-content:center;font-size:16px;padding:16px">Quero o BarberBot AI</a>
      <p class="price-note">Cancele a qualquer momento</p>
    </div>
  </div>
</section>

<!-- DEPOIMENTOS -->
<section class="section section-alt">
  <div class="wrap" style="text-align:center">
    <span class="eyebrow" data-reveal>Depoimentos</span>
    <h2 class="section-title" data-reveal data-delay="1">O que dizem os barbeiros</h2>
    <div class="depo-grid">
      <div class="depo-card" data-reveal data-delay="1">
        <div class="depo-quote">"</div>
        <p class="depo-text">No primeiro dia já vieram 12 agendamentos pelo WhatsApp sem eu precisar responder nada. Parece mágica.</p>
        <div class="depo-name">Rodrigo S.</div>
        <div class="depo-role">Dono, Barbearia Clássica — SP</div>
      </div>
      <div class="depo-card" data-reveal data-delay="2">
        <div class="depo-quote">"</div>
        <p class="depo-text">Meus clientes não percebem que é uma IA. O atendimento ficou mais rápido do que quando era eu respondendo.</p>
        <div class="depo-name">Diego M.</div>
        <div class="depo-role">Barbeiro, Studio 74 — RJ</div>
      </div>
      <div class="depo-card" data-reveal data-delay="3">
        <div class="depo-quote">"</div>
        <p class="depo-text">Acabou com as faltas. Os lembretes automáticos fizeram a diferença — minha agenda tá sempre lotada.</p>
        <div class="depo-name">André L.</div>
        <div class="depo-role">Proprietário, Old School Barber — BH</div>
      </div>
    </div>
  </div>
</section>

<!-- FAQ -->
<section class="section">
  <div class="wrap" style="text-align:center">
    <span class="eyebrow" data-reveal>Dúvidas frequentes</span>
    <h2 class="section-title" data-reveal data-delay="1">Perguntas & Respostas</h2>
    <div class="faq-wrap">
      <div class="faq-item">
        <button class="faq-btn" onclick="faq(this)">
          A IA sabe os preços e serviços da minha barbearia?
          <span class="faq-arrow">⌄</span>
        </button>
        <div class="faq-ans">Sim! Você cadastra sua tabela completa (corte, barba, degradê, progressiva, etc.) com preços e duração. A IA consulta esses dados antes de responder qualquer cliente.</div>
      </div>
      <div class="faq-item">
        <button class="faq-btn" onclick="faq(this)">
          Posso usar meu número atual do WhatsApp?
          <span class="faq-arrow">⌄</span>
        </button>
        <div class="faq-ans">Com certeza. A conexão é feita via QR Code, igual ao WhatsApp Web. Você continua com o mesmo número e pode intervir nas conversas sempre que quiser.</div>
      </div>
      <div class="faq-item">
        <button class="faq-btn" onclick="faq(this)">
          E se o cliente quiser um barbeiro específico?
          <span class="faq-arrow">⌄</span>
        </button>
        <div class="faq-ans">A IA entende isso. Se o cliente pedir o Rodrigo, ela verifica a agenda do Rodrigo e mostra somente os horários disponíveis dele. Preferência sempre respeitada.</div>
      </div>
      <div class="faq-item">
        <button class="faq-btn" onclick="faq(this)">
          Quanto tempo leva para configurar?
          <span class="faq-arrow">⌄</span>
        </button>
        <div class="faq-ans">Em média 20 a 30 minutos. Nossa equipe ajuda por WhatsApp em todo o processo. A maioria dos barbeiros ativa no mesmo dia em que se cadastra.</div>
      </div>
      <div class="faq-item">
        <button class="faq-btn" onclick="faq(this)">
          O cliente sabe que está falando com uma IA?
          <span class="faq-arrow">⌄</span>
        </button>
        <div class="faq-ans">A IA responde de forma natural e fluída. Muitos clientes não percebem. Se o cliente perguntar diretamente, você pode configurar o comportamento que preferir.</div>
      </div>
    </div>
  </div>
</section>

<!-- CTA FINAL -->
<section class="cta-section" id="contato">
  <div class="wrap">
    <span class="eyebrow" data-reveal>Comece agora</span>
    <h2 class="section-title" style="max-width:640px;margin:16px auto 20px" data-reveal data-delay="1">
      Sua barbearia trabalhando<br><span style="color:var(--gold)">enquanto você dorme</span>
    </h2>
    <p class="section-body" style="margin:0 auto 40px;text-align:center" data-reveal data-delay="2">
      Fale com um especialista e veja como o BarberBot AI se encaixa na sua barbearia.
    </p>
    <a href="https://wa.me/5500000000000?text=Olá! Quero saber mais sobre o BarberBot AI" class="btn btn-gold" style="font-size:17px;padding:18px 40px" data-reveal data-delay="3">
      💬 Falar com Especialista
    </a>
    <div class="cta-badges" data-reveal data-delay="3">
      <span class="cta-badge"><span class="cta-dot"></span>Acesso completo</span>
      <span class="cta-badge"><span class="cta-dot"></span>Suporte em português</span>
      <span class="cta-badge"><span class="cta-dot"></span>Cancele a qualquer hora</span>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="wrap footer-inner">
    <div class="footer-logo">Barber<em>Bot</em> AI</div>
    <div class="footer-links">
      <a href="#">Termos de uso</a>
      <a href="#">Privacidade</a>
      <a href="#contato">Contato</a>
    </div>
    <p class="footer-copy">© 2025 BarberBot AI. Todos os direitos reservados.</p>
  </div>
</footer>

<script>
  /* ── Mark JS available — prevents invisible content if JS fails ── */
  document.documentElement.classList.add('js-on');

  /* ── Mobile nav ─────────────────────────────────────────────── */
  const burger = document.getElementById('burger');
  const mobileNav = document.getElementById('nav-mobile');
  burger.addEventListener('click', () => {
    burger.classList.toggle('open');
    mobileNav.classList.toggle('open');
  });
  document.querySelectorAll('.nav-mob-link, .nav-mobile .btn').forEach(el => {
    el.addEventListener('click', () => {
      burger.classList.remove('open');
      mobileNav.classList.remove('open');
    });
  });

  /* ── Scroll reveal ───────────────────────────────────────────── */
  const io = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        io.unobserve(e.target);
      }
    });
  }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });

  document.querySelectorAll('[data-reveal]').forEach(el => io.observe(el));

  /* ── FAQ ─────────────────────────────────────────────────────── */
  function faq(btn) {
    const item = btn.parentElement;
    const isOpen = item.classList.contains('open');
    document.querySelectorAll('.faq-item.open').forEach(i => i.classList.remove('open'));
    if (!isOpen) item.classList.add('open');
  }

  /* ── Counter animation ───────────────────────────────────────── */
  function animCount(el, target, prefix, suffix, duration) {
    const countIO = new IntersectionObserver((entries) => {
      if (!entries[0].isIntersecting) return;
      let start = null;
      const tick = (ts) => {
        if (!start) start = ts;
        const p = Math.min((ts - start) / duration, 1);
        const ease = 1 - Math.pow(1 - p, 3);
        el.textContent = prefix + Math.round(ease * target) + suffix;
        if (p < 1) requestAnimationFrame(tick);
      };
      requestAnimationFrame(tick);
      countIO.unobserve(entries[0].target);
    }, { threshold: 0.5 });
    countIO.observe(el);
  }

  const metric = document.getElementById('metric-counter');
  const stat   = document.getElementById('stat-counter');
  if (metric) animCount(metric, 43, '+', '', 1200);
  if (stat)   animCount(stat,   40, '-', '%', 1000);
</script>
</body>
</html>
