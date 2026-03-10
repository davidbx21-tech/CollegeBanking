<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>כנס הבנקאות והמשפט 2026</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;600;700&family=Heebo:wght@300;400;500;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --gold: #c9a84c;
      --gold-light: #e8c97a;
      --gold-pale: #f5e9c8;
      --dark: #0d0d12;
      --dark-card: #13131c;
      --dark-mid: #1c1c2e;
      --dark-border: #2a2a3e;
      --text-main: #e8e4da;
      --text-muted: #9a9385;
      --accent: #3a6ea8;
    }

    * { margin: 0; padding: 0; box-sizing: border-box; }

    body {
      background: var(--dark);
      color: var(--text-main);
      font-family: 'Heebo', sans-serif;
      min-height: 100vh;
      overflow-x: hidden;
    }

    body::before {
      content: '';
      position: fixed; inset: 0;
      background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.75' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
      pointer-events: none; z-index: 0; opacity: 0.35;
    }

    /* ── HEADER ── */
    header {
      position: relative; z-index: 10;
      padding: 2.5rem 2rem 2.5rem;
      text-align: center;
      border-bottom: 1px solid var(--dark-border);
      background: linear-gradient(180deg, #0a0a10 0%, var(--dark) 100%);
    }

    /* Faculty logo - top left corner */
    .faculty-logo-wrap {
      position: absolute;
      top: 1.2rem;
      left: 1.5rem;
      opacity: 0.75;
      transition: opacity 0.3s;
    }
    .faculty-logo-wrap:hover { opacity: 1; }
    .faculty-logo-wrap img {
      height: 42px;
      width: auto;
      filter: brightness(0) invert(1) opacity(0.6);
    }

    /* Clinic logo - centered above title */
    .clinic-logo-wrap {
      display: flex;
      justify-content: center;
      margin-bottom: 2rem;
    }
    .clinic-logo-wrap img {
      height: 130px;
      width: auto;
      border-radius: 0;
      background: transparent;
      padding: 0;
      box-shadow: none;
    }

    .header-badge {
      display: inline-block;
      border: 1px solid var(--gold);
      color: var(--gold);
      font-size: 0.7rem;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      padding: 0.35em 1.2em;
      margin-bottom: 1.2rem;
      font-family: 'Heebo', sans-serif;
      font-weight: 500;
    }

    header h1 {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(2.4rem, 6vw, 4.4rem);
      font-weight: 600;
      line-height: 1.1;
      background: linear-gradient(135deg, var(--gold-pale) 0%, var(--gold) 50%, #a07828 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 1rem;
    }

    header .subtitle {
      font-size: 0.95rem;
      color: var(--text-muted);
      font-weight: 300;
      letter-spacing: 0.04em;
      max-width: 700px;
      margin: 0 auto;
    }

    .header-meta {
      display: flex;
      justify-content: center;
      gap: 2.5rem;
      margin-top: 1.8rem;
      flex-wrap: wrap;
    }

    .meta-item {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 0.85rem;
      color: var(--text-muted);
    }
    .meta-item .icon { color: var(--gold); font-size: 1rem; }
    .meta-item strong { color: var(--text-main); font-weight: 500; }

    .gold-line {
      width: 80px; height: 1px;
      background: linear-gradient(90deg, transparent, var(--gold), transparent);
      margin: 1.5rem auto 0;
    }

    /* ── GRID ── */
    .grid {
      position: relative; z-index: 5;
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1px;
      background: var(--dark-border);
    }

    /* ── CARD BASE ── */
    .card {
      background: var(--dark-card);
      padding: 3rem 2.8rem;
      position: relative;
      overflow: hidden;
    }

    .card-accent {
      position: absolute;
      top: 0; right: 0;
      width: 4px; height: 100%;
    }
    .card-1 .card-accent { background: linear-gradient(180deg, var(--gold), transparent); }
    .card-2 .card-accent { background: linear-gradient(180deg, #3a6ea8, transparent); }
    .card-3 .card-accent { background: linear-gradient(180deg, #4a9068, transparent); }
    .card-4 .card-accent { background: linear-gradient(180deg, #8a4a9a, transparent); }

    .card-number {
      font-family: 'Cormorant Garamond', serif;
      font-size: 5rem;
      font-weight: 300;
      position: absolute;
      left: 1.5rem; top: 1rem;
      opacity: 0.06; line-height: 1;
      pointer-events: none;
    }

    .card-tag {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      font-size: 0.68rem;
      font-weight: 700;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      padding: 0.3em 0.85em;
      border-radius: 2px;
      margin-bottom: 1.4rem;
    }
    .card-1 .card-tag { background: rgba(201,168,76,0.12); color: var(--gold); border: 1px solid rgba(201,168,76,0.3); }
    .card-2 .card-tag { background: rgba(58,110,168,0.12); color: #7aa8d8; border: 1px solid rgba(58,110,168,0.3); }
    .card-3 .card-tag { background: rgba(74,144,104,0.12); color: #7abf98; border: 1px solid rgba(74,144,104,0.3); }
    .card-4 .card-tag { background: rgba(138,74,154,0.12); color: #c07ad8; border: 1px solid rgba(138,74,154,0.3); }

    .card h2 {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(1.6rem, 2.5vw, 2.2rem);
      font-weight: 600;
      line-height: 1.2;
      margin-bottom: 0.6rem;
      color: var(--text-main);
    }

    .card-divider { width: 40px; height: 1px; margin: 1rem 0 1.4rem; }
    .card-1 .card-divider { background: var(--gold); }
    .card-2 .card-divider { background: #3a6ea8; }
    .card-3 .card-divider { background: #4a9068; }
    .card-4 .card-divider { background: #8a4a9a; }

    .card p.lead {
      font-size: 0.95rem;
      line-height: 1.8;
      color: var(--text-muted);
      margin-bottom: 1.5rem;
    }

    /* CARD 1 */
    .keynote-speaker {
      display: flex; align-items: center; gap: 1.2rem;
      padding: 1.2rem;
      background: rgba(201,168,76,0.06);
      border: 1px solid rgba(201,168,76,0.15);
      border-radius: 4px; margin-top: 1rem;
    }
    .speaker-avatar {
      width: 56px; height: 56px; border-radius: 50%;
      background: linear-gradient(135deg, #c9a84c33, #c9a84c88);
      border: 2px solid var(--gold);
      display: flex; align-items: center; justify-content: center;
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.4rem; color: var(--gold); flex-shrink: 0;
    }
    .speaker-info h3 { font-size: 1rem; font-weight: 600; color: var(--text-main); margin-bottom: 0.2rem; }
    .speaker-info p { font-size: 0.78rem; color: var(--text-muted); line-height: 1.5; }
    .keynote-topic {
      margin-top: 1.5rem; padding: 1rem 1.2rem;
      border-right: 2px solid var(--gold);
      background: rgba(255,255,255,0.02);
    }
    .keynote-topic .topic-label {
      font-size: 0.65rem; letter-spacing: 0.2em;
      text-transform: uppercase; color: var(--gold);
      font-weight: 700; margin-bottom: 0.4rem;
    }
    .keynote-topic p {
      color: var(--text-main); font-style: italic;
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.15rem; line-height: 1.5;
    }

    /* CARD 2 */
    .ted-list { display: flex; flex-direction: column; gap: 0.9rem; margin-top: 0.5rem; }
    .ted-item {
      display: flex; gap: 1rem; padding: 0.9rem 1rem;
      background: rgba(58,110,168,0.05);
      border: 1px solid rgba(58,110,168,0.12);
      border-radius: 3px; align-items: flex-start;
      transition: border-color 0.3s, background 0.3s;
    }
    .ted-item:hover { background: rgba(58,110,168,0.1); border-color: rgba(58,110,168,0.3); }
    .ted-num {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.6rem; font-weight: 300;
      color: rgba(122,168,216,0.4);
      line-height: 1; flex-shrink: 0;
      min-width: 1.8rem; text-align: center;
    }
    .ted-content .ted-title { font-size: 0.88rem; font-weight: 500; color: var(--text-main); margin-bottom: 0.2rem; line-height: 1.4; }
    .ted-content .ted-speaker { font-size: 0.75rem; color: #7aa8d8; }

    /* CARD 3 */
    .flyers-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 0.8rem; margin-top: 0.5rem; }
    .flyer-item {
      padding: 1rem;
      background: rgba(74,144,104,0.05);
      border: 1px solid rgba(74,144,104,0.15);
      border-radius: 3px; transition: all 0.3s; cursor: default;
    }
    .flyer-item:hover { background: rgba(74,144,104,0.1); border-color: rgba(74,144,104,0.3); transform: translateY(-2px); }
    .flyer-icon { font-size: 1.4rem; margin-bottom: 0.5rem; }
    .flyer-item h4 { font-size: 0.82rem; font-weight: 600; color: var(--text-main); margin-bottom: 0.3rem; line-height: 1.3; }
    .flyer-item p { font-size: 0.72rem; color: var(--text-muted); line-height: 1.5; }
    .flyer-full { grid-column: 1 / -1; }

    /* CARD 4 */
    .legal-features { display: flex; flex-direction: column; gap: 0.85rem; margin-top: 0.5rem; }
    .legal-item {
      display: flex; align-items: flex-start; gap: 0.9rem;
      padding: 0.85rem 1rem;
      background: rgba(138,74,154,0.05);
      border: 1px solid rgba(138,74,154,0.12);
      border-radius: 3px; transition: all 0.3s;
    }
    .legal-item:hover { background: rgba(138,74,154,0.1); border-color: rgba(138,74,154,0.3); }
    .legal-dot { width: 8px; height: 8px; border-radius: 50%; background: #c07ad8; flex-shrink: 0; margin-top: 0.35rem; }
    .legal-item h4 { font-size: 0.88rem; font-weight: 600; color: var(--text-main); margin-bottom: 0.2rem; }
    .legal-item p { font-size: 0.77rem; color: var(--text-muted); line-height: 1.5; }
    .cta-box {
      margin-top: 1.5rem; padding: 1.1rem 1.3rem;
      background: linear-gradient(135deg, rgba(138,74,154,0.12), rgba(138,74,154,0.04));
      border: 1px solid rgba(138,74,154,0.25);
      border-radius: 4px;
      display: flex; justify-content: space-between; align-items: center; gap: 1rem;
    }
    .cta-box p { font-size: 0.82rem; color: var(--text-muted); line-height: 1.5; }
    .cta-btn {
      background: none; border: 1px solid #c07ad8; color: #c07ad8;
      padding: 0.5em 1.2em; font-size: 0.78rem; letter-spacing: 0.08em;
      cursor: pointer; font-family: 'Heebo', sans-serif;
      white-space: nowrap; transition: all 0.3s;
      text-decoration: none; display: inline-block;
    }
    .cta-btn:hover { background: #c07ad8; color: var(--dark); }

    /* FOOTER */
    footer {
      position: relative; z-index: 10;
      padding: 2.5rem 2rem;
      text-align: center;
      border-top: 1px solid var(--dark-border);
      background: linear-gradient(0deg, #0a0a10 0%, var(--dark) 100%);
    }
    footer .footer-org { font-family: 'Cormorant Garamond', serif; font-size: 1.1rem; color: var(--gold); margin-bottom: 0.5rem; }
    footer p { font-size: 0.78rem; color: var(--text-muted); }
    .register-btn {
      display: inline-block; margin-top: 1.5rem;
      padding: 0.85em 3em;
      background: linear-gradient(135deg, var(--gold), #a07828);
      color: var(--dark); font-family: 'Heebo', sans-serif;
      font-size: 0.88rem; font-weight: 700;
      letter-spacing: 0.1em; text-transform: uppercase;
      text-decoration: none; border: none; cursor: pointer;
      transition: opacity 0.3s, transform 0.3s;
    }
    .register-btn:hover { opacity: 0.88; transform: translateY(-2px); }

    @media (max-width: 768px) {
      .grid { grid-template-columns: 1fr; }
      .card { padding: 2.2rem 1.6rem; }
      .flyers-grid { grid-template-columns: 1fr; }
      .header-meta { gap: 1.2rem; }
      .faculty-logo-wrap { position: static; margin: 0 auto 1rem; display: block; text-align: center; }
    }

    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(24px); }
      to   { opacity: 1; transform: translateY(0); }
    }
    header  { animation: fadeUp 0.7s ease both; }
    .card-1 { animation: fadeUp 0.7s 0.15s ease both; }
    .card-2 { animation: fadeUp 0.7s 0.25s ease both; }
    .card-3 { animation: fadeUp 0.7s 0.35s ease both; }
    .card-4 { animation: fadeUp 0.7s 0.45s ease both; }
    footer  { animation: fadeUp 0.7s 0.55s ease both; }
  </style>
</head>
<body>

  <header>

    <!-- Clinic logo – centered above title -->
    <div class="clinic-logo-wrap">
      <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMDAgMTQwIiB3aWR0aD0iMjAwIiBoZWlnaHQ9IjE0MCI+CiAgPGRlZnM+CiAgICA8bGluZWFyR3JhZGllbnQgaWQ9Im1nIiB4MT0iMCUiIHkxPSIwJSIgeDI9IjAlIiB5Mj0iMTAwJSI+CiAgICAgIDxzdG9wIG9mZnNldD0iMCUiICAgc3RvcC1jb2xvcj0iI2U4ZThlOCIvPgogICAgICA8c3RvcCBvZmZzZXQ9IjUwJSIgIHN0b3AtY29sb3I9IiNiOGI4YjgiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSIxMDAlIiBzdG9wLWNvbG9yPSIjODg4ODg4Ii8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogICAgPGxpbmVhckdyYWRpZW50IGlkPSJtZ2giIHgxPSIwJSIgeTE9IjAlIiB4Mj0iMTAwJSIgeTI9IjAlIj4KICAgICAgPHN0b3Agb2Zmc2V0PSIwJSIgICBzdG9wLWNvbG9yPSIjNzc3Ii8+CiAgICAgIDxzdG9wIG9mZnNldD0iNDAlIiAgc3RvcC1jb2xvcj0iI2RkZCIvPgogICAgICA8c3RvcCBvZmZzZXQ9IjYwJSIgIHN0b3AtY29sb3I9IiNlZWUiLz4KICAgICAgPHN0b3Agb2Zmc2V0PSIxMDAlIiBzdG9wLWNvbG9yPSIjNzc3Ii8+CiAgICA8L2xpbmVhckdyYWRpZW50PgogIDwvZGVmcz4KCiAgPCEtLSBCQU5LIOKAkyBjZW50cmVkIGluIDIwMC13aWRlIGNhbnZhcyAtLT4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg0OCwgNikiPgoKICAgIDwhLS0gUGVkaW1lbnQgLS0+CiAgICA8cG9seWdvbiBwb2ludHM9IjUyLDAgMTAwLDIyIDQsMjIiCiAgICAgICAgICAgICBmaWxsPSJub25lIiBzdHJva2U9InVybCgjbWdoKSIgc3Ryb2tlLXdpZHRoPSIxLjQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiLz4KCiAgICA8IS0tIEVudGFibGF0dXJlIGJhciAtLT4KICAgIDxyZWN0IHg9IjQiIHk9IjIyIiB3aWR0aD0iOTYiIGhlaWdodD0iNSIgZmlsbD0idXJsKCNtZ2gpIi8+CgogICAgPCEtLSA2IGNvbHVtbnMgLS0+CiAgICA8cmVjdCB4PSIxMCIgIHk9IjI3IiB3aWR0aD0iNiIgaGVpZ2h0PSI0NiIgZmlsbD0idXJsKCNtZykiLz4KICAgIDxyZWN0IHg9IjI2IiAgeT0iMjciIHdpZHRoPSI2IiBoZWlnaHQ9IjQ2IiBmaWxsPSJ1cmwoI21nKSIvPgogICAgPHJlY3QgeD0iNDIiICB5PSIyNyIgd2lkdGg9IjYiIGhlaWdodD0iNDYiIGZpbGw9InVybCgjbWcpIi8+CiAgICA8cmVjdCB4PSI1OCIgIHk9IjI3IiB3aWR0aD0iNiIgaGVpZ2h0PSI0NiIgZmlsbD0idXJsKCNtZykiLz4KICAgIDxyZWN0IHg9Ijc0IiAgeT0iMjciIHdpZHRoPSI2IiBoZWlnaHQ9IjQ2IiBmaWxsPSJ1cmwoI21nKSIvPgogICAgPHJlY3QgeD0iODgiICB5PSIyNyIgd2lkdGg9IjYiIGhlaWdodD0iNDYiIGZpbGw9InVybCgjbWcpIi8+CgogICAgPCEtLSBCYXNlIGJhciAtLT4KICAgIDxyZWN0IHg9IjQiICB5PSI3MyIgd2lkdGg9Ijk2IiBoZWlnaHQ9IjUiIGZpbGw9InVybCgjbWdoKSIvPgogICAgPCEtLSBTdGVwIDEgLS0+CiAgICA8cmVjdCB4PSIwIiAgeT0iNzgiIHdpZHRoPSIxMDQiIGhlaWdodD0iNCIgZmlsbD0idXJsKCNtZ2gpIiBvcGFjaXR5PSIwLjciLz4KICAgIDwhLS0gU3RlcCAyIC0tPgogICAgPHJlY3QgeD0iLTQiIHk9IjgyIiB3aWR0aD0iMTEyIiBoZWlnaHQ9IjQiIGZpbGw9InVybCgjbWdoKSIgb3BhY2l0eT0iMC40NSIvPgoKICA8L2c+CgogIDwhLS0gRElWSURFUiAtLT4KICA8bGluZSB4MT0iMjQiIHkxPSIxMDAiIHgyPSIxNzYiIHkyPSIxMDAiCiAgICAgICAgc3Ryb2tlPSIjNjY2IiBzdHJva2Utd2lkdGg9IjAuNiIgb3BhY2l0eT0iMC42Ii8+CgogIDwhLS0gVEVYVCAtLT4KICA8dGV4dCB4PSIxMDAiIHk9IjExNiIKICAgICAgICB0ZXh0LWFuY2hvcj0ibWlkZGxlIgogICAgICAgIGZvbnQtZmFtaWx5PSInSGVlYm8nLCdBcmlhbCBIZWJyZXcnLEFyaWFsLHNhbnMtc2VyaWYiCiAgICAgICAgZm9udC1zaXplPSIxNCIgZm9udC13ZWlnaHQ9IjYwMCIKICAgICAgICBsZXR0ZXItc3BhY2luZz0iMC40IgogICAgICAgIGZpbGw9IiNkMGQwZDAiPteU16fXnNeZ16DXmden15Qg15zXk9eZ16DXmSDXkdeg16fXkNeV16o8L3RleHQ+CgogIDx0ZXh0IHg9IjEwMCIgeT0iMTMyIgogICAgICAgIHRleHQtYW5jaG9yPSJtaWRkbGUiCiAgICAgICAgZm9udC1mYW1pbHk9IidIZWVibycsJ0FyaWFsIEhlYnJldycsQXJpYWwsc2Fucy1zZXJpZiIKICAgICAgICBmb250LXNpemU9IjguNSIgZm9udC13ZWlnaHQ9IjMwMCIKICAgICAgICBsZXR0ZXItc3BhY2luZz0iMC41IgogICAgICAgIGZpbGw9IiM3ODc4NzgiPteU157Xodec15XXnCDXlNeQ16fXk9ee15kg15TXnteb15zXnNeUINec157Xmdeg15TXnDwvdGV4dD4KCjwvc3ZnPg==" alt="הקליניקה לדיני בנקאות" />
    </div>

    <div class="header-badge">כנס שנתי · 2026</div>
    <h1>הבנקאות בעידן החדש<br>זכויות, רגולציה ומשפט</h1>
    <p class="subtitle">כנס מקצועי בתחום הבנקאות המשפטית · מושגי יסוד, מאפייני שוק הבנקאות בישראל, סיכונים בשוק ההון, חינוך פיננסי ועוד</p>
    <div class="header-meta">
      <div class="meta-item"><span class="icon">📅</span><span>יום שלישי, <strong>18 ביוני 2026</strong></span></div>
      <div class="meta-item"><span class="icon">📍</span><span>קמפוס המסלול האקדמי המכללה למינהל, <strong>ראשון לציון</strong></span></div>
      <div class="meta-item"><span class="icon">🕘</span><span>10:00 – 15:30</span></div>
    </div>
    <div class="gold-line"></div>
  </header>

  <div class="grid">

    <div class="card card-1">
      <div class="card-accent"></div>
      <div class="card-number">01</div>
      <div class="card-tag">⭐ הרצאה ראשית</div>
      <h2>נאום הפתיחה המרכזי</h2>
      <div class="card-divider"></div>
      <p class="lead">הרצאת הדגל של הכנס תפתח את היום ותציב את המסגרת המשפטית והכלכלית לדיון. מיועדת לכלל המשתתפים.</p>
      <div class="keynote-speaker">
        <div class="speaker-avatar">פ"מ</div>
        <div class="speaker-info">
          <h3>פרופ' ירון זליכה</h3>
          <p>ראש החוג לחשבונאות, הקריה האקדמית אונו<br>החשב הכללי של משרד האוצר לשעבר</p>
        </div>
      </div>
      <div class="keynote-topic">
        <div class="topic-label">נושא ההרצאה</div>
        <p>"אתגר הריכוזיות במשק הישראלי: השפעתם של מונופולים על השווקים בישראל, מאפייני הריכוזיות המשקית ועוד"</p>
      </div>
    </div>

    <div class="card card-2">
      <div class="card-accent"></div>
      <div class="card-number">02</div>
      <div class="card-tag">🎤 הרצאות TED</div>
      <h2>ארבע הרצאות מומחים</h2>
      <div class="card-divider"></div>
      <p class="lead">הרצאות קצרות ומחדדות בפורמט TED – כל הרצאה 18 דקות, ממוקדת, עם מסר אחד חזק.</p>
      <div class="ted-list">
        <div class="ted-item">
          <div class="ted-num">1</div>
          <div class="ted-content">
            <div class="ted-title">תפקידיו של בנק ישראל - פיקוח וזכויות</div>
            <div class="ted-speaker">עו"ד ירון מלכה · בכיר בבנק ישראל</div>
          </div>
        </div>
        <div class="ted-item">
          <div class="ted-num">2</div>
          <div class="ted-content">
            <div class="ted-title">סיכונים בשוק ההון - פרשת סלייס</div>
            <div class="ted-speaker">עו"ד ליאב וינבאום, מנהל המחלקה המסחרית בפרקליטות מחוז מרכז</div>
          </div>
        </div>
        <div class="ted-item">
          <div class="ted-num">3</div>
          <div class="ted-content">
            <div class="ted-title">מערכת דירוג אשראי - מהו דירוג אשראי, חשיבותו והשלכותיו על הפעילות הפיננסית</div>
            <div class="ted-speaker">עו"ד שחר דויזון</div>
          </div>
        </div>
        <div class="ted-item">
          <div class="ted-num">4</div>
          <div class="ted-content">
            <div class="ted-title">חינוך פיננסי</div>
            <div class="ted-speaker">ליאל קייזר</div>
          </div>
        </div>
      </div>
    </div>

    <div class="card card-3">
      <div class="card-accent"></div>
      <div class="card-number">03</div>
      <div class="card-tag">📄 פליירים וידע</div>
      <h2>חומרי מידע להפצה</h2>
      <div class="card-divider"></div>
      <p class="lead">במהלך הכנס יחולקו פליירים ממוקדים לשני תחומים מרכזיים – מיצוי זכויות מעשי וידע כללי בבנקאות.</p>
      <div class="flyers-grid">
        <div class="flyer-item">
          <div class="flyer-icon">✅</div>
          <h4>10 זכויות שכל לקוח בנק חייב להכיר</h4>
          <p>מדריך פרקטי לזיהוי ומיצוי זכויות מעמדת הלקוח</p>
        </div>
        <div class="flyer-item">
          <div class="flyer-icon">💰</div>
          <h4>הטבות בנקאיות לאוכלוסיות מיוחדות</h4>
          <p>ותיקים, סטודנטים, בעלי מוגבלויות, עולים חדשים – מה מגיע לכם</p>
        </div>
        <div class="flyer-item">
          <div class="flyer-icon">🏦</div>
          <h4>מדריך להגשת תלונה על הבנק</h4>
          <p>נציב תלונות של הבנקים | המפקח על הבנקים וגורמים חיצוניים</p>
        </div>
        <div class="flyer-item">
          <div class="flyer-icon">📊</div>
          <h4>ידע כללי: מושגי יסוד בבנקאות</h4>
          <p>ריביות, פיקדונות, קרן כספית, מסגרת אשראי – הגדרות בשפה פשוטה</p>
        </div>
        <div class="flyer-item flyer-full">
          <div class="flyer-icon">🔄</div>
          <h4>כיצד לעבור בנק ולשמור על ההיסטוריה הפיננסית שלכם</h4>
          <p>מדריך שלב אחר שלב לניוד חשבון בנק לפי חוק ניוד פיקדונות</p>
        </div>
      </div>
    </div>

    <div class="card card-4">
      <div class="card-accent"></div>
      <div class="card-number">04</div>
      <div class="card-tag">⚖️ סיוע משפטי</div>
      <h2>ייעוץ וסיוע משפטי</h2>
      <div class="card-divider"></div>
      <p class="lead">היכרות עם הקליניקה ופועלה | חשיבותו של הסיוע המשפטי לאוכלוסיות מוחלשות</p>
      <div class="legal-features">
        <div class="legal-item">
          <div class="legal-dot"></div>
          <div>
            <h4>מתן סיוע משפטי מול התאגידים הבנקאיים</h4>
            <p>הזמינו תור מראש לפגישה אישית עם עורך דין מומחה בתחום הבנקאות</p>
          </div>
        </div>
        <div class="legal-item">
          <div class="legal-dot"></div>
          <div>
            <h4>ליווי משפטי מקיף</h4>
            <p>הכוונה, ייעוץ וליווי</p>
          </div>
        </div>
        <div class="legal-item">
          <div class="legal-dot"></div>
          <div>
            <h4>הקליניקה פועלת בשיתוף פעולה עם קליניקות נוספות בתחום המשפט</h4>
            <p>במידת הצורך, הקליניקה עובדת במקביל עם הקליניקות – הוצאה לפועל, חדלות פירעון ודיני משפחה</p>
          </div>
        </div>
        <div class="legal-item">
          <div class="legal-dot"></div>
          <div>
            <h4>על חשיבות שיתוף הפעולה הקליני</h4>
            <p>בית דין משלב, בתי משפט קהילתיים, קליניקות נוספות</p>
          </div>
        </div>
      </div>
      <div class="cta-box">
        <p>טופס פנייה לקבלת ייעוץ</p>
        <a href="#" class="cta-btn">הרשמה לייעוץ</a>
      </div>
    </div>

  </div>

  <footer>
    <div class="footer-org">המסלול האקדמי, המכללה למינהל · מרכז משנה</div>
    <p>כניסה חופשית לכנס · הרשמה מראש נדרשת</p>
    <a href="#" class="register-btn">הרשמה לכנס</a>
    <br><br>
    <p style="font-size:0.72rem; color: #5a5548;">לפרטים נוספים: <a href="/cdn-cgi/l/email-protection" class="__cf_email__" d
