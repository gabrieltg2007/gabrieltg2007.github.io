# gabrieltg2007.github.io
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>BarberBot AI – O Agente de IA para Barbearias</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Inter:wght@400;500;600;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet" />
  <style>
    /* ── TOKENS ─────────────────────────────────────────── */
    :root {
      --ink:     #0f0d0b;
      --cream:   #f5f0e8;
      --bone:    #ece6d9;
      --gold:    #c8922a;
      --gold-lt: #e6b84a;
      --rust:    #8b2c0c;
      --white:   #ffffff;
      --muted:   #6b6460;
      --card-bg: #1a1612;
      --card-br: #2a2420;

      --ff-display: 'Bebas Neue', sans-serif;
      --ff-body:    'Inter', sans-serif;
      --ff-mono:    'DM Mono', monospace;

      --radius: 6px;
      --max: 1100px;
    }

    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      background: var(--ink);
      color: var(--cream);
      font-family: var(--ff-body);
      line-height: 1.6;
      font-size: 16px;
      overflow-x: hidden;
    }

    /* ── UTILITIES ──────────────────────────────────────── */
    .container { max-width: var(--max); margin: 0 auto; padding: 0 24px; }
    .gold { color: var(--gold); }
    .tag {
      display: inline-block;
      font-family: var(--ff-mono);
      font-size: 11px;
      letter-spacing: .12em;
      text-transform: uppercase;
      color: var(--gold);
      background: rgba(200,146,42,.12);
      border: 1px solid rgba(200,146,42,.3);
      padding: 4px 12px;
      border-radius: 20px;
    }

    /* ── NAV ────────────────────────────────────────────── */
    nav {
      position: sticky; top: 0; z-index: 100;
      background: rgba(15,13,11,.9);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(200,146,42,.2);
    }
    .nav-inner {
      display: flex; align-items: center; justify-content: space-between;
      height: 60px; max-width: var(--max); margin: 0 auto; padding: 0 24px;
    }
    .logo {
      font-family: var(--ff-display);
      font-size: 26px;
      letter-spacing: .05em;
      color: var(--white);
      text-decoration: none;
    }
    .logo span { color: var(--gold); }
    .nav-links { display: flex; gap: 28px; align-items: center; list-style: none; }
    .nav-links a {
      font-size: 13px; font-weight: 500; color: var(--cream);
      text-decoration: none; opacity: .8;
      transition: opacity .2s, color .2s;
    }
    .nav-links a:hover { opacity: 1; color: var(--gold); }
    .btn-nav {
      background: var(--gold);
      color: var(--ink) !important;
      font-weight: 700 !important;
      opacity: 1 !important;
      padding: 8px 18px;
      border-radius: var(--radius);
      transition: background .2s !important;
    }
    .btn-nav:hover { background: var(--gold-lt) !important; }

    /* ── HERO ───────────────────────────────────────────── */
    .hero {
      padding: 80px 0 64px;
      position: relative;
      overflow: hidden;
    }
    .hero::before {
      content: '';
      position: absolute; inset: 0;
      background: radial-gradient(ellipse 60% 70% at 70% 40%, rgba(200,146,42,.08) 0%, transparent 70%);
      pointer-events: none;
    }
    /* decorative barber pole lines */
    .hero::after {
      content: '';
      position: absolute; right: -80px; top: -80px;
      width: 320px; height: 320px;
      border-radius: 50%;
      border: 60px solid transparent;
      border-top-color: rgba(200,146,42,.06);
      border-right-color: rgba(139,44,12,.06);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1fr 420px;
      gap: 60px;
      align-items: center;
    }

    .hero-eyebrow { margin-bottom: 20px; }
    .hero-eyebrow .tag { font-size: 12px; }

    h1 {
      font-family: var(--ff-display);
      font-size: clamp(52px, 7vw, 80px);
      line-height: 1.0;
      letter-spacing: .02em;
      margin-bottom: 24px;
    }
    h1 .line-accent {
      display: block;
      color: var(--gold);
      -webkit-text-stroke: 1px var(--gold);
    }

    .hero-sub {
      font-size: 17px;
      color: rgba(245,240,232,.75);
      max-width: 480px;
      margin-bottom: 36px;
      line-height: 1.7;
    }

    .hero-ctas { display: flex; gap: 12px; flex-wrap: wrap; }

    .btn-primary {
      display: inline-block;
      background: var(--gold);
      color: var(--ink);
      font-weight: 700;
      font-size: 15px;
      padding: 14px 28px;
      border-radius: var(--radius);
      text-decoration: none;
      transition: background .2s, transform .15s;
      border: none; cursor: pointer;
    }
    .btn-primary:hover { background: var(--gold-lt); transform: translateY(-1px); }

    .btn-ghost {
      display: inline-block;
      background: transparent;
      color: var(--cream);
      font-weight: 600;
      font-size: 15px;
      padding: 14px 28px;
      border-radius: var(--radius);
      text-decoration: none;
      border: 1px solid rgba(245,240,232,.25);
      transition: border-color .2s, background .2s;
    }
    .btn-ghost:hover { border-color: var(--gold); background: rgba(200,146,42,.06); }

    .hero-badges {
      display: flex; gap: 20px; margin-top: 24px; flex-wrap: wrap;
    }
    .badge {
      display: flex; align-items: center; gap: 6px;
      font-size: 12px; color: var(--muted);
    }
    .badge .dot { width: 6px; height: 6px; border-radius: 50%; background: var(--gold); }

    /* ── CHAT MOCKUP ────────────────────────────────────── */
    .chat-card {
      background: var(--card-bg);
      border: 1px solid var(--card-br);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 24px 60px rgba(0,0,0,.5);
    }
    .chat-header {
      background: var(--card-br);
      padding: 14px 18px;
      display: flex; align-items: center; gap: 10px;
    }
    .chat-avatar {
      width: 36px; height: 36px; border-radius: 50%;
      background: linear-gradient(135deg, var(--gold), var(--rust));
      display: flex; align-items: center; justify-content: center;
      font-size: 18px;
    }
    .chat-info { flex: 1; }
    .chat-name { font-size: 13px; font-weight: 600; color: var(--white); }
    .chat-status { font-size: 11px; color: var(--gold); }
    .chat-dot {
      width: 8px; height: 8px; border-radius: 50%;
      background: #4ade80;
      box-shadow: 0 0 6px #4ade80;
    }

    .chat-body { padding: 18px; display: flex; flex-direction: column; gap: 12px; }

    .msg { max-width: 80%; }
    .msg-in {
      align-self: flex-start;
      background: #2a2420;
      color: var(--cream);
      padding: 10px 14px;
      border-radius: 4px 14px 14px 14px;
      font-size: 13px;
    }
    .msg-out {
      align-self: flex-end;
      background: linear-gradient(135deg, #c8922a, #a87520);
      color: var(--ink);
      padding: 10px 14px;
      border-radius: 14px 4px 14px 14px;
      font-size: 13px;
      font-weight: 500;
    }
    .msg-time { font-size: 10px; color: var(--muted); margin-top: 4px; }

    .chat-metric {
      border-top: 1px solid var(--card-br);
      padding: 12px 18px;
      display: flex; align-items: center; gap: 8px;
    }
    .metric-num {
      font-family: var(--ff-display);
      font-size: 28px;
      color: var(--gold);
      letter-spacing: .02em;
    }
    .metric-label { font-size: 11px; color: var(--muted); line-height: 1.3; }

    /* ── PROBLEMA ───────────────────────────────────────── */
    .section { padding: 96px 0; }
    .section-label {
      font-family: var(--ff-mono);
      font-size: 11px;
      letter-spacing: .15em;
      text-transform: uppercase;
      color: var(--gold);
      margin-bottom: 12px;
    }
    h2 {
      font-family: var(--ff-display);
      font-size: clamp(36px, 5vw, 56px);
      letter-spacing: .02em;
      line-height: 1.05;
      margin-bottom: 16px;
    }
    .section-sub {
      font-size: 16px;
      color: rgba(245,240,232,.65);
      max-width: 560px;
      margin-bottom: 56px;
    }

    .problems-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2px;
    }
    .problem-card {
      background: rgba(26,22,18,.8);
      border: 1px solid var(--card-br);
      padding: 36px 28px;
      position: relative;
      transition: border-color .25s;
    }
    .problem-card:hover { border-color: rgba(200,146,42,.4); }
    .problem-icon {
      font-size: 32px;
      margin-bottom: 16px;
      display: block;
    }
    .problem-card h3 {
      font-family: var(--ff-display);
      font-size: 22px;
      letter-spacing: .04em;
      margin-bottom: 10px;
      color: var(--white);
    }
    .problem-card p { font-size: 14px; color: var(--muted); line-height: 1.65; }
    .problem-loss {
      margin-top: 16px;
      font-family: var(--ff-mono);
      font-size: 11px;
      color: var(--rust);
      letter-spacing: .08em;
    }

    /* ── HOW IT WORKS ───────────────────────────────────── */
    .how-section { background: rgba(200,146,42,.04); border-top: 1px solid rgba(200,146,42,.12); border-bottom: 1px solid rgba(200,146,42,.12); }

    .steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 40px; margin-top: 56px; }
    .step { position: relative; }
    .step-num {
      font-family: var(--ff-display);
      font-size: 64px;
      color: rgba(200,146,42,.18);
      line-height: 1;
      margin-bottom: 8px;
    }
    .step h3 {
      font-family: var(--ff-display);
      font-size: 22px;
      letter-spacing: .04em;
      color: var(--white);
      margin-bottom: 10px;
    }
    .step p { font-size: 14px; color: var(--muted); line-height: 1.65; }
    .step-connector {
      position: absolute; top: 32px; right: -20px;
      width: 40px; height: 1px;
      background: linear-gradient(to right, rgba(200,146,42,.4), transparent);
    }
    .step:last-child .step-connector { display: none; }

    /* ── AGENDA ─────────────────────────────────────────── */
    .agenda-grid {
      display: grid; grid-template-columns: 1fr 1fr; gap: 56px; align-items: center;
    }

    .agenda-ui {
      background: var(--card-bg);
      border: 1px solid var(--card-br);
      border-radius: 12px;
      overflow: hidden;
    }
    .agenda-header {
      background: var(--card-br);
      padding: 14px 18px;
      display: flex; align-items: center; justify-content: space-between;
    }
    .agenda-title { font-size: 13px; font-weight: 600; }
    .agenda-date { font-size: 11px; color: var(--muted); }

    .agenda-slot {
      display: flex; align-items: stretch;
      border-bottom: 1px solid rgba(42,36,32,.8);
      font-size: 13px;
    }
    .slot-time {
      padding: 14px 14px;
      font-family: var(--ff-mono);
      font-size: 11px;
      color: var(--muted);
      min-width: 50px;
      border-right: 1px solid rgba(42,36,32,.8);
    }
    .slot-content { padding: 10px 14px; flex: 1; }
    .slot-name { font-weight: 600; color: var(--cream); font-size: 13px; }
    .slot-service { font-size: 11px; color: var(--muted); margin-top: 2px; }
    .slot-badge {
      margin-top: 4px;
      display: inline-block;
      font-size: 9px;
      padding: 2px 8px;
      border-radius: 20px;
      font-family: var(--ff-mono);
      letter-spacing: .06em;
    }
    .badge-ai { background: rgba(200,146,42,.15); color: var(--gold); }
    .badge-free { background: rgba(74,222,128,.1); color: #4ade80; }
    .badge-manual { background: rgba(99,102,241,.1); color: #818cf8; }

    .agenda-features { display: flex; flex-direction: column; gap: 24px; }
    .feat { display: flex; gap: 16px; }
    .feat-icon {
      width: 40px; height: 40px; border-radius: 8px;
      background: rgba(200,146,42,.12);
      border: 1px solid rgba(200,146,42,.2);
      display: flex; align-items: center; justify-content: center;
      font-size: 18px; flex-shrink: 0;
    }
    .feat-text h4 { font-size: 15px; font-weight: 600; color: var(--white); margin-bottom: 4px; }
    .feat-text p { font-size: 13px; color: var(--muted); line-height: 1.6; }

    /* ── REMINDER ───────────────────────────────────────── */
    .reminder-section { background: rgba(139,44,12,.05); border-top: 1px solid rgba(139,44,12,.15); border-bottom: 1px solid rgba(139,44,12,.15); }

    .reminder-grid { display: grid; grid-template-columns: 1fr 380px; gap: 60px; align-items: center; }

    .reminder-card {
      background: var(--card-bg);
      border: 1px solid var(--card-br);
      border-radius: 12px;
      padding: 24px;
    }
    .reminder-msg {
      background: #2a2420;
      border-radius: 4px 12px 12px 12px;
      padding: 14px 16px;
      font-size: 14px;
      color: var(--cream);
      line-height: 1.6;
      margin-bottom: 12px;
    }
    .reminder-reply {
      background: linear-gradient(135deg, #c8922a, #a87520);
      border-radius: 12px 4px 12px 12px;
      padding: 12px 16px;
      font-size: 14px;
      color: var(--ink);
      font-weight: 500;
      text-align: right;
    }
    .reminder-stat {
      margin-top: 20px;
      padding: 14px;
      background: rgba(200,146,42,.06);
      border: 1px solid rgba(200,146,42,.15);
      border-radius: 8px;
      text-align: center;
    }
    .stat-big {
      font-family: var(--ff-display);
      font-size: 42px;
      color: var(--gold);
    }
    .stat-desc { font-size: 12px; color: var(--muted); margin-top: 2px; }

    .reminder-bullets { display: flex; flex-direction: column; gap: 16px; }
    .rb { display: flex; align-items: flex-start; gap: 12px; font-size: 15px; color: var(--cream); }
    .rb::before { content: '✓'; color: var(--gold); font-weight: 700; flex-shrink: 0; margin-top: 2px; }

    /* ── PRICING ────────────────────────────────────────── */
    .price-center { text-align: center; }
    .price-center .section-sub { margin: 0 auto 56px; }
    .price-card {
      background: var(--card-bg);
      border: 1px solid rgba(200,146,42,.35);
      border-radius: 16px;
      padding: 48px 40px;
      max-width: 480px;
      margin: 0 auto;
      position: relative;
      overflow: hidden;
    }
    .price-card::before {
      content: '';
      position: absolute; top: 0; left: 0; right: 0; height: 3px;
      background: linear-gradient(to right, var(--gold), var(--gold-lt));
    }
    .price-badge {
      position: absolute; top: 24px; right: 24px;
      background: var(--gold);
      color: var(--ink);
      font-size: 10px;
      font-weight: 700;
      font-family: var(--ff-mono);
      letter-spacing: .1em;
      text-transform: uppercase;
      padding: 4px 10px;
      border-radius: 20px;
    }
    .price-desc { font-size: 15px; color: var(--muted); margin-bottom: 32px; }
    .price-list { list-style: none; display: flex; flex-direction: column; gap: 12px; margin-bottom: 36px; text-align: left; }
    .price-list li { display: flex; align-items: center; gap: 10px; font-size: 14px; color: var(--cream); }
    .price-list li::before { content: '✓'; color: var(--gold); font-weight: 700; }
    .price-note { font-size: 12px; color: var(--muted); margin-top: 16px; }
    .price-full { width: 100%; text-align: center; }

    /* ── DEPOIMENTOS ────────────────────────────────────── */
    .depo-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin-top: 56px; }
    .depo {
      background: var(--card-bg);
      border: 1px solid var(--card-br);
      border-radius: 12px;
      padding: 28px 24px;
      position: relative;
    }
    .depo::before {
      content: '"';
      font-family: Georgia, serif;
      font-size: 80px;
      color: rgba(200,146,42,.15);
      position: absolute;
      top: 8px; left: 20px;
      line-height: 1;
    }
    .depo-text { font-size: 14px; color: var(--cream); line-height: 1.7; margin-bottom: 20px; margin-top: 20px; position: relative; z-index: 1; }
    .depo-author { font-weight: 600; font-size: 13px; color: var(--white); }
    .depo-role { font-size: 12px; color: var(--muted); }

    /* ── FAQ ────────────────────────────────────────────── */
    .faq-list { max-width: 680px; margin: 48px auto 0; display: flex; flex-direction: column; gap: 2px; }
    .faq-item {
      background: var(--card-bg);
      border: 1px solid var(--card-br);
      border-radius: var(--radius);
      overflow: hidden;
    }
    .faq-q {
      padding: 18px 22px;
      font-weight: 600; font-size: 15px;
      cursor: pointer;
      display: flex; align-items: center; justify-content: space-between;
      color: var(--cream);
      transition: color .2s;
    }
    .faq-q:hover { color: var(--gold); }
    .faq-arrow { font-size: 18px; color: var(--gold); transition: transform .3s; }
    .faq-a {
      display: none;
      padding: 0 22px 18px;
      font-size: 14px; color: var(--muted); line-height: 1.7;
    }
    .faq-item.open .faq-a { display: block; }
    .faq-item.open .faq-arrow { transform: rotate(180deg); }

    /* ── CTA FINAL ──────────────────────────────────────── */
    .cta-section {
      padding: 96px 0;
      text-align: center;
      background: linear-gradient(180deg, transparent, rgba(200,146,42,.05));
    }
    .cta-section h2 { margin-bottom: 20px; }
    .cta-section .section-sub { margin: 0 auto 40px; }
    .cta-badges { display: flex; gap: 24px; justify-content: center; margin-top: 24px; flex-wrap: wrap; }

    /* ── FOOTER ─────────────────────────────────────────── */
    footer {
      border-top: 1px solid var(--card-br);
      padding: 40px 0;
    }
    .footer-inner {
      display: flex; align-items: center; justify-content: space-between; flex-wrap: gap;
      gap: 16px;
    }
    .footer-logo { font-family: var(--ff-display); font-size: 22px; color: var(--white); }
    .footer-logo span { color: var(--gold); }
    .footer-links { display: flex; gap: 24px; }
    .footer-links a { font-size: 13px; color: var(--muted); text-decoration: none; transition: color .2s; }
    .footer-links a:hover { color: var(--gold); }
    .footer-copy { font-size: 12px; color: var(--muted); }

    /* ── DIVIDER ────────────────────────────────────────── */
    .divider {
      border: none;
      height: 1px;
      background: linear-gradient(to right, transparent, rgba(200,146,42,.2), transparent);
    }

    /* ── RESPONSIVE ─────────────────────────────────────── */
    @media (max-width: 900px) {
      .hero-grid { grid-template-columns: 1fr; }
      .chat-card { max-width: 480px; }
      .problems-grid { grid-template-columns: 1fr; }
      .steps { grid-template-columns: 1fr; }
      .step-connector { display: none; }
      .agenda-grid { grid-template-columns: 1fr; }
      .reminder-grid { grid-template-columns: 1fr; }
      .depo-grid { grid-template-columns: 1fr; }
      .footer-inner { flex-direction: column; text-align: center; }
    }

    @media (max-width: 600px) {
      h1 { font-size: 44px; }
      h2 { font-size: 32px; }
      .section { padding: 64px 0; }
    }

    @media (prefers-reduced-motion: reduce) {
      * { animation: none !important; transition: none !important; }
    }
  </style>
</head>
<body>

<!-- ── NAV ──────────────────────────────────────────── -->
<nav>
  <div class="nav-inner">
    <a class="logo" href="#">Barber<span>Bot</span> AI</a>
    <ul class="nav-links">
      <li><a href="#problema">O Problema</a></li>
      <li><a href="#como-funciona">Como Funciona</a></li>
      <li><a href="#agenda">Agenda</a></li>
      <li><a href="#contato" class="btn-nav">Falar com Especialista</a></li>
    </ul>
  </div>
</nav>

<!-- ── HERO ─────────────────────────────────────────── -->
<section class="hero">
  <div class="container">
    <div class="hero-grid">

      <div>
        <div class="hero-eyebrow">
          <span class="tag">💈 IA disponível 24 horas por dia</span>
        </div>
        <h1>
          Sua barbearia<br>
          lotada,<br>
          <span class="line-accent">sem esforço</span>
        </h1>
        <p class="hero-sub">
          O agente de IA que agenda cortes, tirar dúvidas e confirma horários no WhatsApp — enquanto você foca na navalha.
        </p>
        <div class="hero-ctas">
          <a href="#contato" class="btn-primary">Falar com Especialista</a>
          <a href="#como-funciona" class="btn-ghost">Ver como funciona →</a>
        </div>
        <div class="hero-badges">
          <span class="badge"><span class="dot"></span>Fácil de configurar</span>
          <span class="badge"><span class="dot"></span>Suporte em português</span>
          <span class="badge"><span class="dot"></span>Cancele a qualquer hora</span>
        </div>
      </div>

      <div>
        <div class="chat-card">
          <div class="chat-header">
            <div class="chat-avatar">💈</div>
            <div class="chat-info">
              <div class="chat-name">BarberBot AI — Barbearia do Pedro</div>
              <div class="chat-status">● Online agora</div>
            </div>
            <div class="chat-dot"></div>
          </div>
          <div class="chat-body">
            <div class="msg msg-in">
              Oi! Tem horário hoje pra corte e barba?
            </div>
            <small class="msg-time">10:23</small>

            <div class="msg msg-out">
              Oi! Tem sim 💈 Hoje temos:<br>
              <strong>14h</strong> com Rodrigo<br>
              <strong>16h</strong> com Diego<br><br>
              Qual prefere?
            </div>
            <small class="msg-time" style="text-align:right;display:block">10:23</small>

            <div class="msg msg-in">
              Às 14h com o Rodrigo! Quanto fica?
            </div>

            <div class="msg msg-out">
              Corte + barba: <strong>R$ 65</strong>.<br>
              Agendado! ✅ Te espero às 14h, pode vir na rua XV, n° 210.
            </div>

          </div>
          <div class="chat-metric">
            <div>
              <div class="metric-num">+43</div>
              <div class="metric-label">agendamentos<br>esta semana via IA</div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<hr class="divider" />

<!-- ── PROBLEMA ──────────────────────────────────────── -->
<section class="section" id="problema">
  <div class="container">
    <div class="section-label">O problema</div>
    <h2>Você perde dinheiro toda vez que…</h2>
    <p class="section-sub">Cada mensagem não respondida é um corte que vai parar na barbearia ao lado.</p>

    <div class="problems-grid">
      <div class="problem-card">
        <span class="problem-icon">📵</span>
        <h3>Não Atende na Hora</h3>
        <p>O cliente manda mensagem perguntando sobre horário. Você está com a tesoura na mão. Ele não espera e marca em outra barbearia.</p>
        <div class="problem-loss">↑ RECEITA PERDIDA</div>
      </div>
      <div class="problem-card">
        <span class="problem-icon">🪑</span>
        <h3>Cadeira Vazia (No-Show)</h3>
        <p>Você reservou o horário, preparou tudo... e o cliente não apareceu. Tempo perdido que virou prejuízo direto no seu caixa.</p>
        <div class="problem-loss">↑ CADEIRA VAZIA</div>
      </div>
      <div class="problem-card">
        <span class="problem-icon">🌙</span>
        <h3>Depois do Expediente</h3>
        <p>Muitos homens querem marcar à noite ou no fim de semana. Se você não está online, perde o cliente para quem está.</p>
        <div class="problem-loss">↑ CLIENTES PERDIDOS</div>
      </div>
    </div>
  </div>
</section>

<!-- ── COMO FUNCIONA ──────────────────────────────────── -->
<section class="section how-section" id="como-funciona">
  <div class="container">
    <div class="section-label">Solução</div>
    <h2>Configurado em 3 passos,<br>funcionando em minutos</h2>
    <p class="section-sub">Não precisa saber de tecnologia. Se você sabe usar WhatsApp, você consegue usar o BarberBot AI.</p>

    <div class="steps">
      <div class="step">
        <div class="step-num">01</div>
        <h3>Configure a Agenda</h3>
        <p>Defina seus barbeiros, horários de atendimento e serviços (corte, barba, degradê, etc.) no painel simples.</p>
        <div class="step-connector"></div>
      </div>
      <div class="step">
        <div class="step-num">02</div>
        <h3>Treine a IA</h3>
        <p>Informe os preços, o endereço e as regras da sua barbearia. A IA aprende tudo e já sabe responder como você responderia.</p>
        <div class="step-connector"></div>
      </div>
      <div class="step">
        <div class="step-num">03</div>
        <h3>Ative no WhatsApp</h3>
        <p>Leia o QR Code com seu celular e pronto. O BarberBot AI assume as conversas e começa a lotar sua agenda.</p>
      </div>
    </div>
  </div>
</section>

<!-- ── AGENDA ─────────────────────────────────────────── -->
<section class="section" id="agenda">
  <div class="container">
    <div class="agenda-grid">

      <div class="agenda-ui">
        <div class="agenda-header">
          <span class="agenda-title">Agenda — Barbearia do Pedro</span>
          <span class="agenda-date">Hoje, quarta-feira</span>
        </div>

        <div class="agenda-slot">
          <div class="slot-time">09:00</div>
          <div class="slot-content">
            <div class="slot-name">Carlos Mendes</div>
            <div class="slot-service">Corte + Barba · Rodrigo</div>
            <span class="slot-badge badge-ai">Agendado via IA</span>
          </div>
        </div>
        <div class="agenda-slot">
          <div class="slot-time">10:30</div>
          <div class="slot-content">
            <div class="slot-name">Lucas Ferreira</div>
            <div class="slot-service">Degradê · Diego</div>
            <span class="slot-badge badge-manual">Presencial</span>
          </div>
        </div>
        <div class="agenda-slot">
          <div class="slot-time">11:00</div>
          <div class="slot-content">
            <div class="slot-name">Horário Livre</div>
            <div class="slot-service">Rodrigo</div>
            <span class="slot-badge badge-free">Disponível</span>
          </div>
        </div>
        <div class="agenda-slot" style="border-bottom:none">
          <div class="slot-time">14:00</div>
          <div class="slot-content">
            <div class="slot-name">André Lima</div>
            <div class="slot-service">Barba completa · Rodrigo</div>
            <span class="slot-badge badge-ai">Agendado via IA</span>
          </div>
        </div>

        <div style="padding:14px 18px;border-top:1px solid #2a2420;background:rgba(200,146,42,.04);font-size:12px;color:var(--muted)">
          💬 Enviado automaticamente 2h antes:<br>
          <em style="color:var(--cream)">"Oi André! Seu corte é hoje às 14h com o Rodrigo. Tá confirmado? ✂️"</em>
        </div>
      </div>

      <div class="agenda-features">
        <div class="section-label">Gestão completa</div>
        <h2 style="font-size:clamp(30px,4vw,44px);margin-bottom:8px">Uma agenda poderosa, sem complicação</h2>
        <p style="font-size:15px;color:var(--muted);margin-bottom:32px;line-height:1.7">Esqueça cadernos e WhatsApp desorganizado. Você e sua equipe têm visão total de todos os horários.</p>

        <div class="feat">
          <div class="feat-icon">✂️</div>
          <div class="feat-text">
            <h4>Todos os Barbeiros</h4>
            <p>Gerencie a agenda de todos os profissionais em um único painel. Cada um com seus horários.</p>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon">💬</div>
          <div class="feat-text">
            <h4>Entende Áudios do WhatsApp</h4>
            <p>A IA transcreve e entende mensagens de voz. Seu cliente pode falar no áudio que ela responde.</p>
          </div>
        </div>
        <div class="feat">
          <div class="feat-icon">🎯</div>
          <div class="feat-text">
            <h4>Barbeiro Favorito</h4>
            <p>Se o cliente pedir um barbeiro específico, a IA mostra só os horários disponíveis daquele profissional.</p>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<hr class="divider" />

<!-- ── LEMBRETES ──────────────────────────────────────── -->
<section class="section reminder-section">
  <div class="container">
    <div class="reminder-grid">

      <div>
        <div class="section-label">Sem faltas</div>
        <h2>Lembretes que garantem a presença</h2>
        <p style="font-size:15px;color:var(--muted);margin:16px 0 32px;line-height:1.7">
          Cliente que esquece do horário é cadeira vazia. O BarberBot AI nunca esquece — manda lembrete automático e pede confirmação.
        </p>
        <div class="reminder-bullets">
          <div class="rb">Reduza faltas em até 40%</div>
          <div class="rb">Se o cliente cancelar, a IA libera o horário na hora</div>
          <div class="rb">Você foca no corte, a IA cuida do resto</div>
        </div>
      </div>

      <div>
        <div class="reminder-card">
          <div class="reminder-msg">
            💈 Oi, André! Só lembrando que seu corte é <strong>hoje às 14h</strong> com o Rodrigo, na Barbearia do Pedro.<br><br>
            Confirma presença? ✂️
          </div>
          <div class="reminder-reply">
            Confirmado! Já tô saindo 👊
          </div>
          <div class="reminder-stat">
            <div class="stat-big">-40%</div>
            <div class="stat-desc">redução de no-show com lembretes automáticos</div>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ── PRICING ───────────────────────────────────────── -->
<section class="section" id="preco">
  <div class="container">
    <div class="price-center">
      <div class="section-label">Investimento</div>
      <h2>Quanto custa um cliente perdido?</h2>
      <p class="section-sub">Se a IA recuperar apenas <strong style="color:var(--gold)">1 cliente por mês</strong>, ela já se paga. Imagine recuperar dezenas.</p>
        <div class="price-badge">Mais popular</div>
        <p class="price-desc">Acesso completo. Sem surpresas.</p>
        <ul class="price-list">
          <li>Agendamentos ilimitados via WhatsApp</li>
          <li>Agenda visual para toda a equipe</li>
          <li>Lembretes automáticos e confirmação</li>
          <li>IA que entende áudios de WhatsApp</li>
          <li>Suporte por profissional específico</li>
          <li>Painel de gestão completo</li>
          <li>Suporte via WhatsApp</li>
        </ul>
        <a href="#contato" class="btn-primary price-full">Quero o BarberBot AI</a>
        <p class="price-note">• Cancele a qualquer momento</p>
      </div>
    </div>
  </div>
</section>

<!-- ── DEPOIMENTOS ────────────────────────────────────── -->
<section class="section" style="padding-top:0" id="depoimentos">
  <div class="container">
    <div class="section-label" style="text-align:center">Depoimentos</div>
    <h2 style="text-align:center">O que dizem os barbeiros</h2>

    <div class="depo-grid">
      <div class="depo">
        <p class="depo-text">No primeiro dia já vieram 12 agendamentos pelo WhatsApp sem eu precisar responder nada. Parece mágica.</p>
        <div class="depo-author">Rodrigo S.</div>
        <div class="depo-role">Dono, Barbearia Clássica — SP</div>
      </div>
      <div class="depo">
        <p class="depo-text">Meus clientes não percebem que é uma IA. O atendimento ficou mais rápido do que quando era eu mesmo respondendo.</p>
        <div class="depo-author">Diego M.</div>
        <div class="depo-role">Barbeiro, Studio 74 — RJ</div>
      </div>
      <div class="depo">
        <p class="depo-text">Acabou com as faltas. Os lembretes automáticos fizeram a diferença — minha agenda tá sempre lotada agora.</p>
        <div class="depo-author">André L.</div>
        <div class="depo-role">Proprietário, Old School Barber — BH</div>
      </div>
    </div>
  </div>
</section>

<!-- ── FAQ ────────────────────────────────────────────── -->
<section class="section" style="padding-top:0" id="faq">
  <div class="container">
    <div class="section-label" style="text-align:center">Dúvidas frequentes</div>
    <h2 style="text-align:center">Perguntas & Respostas</h2>

    <div class="faq-list">

      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">
          A IA sabe os preços e serviços da minha barbearia?
          <span class="faq-arrow">⌄</span>
        </div>
        <div class="faq-a">Sim! Você cadastra sua tabela completa (corte, barba, degradê, progressiva, etc.) com preços e duração de cada serviço. A IA consulta esses dados antes de responder qualquer cliente.</div>
      </div>

      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">
          Posso usar meu número atual do WhatsApp?
          <span class="faq-arrow">⌄</span>
        </div>
        <div class="faq-a">Com certeza. A conexão é feita via QR Code, igual ao WhatsApp Web. Você continua usando o mesmo número que já usa na barbearia e pode intervir nas conversas sempre que quiser.</div>
      </div>

      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">
          E se o cliente quiser um barbeiro específico?
          <span class="faq-arrow">⌄</span>
        </div>
        <div class="faq-a">A IA entende isso! Se o cliente pedir o Rodrigo, ela verifica a agenda do Rodrigo e mostra somente os horários disponíveis dele. Preferência respeitada.</div>
      </div>

      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">
          Quanto tempo leva para configurar?
          <span class="faq-arrow">⌄</span>
        </div>
        <div class="faq-a">Em média 20 a 30 minutos. Nossa equipe pode te ajudar por WhatsApp em todo o processo. A maioria dos barbeiros ativa no mesmo dia em que se cadastra.</div>
      </div>

      <div class="faq-item">
        <div class="faq-q" onclick="toggleFaq(this)">
          O cliente sabe que está falando com uma IA?
          <span class="faq-arrow">⌄</span>
        </div>
        <div class="faq-a">A IA responde de forma natural e fluída. Muitos clientes nem percebem. Se o cliente perguntar diretamente, a IA pode ser configurada para revelar — ou você pode personalizar o comportamento.</div>
      </div>

    </div>
  </div>
</section>

<!-- ── CTA FINAL ──────────────────────────────────────── -->
<section class="cta-section" id="contato">
  <div class="container">
    <div class="tag" style="margin-bottom:20px">Comece agora</div>
    <h2>Sua barbearia,<br>trabalhando <span class="gold">enquanto você dorme</span></h2>
    <p class="section-sub">Fale com um especialista e veja como o BarberBot AI se encaixa na sua barbearia.</p>
    <a href="https://wa.me/5500000000000?text=Olá! Quero saber mais sobre o BarberBot AI" class="btn-primary" style="font-size:16px;padding:16px 36px">
      💬 Falar com Especialista
    </a>
    <div class="cta-badges">
      <span class="badge"><span class="dot"></span>Acesso completo</span>
      <span class="badge"><span class="dot"></span>Suporte em português</span>
      <span class="badge"><span class="dot"></span>Cancele a qualquer hora</span>
    </div>
  </div>
</section>

<!-- ── FOOTER ─────────────────────────────────────────── -->
<footer>
  <div class="container">
    <div class="footer-inner">
      <div class="footer-logo">Barber<span>Bot</span> AI</div>
      <div class="footer-links">
        <a href="#">Termos de uso</a>
        <a href="#">Privacidade</a>
        <a href="#contato">Contato</a>
      </div>
      <p class="footer-copy">© 2025 BarberBot AI. Todos os direitos reservados.</p>
    </div>
  </div>
</footer>

<script>
  function toggleFaq(el) {
    const item = el.parentElement;
    item.classList.toggle('open');
  }
</script>

</body>
</html>
