<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Algebra • Solving Quadratic Equations, Part I: 20-Problem Mastery Suite</title>

  <!-- MathJax Configuration & Loader -->
  <script>
    window.MathJax = {
      tex: {
        inlineMath: [['\\(', '\\)'], ['$', '$']],
        displayMath: [['\\[', '\\]'], ['$$', '$$']],
        processEscapes: true
      },
      svg: { fontCache: 'global' }
    };
  </script>
  <script type="text/javascript" id="MathJax-script" async
    src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>

  <style>
    :root {
      --navy-dark: #0f172a;
      --brand-blue: #2563eb;
      --accent-cyan: #0284c7;
      --bg-tint: #f8fafc;
      --card-surf: #ffffff;
      --border-accent: #93c5fd;
      --border-soft: #cbd5e1;
      --green-ok: #059669;
      --green-surf: #d1fae5;
      --red-fail: #dc2626;
      --red-surf: #fee2e2;
      --brand-gold: #f59e0b;
      --gold-dark: #d97706;
      --gold-surf: #fef3c7;
      --text-main: #0f172a;
      --text-muted: #475569;

      /* High-Contrast Clear Light Yellow Options Palette */
      --opt-yellow-bg: #fefce8;
      --opt-yellow-border: #fef08a;
      --opt-yellow-hover: #fef9c3;
      --opt-yellow-active: #fde047;
      --opt-yellow-text: #713f12;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
    }

    body {
      background-color: var(--bg-tint);
      color: var(--text-main);
      display: flex;
      flex-direction: column;
      min-height: 100vh;
    }

    header {
      background: var(--navy-dark);
      color: #fff;
      padding: 14px 24px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 4px 12px rgba(15, 23, 42, 0.2);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .brand-wrap {
      display: flex;
      align-items: center;
      gap: 14px;
    }

    .logo-badge {
      width: 44px;
      height: 44px;
      background: #ffffff;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.25);
    }

    .brand-title h1 {
      font-size: 1.15rem;
      font-weight: 700;
      letter-spacing: 0.5px;
    }

    .brand-title p {
      font-size: 0.78rem;
      color: #38bdf8;
      font-weight: 500;
    }

    .header-controls {
      display: flex;
      align-items: center;
      gap: 12px;
    }

    .chip {
      background: rgba(255, 255, 255, 0.12);
      border: 1px solid rgba(255, 255, 255, 0.25);
      padding: 6px 14px;
      border-radius: 20px;
      font-size: 0.88rem;
      color: #ffffff;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .chip strong {
      color: #ffffff;
      font-weight: 800;
      letter-spacing: 0.3px;
    }

    .btn-icon {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.3);
      color: #fff;
      border-radius: 50%;
      width: 36px;
      height: 36px;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
    }

    nav {
      background: #ffffff;
      border-bottom: 1px solid var(--border-soft);
      display: flex;
      justify-content: center;
      gap: 8px;
      padding: 8px 16px;
      flex-wrap: wrap;
    }

    nav button {
      background: none;
      border: none;
      outline: none;
      padding: 10px 20px;
      font-size: 0.92rem;
      font-weight: 600;
      color: var(--text-muted);
      cursor: pointer;
      border-radius: 8px;
      transition: all 0.2s;
    }

    nav button.active {
      background: #eff6ff;
      color: var(--brand-blue);
      border-bottom: 3px solid var(--brand-blue);
    }

    main {
      flex: 1;
      padding: 24px;
      max-width: 1400px;
      margin: 0 auto;
      width: 100%;
    }

    .view {
      display: none;
    }

    .view.active {
      display: block;
    }

    #loginGateView {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(15, 23, 42, 0.94);
      backdrop-filter: blur(6px);
      z-index: 1000;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .login-box {
      background: #fff;
      padding: 36px;
      border-radius: 16px;
      width: 100%;
      max-width: 480px;
      text-align: center;
      box-shadow: 0 14px 35px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      font-size: 1.45rem;
      color: var(--navy-dark);
      margin-bottom: 6px;
    }

    .login-box p {
      font-size: 0.88rem;
      color: var(--text-muted);
      margin-bottom: 20px;
      line-height: 1.5;
    }

    .resume-alert {
      display: none;
      background: #eff6ff;
      border: 1px solid var(--border-accent);
      border-radius: 8px;
      padding: 10px 14px;
      margin-bottom: 16px;
      font-size: 0.86rem;
      color: var(--navy-dark);
      text-align: left;
    }

    .login-box input {
      width: 100%;
      padding: 12px 16px;
      border: 1px solid var(--border-soft);
      border-radius: 8px;
      font-size: 1rem;
      margin-bottom: 16px;
      outline: none;
    }

    .btn-primary {
      background: var(--brand-blue);
      color: #fff;
      border: none;
      padding: 12px 24px;
      font-size: 1rem;
      font-weight: 600;
      border-radius: 8px;
      cursor: pointer;
      width: 100%;
      transition: background 0.2s;
    }

    .btn-primary:hover {
      background: #1d4ed8;
    }

    .btn-secondary {
      background: transparent;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 9px 18px;
      font-size: 0.88rem;
      font-weight: 600;
      border-radius: 6px;
      cursor: pointer;
      width: 100%;
      margin-top: 10px;
    }

    .btn-secondary:hover {
      background: var(--bg-tint);
    }

    .sheet-grid {
      display: grid;
      grid-template-columns: 1fr 340px;
      gap: 24px;
    }

    @media (max-width: 990px) {
      .sheet-grid {
        grid-template-columns: 1fr;
      }
    }

    .topic-integrated-banner {
      background: #ffffff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 22px;
      margin-bottom: 22px;
      box-shadow: 0 2px 8px rgba(15, 23, 42, 0.04);
    }

    .topic-integrated-banner h3 {
      color: var(--navy-dark);
      font-size: 1.25rem;
      display: flex;
      align-items: center;
      gap: 8px;
      margin-bottom: 8px;
    }

    .paul-notes-container {
      background: #f0fdf4;
      border: 1px solid #bbf7d0;
      border-radius: 10px;
      padding: 16px 18px;
      margin: 14px 0;
    }

    .paul-notes-container h4 {
      color: #166534;
      font-size: 0.98rem;
      display: flex;
      align-items: center;
      gap: 6px;
      margin-bottom: 8px;
    }

    .paul-notes-body {
      font-size: 0.9rem;
      line-height: 1.65;
      color: #14532d;
    }

    .paul-notes-body ul {
      margin-left: 20px;
      margin-top: 6px;
      margin-bottom: 6px;
    }

    .formula-box {
      background: #f8fafc;
      border-left: 4px solid var(--brand-blue);
      border-radius: 0 6px 6px 0;
      padding: 10px 14px;
      margin: 12px 0;
    }

    .question-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 26px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.03);
    }

    .concept-tag {
      display: inline-block;
      padding: 4px 10px;
      border-radius: 14px;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      margin-bottom: 8px;
      background: #e0f2fe;
      color: #0369a1;
      border: 1px solid #7dd3fc;
    }

    .hint-container {
      margin: 14px 0;
    }

    .btn-hint-toggle {
      background: #fffbeb;
      border: 1px solid #fde68a;
      color: #b45309;
      font-size: 0.86rem;
      font-weight: 600;
      padding: 7px 14px;
      border-radius: 6px;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s ease;
    }

    .btn-hint-toggle:hover {
      background: #fef3c7;
      border-color: #f59e0b;
    }

    .hint-box {
      display: none;
      background: #fffbeb;
      border-left: 4px solid #f59e0b;
      border-radius: 0 8px 8px 0;
      padding: 12px 16px;
      margin-top: 8px;
      font-size: 0.9rem;
      color: #92400e;
      line-height: 1.6;
    }

    /* Step Box Structure - Sequential Strict Reveal */
    .step-unit {
      margin-top: 18px;
      padding: 18px;
      background: #f8fafc;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      animation: fadeIn 0.3s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(6px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .step-unit.completed {
      border-color: #86efac;
      background: #f0fdf4;
    }

    .step-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 10px;
    }

    .step-title {
      font-size: 0.98rem;
      font-weight: 700;
      color: var(--navy-dark);
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .step-badge {
      font-size: 0.75rem;
      font-weight: 700;
      padding: 2px 8px;
      border-radius: 10px;
      background: #e2e8f0;
      color: #475569;
    }

    .step-badge.resolved {
      background: #dcfce7;
      color: #166534;
    }

    .mcq-container {
      display: grid;
      grid-template-columns: 1fr;
      gap: 10px;
      margin: 12px 0;
    }

    /* Light Yellow Clear Options */
    .mcq-option-btn {
      background: var(--opt-yellow-bg);
      border: 2px solid var(--opt-yellow-border);
      border-radius: 10px;
      padding: 12px 16px;
      text-align: left;
      font-size: 0.95rem;
      color: var(--opt-yellow-text);
      cursor: pointer;
      transition: all 0.15s ease;
      display: flex;
      align-items: center;
      gap: 12px;
      box-shadow: 0 2px 4px rgba(254, 240, 138, 0.25);
    }

    .mcq-option-btn:hover:not(:disabled) {
      background: var(--opt-yellow-hover);
      border-color: var(--opt-yellow-active);
      transform: translateY(-1px);
    }

    .mcq-option-btn.selected-correct {
      background: var(--green-surf) !important;
      border-color: var(--green-ok) !important;
      color: var(--green-ok) !important;
      font-weight: 700;
      box-shadow: none;
    }

    .mcq-option-btn.selected-wrong {
      background: var(--red-surf) !important;
      border-color: var(--red-fail) !important;
      color: var(--red-fail) !important;
      box-shadow: none;
    }

    .opt-letter {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #ffffff;
      border: 2px solid var(--opt-yellow-active);
      font-weight: 800;
      color: var(--opt-yellow-text);
      flex-shrink: 0;
    }

    .attempts-badge {
      font-size: 0.8rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 12px;
      background: #f1f5f9;
      color: #64748b;
      margin-left: 6px;
    }

    .step-feedback-box {
      margin-top: 12px;
      padding: 12px 14px;
      border-radius: 8px;
      font-size: 0.9rem;
      line-height: 1.6;
      display: block;
      animation: fadeIn 0.25s ease-in;
    }

    .step-feedback-box.correct {
      background: #ecfdf5;
      border-left: 4px solid var(--green-ok);
      color: #065f46;
    }

    .step-feedback-box.incorrect {
      background: #fef2f2;
      border-left: 4px solid var(--red-fail);
      color: #991b1b;
    }

    .btn-reveal-step {
      background: var(--brand-gold);
      color: #fff;
      border: none;
      padding: 6px 12px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.82rem;
      cursor: pointer;
      margin-top: 8px;
    }

    .btn-reveal-step:hover {
      background: var(--gold-dark);
    }

    .svg-container {
      display: flex;
      justify-content: center;
      margin: 16px 0;
      padding: 16px;
      background: var(--bg-tint);
      border-radius: 8px;
      border: 1px solid var(--border-soft);
      overflow-x: auto;
    }

    .nav-toolbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 26px;
      padding-top: 18px;
      border-top: 1px solid var(--border-soft);
    }

    .nav-btn-group {
      display: flex;
      gap: 10px;
    }

    .btn-nav-action {
      background: #f8fafc;
      border: 1px solid var(--border-accent);
      color: var(--navy-dark);
      padding: 8px 18px;
      border-radius: 6px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 6px;
      transition: all 0.15s;
    }

    .btn-nav-action:hover:not(:disabled) {
      background: var(--bg-tint);
      border-color: var(--brand-blue);
    }

    .btn-nav-action:disabled {
      opacity: 0.45;
      cursor: not-allowed;
    }

    .btn-skip {
      border-color: var(--brand-gold);
      color: var(--gold-dark);
      background: var(--gold-surf);
    }

    .btn-skip:hover {
      background: #fde68a;
    }

    .palette-box {
      background: #fff;
      border: 1px solid var(--border-soft);
      border-radius: 12px;
      padding: 16px;
      margin-bottom: 20px;
    }

    .palette-filters {
      display: flex;
      gap: 6px;
      margin-bottom: 12px;
    }

    .btn-filter {
      flex: 1;
      padding: 6px 4px;
      font-size: 0.78rem;
      font-weight: 700;
      border: 1px solid var(--border-soft);
      background: #f8fafc;
      border-radius: 6px;
      cursor: pointer;
      color: var(--text-muted);
    }

    .btn-filter.active {
      background: var(--brand-blue);
      color: #fff;
      border-color: var(--brand-blue);
    }

    .palette-legend {
      display: flex;
      justify-content: space-between;
      font-size: 0.72rem;
      margin: 8px 0 12px 0;
      padding: 6px 8px;
      background: var(--bg-tint);
      border-radius: 6px;
    }

    .legend-item {
      display: flex;
      align-items: center;
      gap: 4px;
      font-weight: 600;
    }

    .legend-dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
    }

    .palette-grid {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 6px;
      margin-bottom: 12px;
      max-height: 380px;
      overflow-y: auto;
      padding-right: 4px;
    }

    .palette-btn {
      aspect-ratio: 1;
      border: 1px solid var(--border-soft);
      background: var(--bg-tint);
      border-radius: 6px;
      font-weight: 700;
      cursor: pointer;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      transition: all 0.15s;
      font-size: 0.82rem;
      color: var(--navy-dark);
    }

    .palette-btn.active {
      border: 2px solid var(--navy-dark) !important;
      background: #bfdbfe;
      color: #1e3a8a;
    }

    .palette-btn.completed {
      background: var(--green-ok) !important;
      color: #fff !important;
      border-color: var(--green-ok) !important;
    }

    .palette-btn.partial {
      background: var(--brand-gold) !important;
      color: #fff !important;
      border-color: var(--gold-dark) !important;
    }

    .theory-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 24px;
      margin-bottom: 24px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.02);
    }

    .theory-card h3 {
      color: var(--navy-dark);
      margin-bottom: 14px;
      display: flex;
      align-items: center;
      gap: 8px;
      font-size: 1.25rem;
    }

    .compendium-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 20px;
      margin: 16px 0;
    }

    .comp-card {
      background: #ffffff;
      border: 1px solid var(--border-soft);
      border-radius: 10px;
      padding: 18px;
      display: flex;
      flex-direction: column;
      box-shadow: 0 2px 6px rgba(15, 23, 42, 0.04);
    }

    .comp-card h4 {
      color: var(--navy-dark);
      border-bottom: 2px solid var(--border-soft);
      padding-bottom: 8px;
      margin-bottom: 12px;
      font-size: 1.05rem;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .recap-body {
      font-size: 0.92rem;
      line-height: 1.65;
      color: var(--text-main);
    }

    .hero-score-card {
      background: #fff;
      border-radius: 12px;
      border: 1px solid var(--border-soft);
      padding: 28px;
      text-align: center;
      margin-bottom: 24px;
      box-shadow: 0 4px 14px rgba(0,0,0,0.03);
    }

    .student-badge {
      display: inline-block;
      background: var(--bg-tint);
      border: 1px solid var(--border-accent);
      padding: 6px 18px;
      border-radius: 20px;
      font-size: 1rem;
      margin-bottom: 14px;
      color: var(--navy-dark);
    }

    .student-badge strong {
      color: var(--brand-blue);
    }

    .score-badge {
      font-size: 3rem;
      font-weight: 800;
      color: var(--brand-blue);
      margin: 8px 0;
    }

    .progress-bar-wrap {
      width: 100%;
      height: 12px;
      background: #e2e8f0;
      border-radius: 6px;
      overflow: hidden;
      margin: 16px 0;
    }

    .progress-bar-fill {
      height: 100%;
      background: var(--green-ok);
      width: 0%;
      transition: width 0.3s ease;
    }

    .toast {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: var(--navy-dark);
      color: #fff;
      padding: 12px 20px;
      border-radius: 8px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.2);
      display: none;
      z-index: 1000;
    }

    @media print {
      header, nav, .palette-box, .btn-primary, #loginGateView, .nav-toolbar, .btn-hint-toggle {
        display: none !important;
      }
      body { background: #fff; }
      main { width: 100%; max-width: 100%; padding: 0; }
      .sheet-grid { display: block; }
      .view { display: block !important; }
    }
  </style>
</head>
<body>

  <header>
    <div class="brand-wrap">
      <div class="logo-badge">
        <svg width="34" height="34" viewBox="0 0 100 100" fill="none">
          <circle cx="50" cy="50" r="44" stroke="#2563eb" stroke-width="7"/>
          <path d="M 28 65 Q 50 15 72 65" stroke="#0284c7" stroke-width="6" fill="none"/>
          <circle cx="50" cy="40" r="5" fill="#f59e0b"/>
        </svg>
      </div>
      <div class="brand-title">
        <h1>Algebra • Solving Quadratic Equations, Part I</h1>
        <p>Factoring, Zero Factor Property &amp; Square Root Property • Lamar University Complete 20-Problem Suite</p>
      </div>
    </div>
    <div class="header-controls">
      <div class="chip" id="timerChip">⏱️ 00:00</div>
      <div class="chip" id="userPill"><strong>Student: Guest</strong></div>
      <button class="btn-icon" id="audioToggleBtn" title="Toggle Audio">🔊</button>
    </div>
  </header>

  <nav>
    <button class="tab-btn active" id="tabPracticeBtn" onclick="switchMainTab('practice')">
      🎯 Interactive Practice Workstation (20 Problems)
    </button>
    <button class="tab-btn" id="tabTheoryBtn" onclick="switchMainTab('theory')">
      📖 Quadratic Equations Compendium &amp; Methods
    </button>
    <button class="tab-btn" id="tabScorecardBtn" onclick="switchMainTab('scorecard')">
      📊 Master Scorecard &amp; Solutions
    </button>
  </nav>

  <!-- Login Modal with Session Persistence -->
  <div id="loginGateView">
    <div class="login-box">
      <h2>Quadratic Equations Practice Portal</h2>
      <p>Algebra • Zero Factor Property, Factoring Trinomials &amp; The Square Root Property</p>
      
      <div id="resumeAlertBox" class="resume-alert">
        <strong>Saved Session Found!</strong><br>
        <span id="savedSessionDetails"></span>
      </div>

      <input type="text" id="studentNameInput" placeholder="Enter Student Name" />
      <button class="btn-primary" id="startSessionBtn" onclick="initDirectLogin(false)">Start Learning Session</button>
      <button class="btn-secondary" id="resumeSessionBtn" style="display:none;" onclick="initDirectLogin(true)">Resume Saved Session</button>
    </div>
  </div>

  <main>
    <!-- View 1: Unified Interactive Learning Stream -->
    <div id="viewPractice" class="view active">
      <div class="sheet-grid">
        <div>
          <!-- Unified Header Card: Synchronized Notes directly above active problem -->
          <div class="topic-integrated-banner" id="topicBannerContainer"></div>

          <!-- Question Workstation Card -->
          <div class="question-card" id="activeQuestionCard"></div>
        </div>

        <aside>
          <div class="palette-box">
            <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px;">
              <h4 id="paletteHeaderTitle">All 20 Problems</h4>
              <span style="font-size:0.8rem; color:var(--text-muted);" id="paletteCount">0 / 20 Solved</span>
            </div>

            <div class="palette-filters">
              <button class="btn-filter active" id="filterAllBtn" onclick="filterPalette('all')">All (20)</button>
              <button class="btn-filter" id="filterP1Btn" onclick="filterPalette('p1')">Practice (8)</button>
              <button class="btn-filter" id="filterP2Btn" onclick="filterPalette('p2')">Assignment (12)</button>
            </div>

            <div class="palette-legend">
              <div class="legend-item"><span class="legend-dot" style="background:var(--green-ok);"></span> Completed</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f59e0b;"></span> In Progress</div>
              <div class="legend-item"><span class="legend-dot" style="background:#bfdbfe;"></span> Active</div>
              <div class="legend-item"><span class="legend-dot" style="background:#f0f9ff; border:1px solid #bae6fd;"></span> Unseen</div>
            </div>
            
            <div class="palette-grid" id="paletteGrid"></div>
            
            <button class="btn-primary" style="margin-top: 10px; background: var(--navy-dark);" onclick="switchMainTab('scorecard')">
              📊 View Evaluation Scorecard
            </button>
            <button class="btn-secondary" style="margin-top: 8px; border-color: #cbd5e1;" onclick="resetStudentProgress()">
              🔄 Reset All Progress
            </button>
          </div>

          <div class="palette-box" style="background: #f8fafc;">
            <h4 style="font-size: 0.92rem; margin-bottom: 8px; color: var(--navy-dark);">Strict Step-Gating Rules</h4>
            <p style="font-size: 0.82rem; line-height: 1.6; color: var(--text-muted);">
              • <strong>Sequential Lock:</strong> Step 2 remains completely hidden until Step 1 is verified.<br/>
              • <strong>Balanced Options:</strong> Correct answer letters are evenly distributed across (A), (B), (C), and (D).<br/>
              • <strong>Embedded Paul's Notes:</strong> Direct reference notes and algebraic warnings update above each problem.<br/>
              • Click <strong>💡 Need a Hint?</strong> to reveal tailored algebraic hints.<br/>
              • You get <strong>2 attempts</strong> per step. If unresolved after 2 attempts, the <strong>Reveal Step Solution</strong> button unlocks.
            </p>
          </div>
        </aside>
      </div>
    </div>

    <!-- View 2: Compendium Guide -->
    <div id="viewTheory" class="view">
      <div class="theory-card">
        <h3>📐 Paul's Online Notes: Solving Quadratic Equations, Part I Compendium</h3>
        <p class="theory-intro-text">
          A quadratic equation is any equation that can be written in the standard form \(ax^2 + bx + c = 0\) where \(a \ne 0\). This guide details the two fundamental solving methods: Factoring and the Square Root Property.
        </p>

        <div class="compendium-grid">
          <div class="comp-card">
            <h4>1. The Zero Factor Property</h4>
            <div class="recap-body">
              <p>If the product of two expressions is zero, at least one of them must be zero:</p>
              <div class="formula-box">
                \[AB = 0 \iff A = 0 \quad \text{or} \quad B = 0\]
                <p><strong>CRITICAL WARNING:</strong> This property is valid <em>only</em> when one side equals zero! If \(AB = 12\), you cannot claim \(A = 3\) or \(B = 4\). You must expand and move all terms to one side so the other side is zero!</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>2. Common Factoring Pitfall: Dividing by the Variable</h4>
            <div class="recap-body">
              <p>Consider equations like \(4x^2 = 12x\):</p>
              <div class="formula-box">
                <p><strong>NEVER divide by the variable \(x\)!</strong> Dividing by \(x\) loses the solution \(x = 0\) and introduces potential division by zero. Always subtract \(12x\) to the left side and factor out the greatest common factor: \(4x(x - 3) = 0\).</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>3. The Square Root Property</h4>
            <div class="recap-body">
              <p>When an equation consists of a perfect square equal to a constant:</p>
              <div class="formula-box">
                \[u^2 = p \implies u = \pm \sqrt{p}\]
                \[(ax + b)^2 = p \implies ax + b = \pm \sqrt{p} \implies x = \frac{-b \pm \sqrt{p}}{a}\]
                <p>Do not forget the \(\pm\) sign! Every non-zero number has two square roots.</p>
              </div>
            </div>
          </div>

          <div class="comp-card">
            <h4>4. Complex Solutions with Square Root Property</h4>
            <div class="recap-body">
              <p>When the constant \(p\) is negative (\(p < 0\)):</p>
              <div class="formula-box">
                \[\sqrt{-k} = i\sqrt{k} \quad (k > 0, \, i^2 = -1)\]
                <p>Example: \((x - 4)^2 = -16 \implies x - 4 = \pm \sqrt{-16} = \pm 4i \implies x = 4 \pm 4i\).</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- View 3: Complete Scorecard & Master Solutions -->
    <div id="viewScorecard" class="view">
      <div class="hero-score-card">
        <h2>Quadratic Equations Part I Diagnostic Scorecard</h2>
        <div class="student-badge" id="reportStudentBadge"><strong>Student: Guest</strong></div>
        <div class="score-badge" id="scoreValue">0 / 20</div>
        <div class="progress-bar-wrap">
          <div class="progress-bar-fill" id="progressBarFill"></div>
        </div>
        <p id="scoreSubtitle" style="font-size:1.02rem; font-weight:600; color:var(--navy-dark); margin-top:8px;">
          Review all 20 problem solutions, step evaluations, and derivations below.
        </p>
        <button class="btn-primary" style="margin-top: 14px; max-width: 240px;" onclick="window.print()">🖨️ Print Final Scorecard</button>
      </div>

      <div id="completeSolutionsContainer"></div>
    </div>
  </main>

  <div class="toast" id="toastMessage"></div>

  <script>
    /* ==========================================================================
       COMPLETE 20-PROBLEM DATASET (8 PRACTICE + 12 ASSIGNMENT)
       Options and correctIndex are balanced across A (0), B (1), C (2), and D (3).
       Strict step gating: Step 2 remains hidden until Step 1 is verified.
       ========================================================================== */
    const PROBLEMS_DATA = [
      // ---------- PART 1: PRACTICE PROBLEMS (1 TO 8) ----------
      {
        id: 1,
        set: "p1",
        setName: "Practice Problems",
        title: "Solving Monic Quadratic by Factoring",
        prompt: "Solve the quadratic equation by factoring: \\[x^2 - 5x - 24 = 0\\]",
        hint: "Find two numbers that multiply to -24 and add to -5. The factors are -8 and 3.",
        svg: `<svg width="100%" height="180" viewBox="0 0 360 160" style="max-width:360px;">
          <rect width="360" height="160" fill="#ffffff" stroke="#cbd5e1" stroke-width="1.5" rx="6"/>
          <line x1="20" y1="90" x2="340" y2="90" stroke="#64748b" stroke-width="1.5"/>
          <line x1="120" y1="15" x2="120" y2="145" stroke="#64748b" stroke-width="1.5"/>
          <!-- Parabola x^2 - 5x - 24 crossing at x = -3 and x = 8 -->
          <path d="M 60,30 Q 185,170 310,30" fill="none" stroke="#0284c7" stroke-width="2.5"/>
          <circle cx="85" cy="90" r="4.5" fill="#059669"/>
          <text x="70" y="108" font-size="10" font-weight="bold" fill="#059669">x = −3</text>
          <circle cx="285" cy="90" r="4.5" fill="#059669"/>
          <text x="275" y="108" font-size="10" font-weight="bold" fill="#059669">x = 8</text>
        </svg>`,
        steps: [
          {
            title: "Step 1: Factor the Trinomial",
            prompt: "What is the correct factorization of \\(x^2 - 5x - 24\\)?",
            options: [
              { label: "A", text: "(x - 6)(x + 4)" },
              { label: "B", text: "(x - 12)(x + 2)" },
              { label: "C", text: "(x - 8)(x + 3)" },
              { label: "D", text: "(x + 8)(x - 3)" }
            ],
            correctIndex: 2, // C
            explanation: "Since \\((-8)(3) = -24\\) and \\(-8 + 3 = -5\\), the trinomial factors as \\((x - 8)(x + 3) = 0\\)."
          },
          {
            title: "Step 2: Apply Zero Factor Property & Solve",
            prompt: "Set each factor to zero and solve for \\(x\\).",
            options: [
              { label: "A", text: "x = 8 \\quad \\text{and} \\quad x = -3" },
              { label: "B", text: "x = -8 \\quad \\text{and} \\quad x = 3" },
              { label: "C", text: "x = 6 \\quad \\text{and} \\quad x = -4" },
              { label: "D", text: "x = 24 \\quad \\text{and} \\quad x = -1" }
            ],
            correctIndex: 0, // A
            explanation: "\\(x - 8 = 0 \\implies x = 8\\); \\(x + 3 = 0 \\implies x = -3\\)."
          }
        ]
      },
      {
        id: 2,
        set: "p1",
        setName: "Practice Problems",
        title: "Solving Non-Monic Quadratic by Factoring",
        prompt: "Solve the quadratic equation by factoring: \\[3z^2 + 14z - 5 = 0\\]",
        hint: "We need factors of \\(3(-5) = -15\\) that sum to 14. These are 15 and -1.",
        svg: null,
        steps: [
          {
            title: "Step 1: Factor the Trinomial",
            prompt: "What is the factored form of \\(3z^2 + 14z - 5\\)?",
            options: [
              { label: "A", text: "(3z + 5)(z - 1)" },
              { label: "B", text: "(3z - 1)(z + 5)" },
              { label: "C", text: "(3z + 1)(z - 5)" },
              { label: "D", text: "(z - 1)(3z + 15)" }
            ],
            correctIndex: 1, // B
            explanation: "Grouping: \\(3z^2 + 15z - z - 5 = 3z(z + 5) - 1(z + 5) = (3z - 1)(z + 5) = 0\\)."
          },
          {
            title: "Step 2: Solve for z",
            prompt: "Apply the Zero Factor Property to solve for \\(z\\).",
            options: [
              { label: "A", text: "z = -1/3 \\quad \\text{and} \\quad z = 5" },
              { label: "B", text: "z = 3 \\quad \\text{and} \\quad z = -5" },
              { label: "C", text: "z = 1 \\quad \\text{and} \\quad z = -5" },
              { label: "D", text: "z = 1/3 \\quad \\text{and} \\quad z = -5" }
            ],
            correctIndex: 3, // D
            explanation: "\\(3z - 1 = 0 \\implies z = 1/3\\); \\(z + 5 = 0 \\implies z = -5\\)."
          }
        ]
      },
      {
        id: 3,
        set: "p1",
        setName: "Practice Problems",
        title: "Quadratic with GCF (Avoiding Variable Division)",
        prompt: "Solve the equation: \\[4y^2 = 12y\\]",
        hint: "Do NOT divide both sides by \\(y\\)! Move \\(12y\\) to the left side and factor out the greatest common factor \\(4y\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Move Terms to One Side and Factor",
            prompt: "What is the correct factored form with 0 on the right side?",
            options: [
              { label: "A", text: "4y(y - 12) = 0" },
              { label: "B", text: "y(4y - 3) = 0" },
              { label: "C", text: "(2y - 3)(2y + 3) = 0" },
              { label: "D", text: "4y(y - 3) = 0" }
            ],
            correctIndex: 3, // D
            explanation: "\\(4y^2 - 12y = 0 \\implies 4y(y - 3) = 0\\)."
          },
          {
            title: "Step 2: Solve for y",
            prompt: "What are the solutions to \\(4y(y - 3) = 0\\)?",
            options: [
              { label: "A", text: "y = 0 \\quad \\text{and} \\quad y = 3" },
              { label: "B", text: "y = 3 \\text{ only}" },
              { label: "C", text: "y = 0 \\quad \\text{and} \\quad y = 12" },
              { label: "D", text: "y = 4 \\quad \\text{and} \\quad y = 3" }
            ],
            correctIndex: 0, // A
            explanation: "\\(4y = 0 \\implies y = 0\\); \\(y - 3 = 0 \\implies y = 3\\). Dividing by \\(y\\) would have lost the solution \\(y = 0\\)!"
          }
        ]
      },
      {
        id: 4,
        set: "p1",
        setName: "Practice Problems",
        title: "Non-Zero Right Hand Side Quadratic",
        prompt: "Solve the equation: \\[(x - 1)(x + 4) = 14\\]",
        hint: "You cannot set factors equal to 14! Expand the left side: \\(x^2 + 3x - 4 = 14\\), subtract 14 to get zero on the right side, then factor.",
        svg: null,
        steps: [
          {
            title: "Step 1: Expand and Write in Standard Form",
            prompt: "What is the equation in standard form \\(ax^2 + bx + c = 0\\)?",
            options: [
              { label: "A", text: "x^2 + 3x - 18 = 0" },
              { label: "B", text: "x^2 + 3x + 10 = 0" },
              { label: "C", text: "x^2 - 4x - 14 = 0" },
              { label: "D", text: "x^2 + 3x - 4 = 0" }
            ],
            correctIndex: 0, // A
            explanation: "\\((x - 1)(x + 4) = x^2 + 3x - 4\\). Subtracting 14 yields \\(x^2 + 3x - 18 = 0\\)."
          },
          {
            title: "Step 2: Factor and Solve",
            prompt: "Factor \\(x^2 + 3x - 18 = 0\\) and solve for \\(x\\).",
            options: [
              { label: "A", text: "(x - 9)(x + 2) = 0 \\implies x = 9, -2" },
              { label: "B", text: "(x - 6)(x + 3) = 0 \\implies x = 6, -3" },
              { label: "C", text: "(x + 6)(x - 3) = 0 \\implies x = -6, 3" },
              { label: "D", text: "(x + 18)(x - 1) = 0 \\implies x = -18, 1" }
            ],
            correctIndex: 2, // C
            explanation: "\\((x + 6)(x - 3) = 0 \\implies x = -6\\) or \\(x = 3\\)."
          }
        ]
      },
      {
        id: 5,
        set: "p1",
        setName: "Practice Problems",
        title: "Square Root Property with Radical Simplification",
        prompt: "Solve the equation using the square root property: \\[t^2 = 45\\]",
        hint: "Apply \\(t = \\pm \\sqrt{45}\\). Remember to simplify \\(\\sqrt{45} = \\sqrt{9 \\cdot 5} = 3\\sqrt{5}\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply the Square Root Property",
            prompt: "Which statement correctly applies the square root property?",
            options: [
              { label: "A", text: "t = \\sqrt{45}" },
              { label: "B", text: "t = \\pm \\sqrt{45}" },
              { label: "C", text: "t = 45^2" },
              { label: "D", text: "t = \\pm 45" }
            ],
            correctIndex: 1, // B
            explanation: "By the square root property, \\(t^2 = p \\implies t = \\pm \\sqrt{p}\\), so \\(t = \\pm \\sqrt{45}\\)."
          },
          {
            title: "Step 2: Simplify the Radical",
            prompt: "What is the fully simplified exact solution?",
            options: [
              { label: "A", text: "t = 3\\sqrt{5}" },
              { label: "B", text: "t = \\pm 9\\sqrt{5}" },
              { label: "C", text: "t = \\pm 5\\sqrt{3}" },
              { label: "D", text: "t = \\pm 3\\sqrt{5}" }
            ],
            correctIndex: 3, // D
            explanation: "\\(\\sqrt{45} = \\sqrt{9 \\cdot 5} = 3\\sqrt{5}\\), giving \\(t = \\pm 3\\sqrt{5}\\)."
          }
        ]
      },
      {
        id: 6,
        set: "p1",
        setName: "Practice Problems",
        title: "Square Root Property with Binomial Square",
        prompt: "Solve the equation using the square root property: \\[(2x - 3)^2 = 25\\]",
        hint: "Take the square root of both sides to get \\(2x - 3 = \\pm 5\\). Then solve the two resulting linear equations.",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply Square Root Property",
            prompt: "What equation results from taking the square root of both sides?",
            options: [
              { label: "A", text: "2x - 3 = 5" },
              { label: "B", text: "4x^2 - 12x + 9 = 25" },
              { label: "C", text: "2x - 3 = \\pm 5" },
              { label: "D", text: "2x - 3 = \\pm 25" }
            ],
            correctIndex: 2, // C
            explanation: "Taking square roots gives \\(2x - 3 = \\pm \\sqrt{25} = \\pm 5\\)."
          },
          {
            title: "Step 2: Solve Both Linear Branches",
            prompt: "Solve \\(2x - 3 = 5\\) and \\(2x - 3 = -5\\).",
            options: [
              { label: "A", text: "x = 4 \\text{ only}" },
              { label: "B", text: "x = 4 \\quad \\text{and} \\quad x = -1" },
              { label: "C", text: "x = 1 \\quad \\text{and} \\quad x = -4" },
              { label: "D", text: "x = 8 \\quad \\text{and} \\quad x = -2" }
            ],
            correctIndex: 1, // B
            explanation: "• \\(2x = 3 + 5 = 8 \\implies x = 4\\).<br>• \\(2x = 3 - 5 = -2 \\implies x = -1\\)."
          }
        ]
      },
      {
        id: 7,
        set: "p1",
        setName: "Practice Problems",
        title: "Binomial Square with Radical Simplification",
        prompt: "Solve the equation using the square root property: \\[(3w + 1)^2 = 18\\]",
        hint: "\\(\\sqrt{18} = \\sqrt{9 \\cdot 2} = 3\\sqrt{2}\\). Then subtract 1 and divide by 3.",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply Square Root Property and Simplify Radical",
            prompt: "What is \\(3w + 1\\) equal to?",
            options: [
              { label: "A", text: "3w + 1 = \\pm 3\\sqrt{2}" },
              { label: "B", text: "3w + 1 = 3\\sqrt{2}" },
              { label: "C", text: "3w + 1 = \\pm 2\\sqrt{3}" },
              { label: "D", text: "3w + 1 = \\pm 9" }
            ],
            correctIndex: 0, // A
            explanation: "\\(3w + 1 = \\pm \\sqrt{18} = \\pm \\sqrt{9 \\cdot 2} = \\pm 3\\sqrt{2}\\)."
          },
          {
            title: "Step 2: Isolate w",
            prompt: "Subtract 1 and divide by 3 to solve for \\(w\\).",
            options: [
              { label: "A", text: "w = -1 \\pm \\sqrt{2}" },
              { label: "B", text: "w = \\frac{1 \\pm 3\\sqrt{2}}{3}" },
              { label: "C", text: "w = \\pm \\sqrt{2}" },
              { label: "D", text: "w = \\frac{-1 \\pm 3\\sqrt{2}}{3} \\quad \\text{or} \\quad -\\frac{1}{3} \\pm \\sqrt{2}" }
            ],
            correctIndex: 3, // D
            explanation: "\\(3w = -1 \\pm 3\\sqrt{2} \\implies w = \\frac{-1 \\pm 3\\sqrt{2}}{3} = -\\frac{1}{3} \\pm \\sqrt{2}\\)."
          }
        ]
      },
      {
        id: 8,
        set: "p1",
        setName: "Practice Problems",
        title: "Square Root Property with Complex Solutions",
        prompt: "Solve the equation using the square root property: \\[(z - 4)^2 = -16\\]",
        hint: "The right-hand side is negative! Recall that \\(\\sqrt{-16} = \\sqrt{16} \\cdot \\sqrt{-1} = 4i\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply Square Root Property with Imaginary Unit",
            prompt: "What does \\(z - 4\\) equal?",
            options: [
              { label: "A", text: "z - 4 = \\pm 4" },
              { label: "B", text: "z - 4 = 4i" },
              { label: "C", text: "z - 4 = -4" },
              { label: "D", text: "z - 4 = \\pm 4i" }
            ],
            correctIndex: 3, // D
            explanation: "\\(z - 4 = \\pm \\sqrt{-16} = \\pm 4i\\)."
          },
          {
            title: "Step 2: Solve for z",
            prompt: "Add 4 to both sides to state the complex solutions.",
            options: [
              { label: "A", text: "z = -4 \\pm 4i" },
              { label: "B", text: "z = 4 \\pm 4i" },
              { label: "C", text: "z = \\pm 8i" },
              { label: "D", text: "No solution exists in any number system" }
            ],
            correctIndex: 1, // B
            explanation: "\\(z = 4 \\pm 4i\\)."
          }
        ]
      },

      // ---------- PART 2: ASSIGNMENT PROBLEMS (9 TO 20) ----------
      {
        id: 9,
        set: "p2",
        setName: "Assignment Problems",
        title: "Factoring Monic Trinomial",
        prompt: "Solve the quadratic equation by factoring: \\[u^2 + 11u + 28 = 0\\]",
        hint: "Find two numbers whose product is 28 and sum is 11. (7 and 4).",
        svg: null,
        steps: [
          {
            title: "Step 1: Factor the Trinomial",
            prompt: "What is the factored form of \\(u^2 + 11u + 28\\)?",
            options: [
              { label: "A", text: "(u - 7)(u - 4) = 0" },
              { label: "B", text: "(u + 7)(u + 4) = 0" },
              { label: "C", text: "(u + 14)(u + 2) = 0" },
              { label: "D", text: "(u + 28)(u + 1) = 0" }
            ],
            correctIndex: 1, // B
            explanation: "\\(7 \\times 4 = 28\\) and \\(7 + 4 = 11\\), so \\((u + 7)(u + 4) = 0\\)."
          },
          {
            title: "Step 2: Solve for u",
            prompt: "What are the solutions for \\(u\\)?",
            options: [
              { label: "A", text: "u = -7 \\quad \\text{and} \\quad u = -4" },
              { label: "B", text: "u = 7 \\quad \\text{and} \\quad u = 4" },
              { label: "C", text: "u = -14 \\quad \\text{and} \\quad u = -2" },
              { label: "D", text: "u = -11 \\quad \\text{and} \\quad u = 28" }
            ],
            correctIndex: 0, // A
            explanation: "\\(u + 7 = 0 \\implies u = -7\\); \\(u + 4 = 0 \\implies u = -4\\)."
          }
        ]
      },
      {
        id: 10,
        set: "p2",
        setName: "Assignment Problems",
        title: "Factoring Trinomial with Leading Coefficient 2",
        prompt: "Solve the quadratic equation by factoring: \\[2x^2 - 9x + 4 = 0\\]",
        hint: "Find factors of \\(2(4) = 8\\) that add to -9. These are -8 and -1.",
        svg: null,
        steps: [
          {
            title: "Step 1: Factor the Trinomial",
            prompt: "What is the correct factorization of \\(2x^2 - 9x + 4\\)?",
            options: [
              { label: "A", text: "(2x - 4)(x - 1)" },
              { label: "B", text: "(2x + 1)(x - 4)" },
              { label: "C", text: "(2x - 1)(x - 4)" },
              { label: "D", text: "(x - 8)(2x - 1)" }
            ],
            correctIndex: 2, // C
            explanation: "\\(2x^2 - 8x - x + 4 = 2x(x - 4) - 1(x - 4) = (2x - 1)(x - 4) = 0\\)."
          },
          {
            title: "Step 2: Solve for x",
            prompt: "Apply Zero Factor Property to find \\(x\\).",
            options: [
              { label: "A", text: "x = -1/2 \\quad \\text{and} \\quad x = -4" },
              { label: "B", text: "x = 2 \\quad \\text{and} \\quad x = 4" },
              { label: "C", text: "x = 1/2 \\quad \\text{and} \\quad x = -4" },
              { label: "D", text: "x = 1/2 \\quad \\text{and} \\quad x = 4" }
            ],
            correctIndex: 3, // D
            explanation: "\\(2x - 1 = 0 \\implies x = 1/2\\); \\(x - 4 = 0 \\implies x = 4\\)."
          }
        ]
      },
      {
        id: 11,
        set: "p2",
        setName: "Assignment Problems",
        title: "Factoring Binomial with GCF",
        prompt: "Solve the equation: \\[5t^2 = -20t\\]",
        hint: "Add \\(20t\\) to the left side: \\(5t^2 + 20t = 0\\). Do NOT divide by \\(t\\)!",
        svg: null,
        steps: [
          {
            title: "Step 1: Write with Zero on Right and Factor",
            prompt: "What is the factored form of the equation?",
            options: [
              { label: "A", text: "5t(t + 4) = 0" },
              { label: "B", text: "5t(t - 4) = 0" },
              { label: "C", text: "t(5t - 20) = 0" },
              { label: "D", text: "5(t^2 + 4) = 0" }
            ],
            correctIndex: 0, // A
            explanation: "\\(5t^2 + 20t = 0 \\implies 5t(t + 4) = 0\\)."
          },
          {
            title: "Step 2: Solve for t",
            prompt: "State both solutions.",
            options: [
              { label: "A", text: "t = -4 \\text{ only}" },
              { label: "B", text: "t = 0 \\quad \\text{and} \\quad t = 4" },
              { label: "C", text: "t = 0 \\quad \\text{and} \\quad t = -4" },
              { label: "D", text: "t = 5 \\quad \\text{and} \\quad t = -4" }
            ],
            correctIndex: 2, // C
            explanation: "\\(5t = 0 \\implies t = 0\\); \\(t + 4 = 0 \\implies t = -4\\)."
          }
        ]
      },
      {
        id: 12,
        set: "p2",
        setName: "Assignment Problems",
        title: "Expanding Binomials to Standard Form",
        prompt: "Solve the equation: \\[(2y - 1)(y - 3) = -2\\]",
        hint: "Expand the left side: \\(2y^2 - 7y + 3 = -2\\). Add 2 to both sides so the right side is zero!",
        svg: null,
        steps: [
          {
            title: "Step 1: Expand and Set to Zero",
            prompt: "What is the standard form equation?",
            options: [
              { label: "A", text: "2y^2 - 7y + 1 = 0" },
              { label: "B", text: "2y^2 - 7y - 5 = 0" },
              { label: "C", text: "2y^2 - 6y + 5 = 0" },
              { label: "D", text: "2y^2 - 7y + 5 = 0" }
            ],
            correctIndex: 3, // D
            explanation: "\\(2y^2 - 6y - y + 3 = -2 \\implies 2y^2 - 7y + 3 + 2 = 0 \\implies 2y^2 - 7y + 5 = 0\\)."
          },
          {
            title: "Step 2: Factor and Solve",
            prompt: "Factor \\(2y^2 - 7y + 5 = 0\\) and solve for \\(y\\).",
            options: [
              { label: "A", text: "(2y + 5)(y + 1) = 0 \\implies y = -5/2, -1" },
              { label: "B", text: "(2y - 5)(y - 1) = 0 \\implies y = 5/2, 1" },
              { label: "C", text: "(2y - 1)(y - 5) = 0 \\implies y = 1/2, 5" },
              { label: "D", text: "(y - 5)(2y + 1) = 0 \\implies y = 5, -1/2" }
            ],
            correctIndex: 1, // B
            explanation: "\\((2y - 5)(y - 1) = 0 \\implies y = 5/2\\) or \\(y = 1\\)."
          }
        ]
      },
      {
        id: 13,
        set: "p2",
        setName: "Assignment Problems",
        title: "Distributive Monomial with Non-Zero RHS",
        prompt: "Solve the equation: \\[x(3x + 10) = 8\\]",
        hint: "Distribute \\(x\\): \\(3x^2 + 10x = 8\\). Subtract 8 to set equal to zero.",
        svg: null,
        steps: [
          {
            title: "Step 1: Write in Standard Form",
            prompt: "What is the equation after distributing and subtracting 8?",
            options: [
              { label: "A", text: "3x^2 + 10x + 8 = 0" },
              { label: "B", text: "3x^2 + 10x - 8 = 0" },
              { label: "C", text: "3x^2 + 10x = 0" },
              { label: "D", text: "x(3x + 10) - 8 = 8" }
            ],
            correctIndex: 1, // B
            explanation: "\\(3x^2 + 10x - 8 = 0\\)."
          },
          {
            title: "Step 2: Factor and Solve for x",
            prompt: "Factor \\(3x^2 + 10x - 8 = 0\\) and find \\(x\\).",
            options: [
              { label: "A", text: "(3x - 2)(x + 4) = 0 \\implies x = 2/3, -4" },
              { label: "B", text: "(3x + 2)(x - 4) = 0 \\implies x = -2/3, 4" },
              { label: "C", text: "(3x - 4)(x + 2) = 0 \\implies x = 4/3, -2" },
              { label: "D", text: "(x + 8)(3x - 1) = 0 \\implies x = -8, 1/3" }
            ],
            correctIndex: 0, // A
            explanation: "\\(3x^2 + 12x - 2x - 8 = 3x(x + 4) - 2(x + 4) = (3x - 2)(x + 4) = 0 \\implies x = 2/3, -4\\)."
          }
        ]
      },
      {
        id: 14,
        set: "p2",
        setName: "Assignment Problems",
        title: "Basic Square Root Property",
        prompt: "Solve the equation using the square root property: \\[w^2 = 64\\]",
        hint: "Don't forget the \\(\\pm\\) sign.",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply Square Root Property",
            prompt: "What is \\(w\\) equal to?",
            options: [
              { label: "A", text: "w = 8" },
              { label: "B", text: "w = -8" },
              { label: "C", text: "w = \\pm 8" },
              { label: "D", text: "w = \\pm 32" }
            ],
            correctIndex: 2, // C
            explanation: "\\(w = \\pm \\sqrt{64} = \\pm 8\\)."
          },
          {
            title: "Step 2: Verify Solutions",
            prompt: "Do both \\(w = 8\\) and \\(w = -8\\) satisfy \\(w^2 = 64\\)?",
            options: [
              { label: "A", text: "No, (-8)^2 = -64." },
              { label: "B", text: "Only w = 8 is valid because square roots are principal." },
              { label: "C", text: "No, 64 has only one square root." },
              { label: "D", text: "Yes, 8^2 = 64 and (-8)^2 = 64." }
            ],
            correctIndex: 3, // D
            explanation: "Both \\((8)^2 = 64\\) and \\((-8)^2 = 64\\) are true."
          }
        ]
      },
      {
        id: 15,
        set: "p2",
        setName: "Assignment Problems",
        title: "Isolating the Square Before Square Root Property",
        prompt: "Solve the equation using the square root property: \\[4z^2 - 49 = 0\\]",
        hint: "Add 49 to both sides, divide by 4, then take the square root.",
        svg: null,
        steps: [
          {
            title: "Step 1: Isolate z²",
            prompt: "What is \\(z^2\\) equal to?",
            options: [
              { label: "A", text: "z^2 = 49/4" },
              { label: "B", text: "z^2 = 49 - 4" },
              { label: "C", text: "z^2 = 4/49" },
              { label: "D", text: "z^2 = 49" }
            ],
            correctIndex: 0, // A
            explanation: "\\(4z^2 = 49 \\implies z^2 = \\frac{49}{4}\\)."
          },
          {
            title: "Step 2: Take Square Roots",
            prompt: "Solve for \\(z\\).",
            options: [
              { label: "A", text: "z = 7/2" },
              { label: "B", text: "z = \\pm 7/2" },
              { label: "C", text: "z = \\pm 49/4" },
              { label: "D", text: "z = \\pm 7/4" }
            ],
            correctIndex: 1, // B
            explanation: "\\(z = \\pm \\sqrt{\\frac{49}{4}} = \\pm \\frac{7}{2}\\)."
          }
        ]
      },
      {
        id: 16,
        set: "p2",
        setName: "Assignment Problems",
        title: "Dividing by Leading Coefficient First",
        prompt: "Solve the equation using the square root property: \\[2x^2 = 50\\]",
        hint: "Divide both sides by 2 first to isolate \\(x^2\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Isolate x²",
            prompt: "What is \\(x^2\\) equal to?",
            options: [
              { label: "A", text: "x^2 = 100" },
              { label: "B", text: "x^2 = 48" },
              { label: "C", text: "x^2 = 25" },
              { label: "D", text: "x = 25" }
            ],
            correctIndex: 2, // C
            explanation: "Divide both sides by 2: \\(x^2 = 50 / 2 = 25\\)."
          },
          {
            title: "Step 2: Solve for x",
            prompt: "What is \\(x\\)?",
            options: [
              { label: "A", text: "x = 5" },
              { label: "B", text: "x = \\pm 25" },
              { label: "C", text: "x = \\pm 5" },
              { label: "D", text: "x = -5" }
            ],
            correctIndex: 2, // C
            explanation: "\\(x = \\pm \\sqrt{25} = \\pm 5\\)."
          }
        ]
      },
      {
        id: 17,
        set: "p2",
        setName: "Assignment Problems",
        title: "Binomial Square with Radical Simplification",
        prompt: "Solve the equation using the square root property: \\[(t + 5)^2 = 12\\]",
        hint: "Take square roots: \\(t + 5 = \\pm \\sqrt{12} = \\pm 2\\sqrt{3}\\). Then subtract 5.",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply Square Root Property",
            prompt: "What is \\(t + 5\\) equal to in simplified radical form?",
            options: [
              { label: "A", text: "t + 5 = \\pm 3\\sqrt{2}" },
              { label: "B", text: "t + 5 = \\pm 2\\sqrt{3}" },
              { label: "C", text: "t + 5 = \\pm 6" },
              { label: "D", text: "t + 5 = 2\\sqrt{3}" }
            ],
            correctIndex: 1, // B
            explanation: "\\(t + 5 = \\pm \\sqrt{12} = \\pm \\sqrt{4 \\cdot 3} = \\pm 2\\sqrt{3}\\)."
          },
          {
            title: "Step 2: Solve for t",
            prompt: "Subtract 5 from both sides to state the solution.",
            options: [
              { label: "A", text: "t = -5 \\pm 2\\sqrt{3}" },
              { label: "B", text: "t = 5 \\pm 2\\sqrt{3}" },
              { label: "C", text: "t = -5 \\pm 3\\sqrt{2}" },
              { label: "D", text: "t = -5 \\pm 12" }
            ],
            correctIndex: 0, // A
            explanation: "\\(t = -5 \\pm 2\\sqrt{3}\\)."
          }
        ]
      },
      {
        id: 18,
        set: "p2",
        setName: "Assignment Problems",
        title: "Binomial Square with Fractional Result",
        prompt: "Solve the equation using the square root property: \\[(4x - 1)^2 = 32\\]",
        hint: "\\(\\sqrt{32} = \\sqrt{16 \\cdot 2} = 4\\sqrt{2}\\). Add 1 and divide by 4.",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply Square Root Property",
            prompt: "What is \\(4x - 1\\) equal to?",
            options: [
              { label: "A", text: "4x - 1 = \\pm 16\\sqrt{2}" },
              { label: "B", text: "4x - 1 = \\pm 2\\sqrt{8}" },
              { label: "C", text: "4x - 1 = \\pm 4\\sqrt{2}" },
              { label: "D", text: "4x - 1 = 4\\sqrt{2}" }
            ],
            correctIndex: 2, // C
            explanation: "\\(4x - 1 = \\pm \\sqrt{32} = \\pm 4\\sqrt{2}\\)."
          },
          {
            title: "Step 2: Isolate x",
            prompt: "Solve for \\(x\\).",
            options: [
              { label: "A", text: "x = \\frac{1 \\pm 4\\sqrt{2}}{2}" },
              { label: "B", text: "x = -1 \\pm \\sqrt{2}" },
              { label: "C", text: "x = \\frac{-1 \\pm 4\\sqrt{2}}{4}" },
              { label: "D", text: "x = \\frac{1 \\pm 4\\sqrt{2}}{4} \\quad \\text{or} \\quad \\frac{1}{4} \\pm \\sqrt{2}" }
            ],
            correctIndex: 3, // D
            explanation: "\\(4x = 1 \\pm 4\\sqrt{2} \\implies x = \\frac{1 \\pm 4\\sqrt{2}}{4} = \\frac{1}{4} \\pm \\sqrt{2}\\)."
          }
        ]
      },
      {
        id: 19,
        set: "p2",
        setName: "Assignment Problems",
        title: "Binomial Square with Negative Constant",
        prompt: "Solve the equation using the square root property: \\[(y + 3)^2 = -49\\]",
        hint: "\\(\\sqrt{-49} = \\pm 7i\\). Subtract 3 to isolate \\(y\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Apply Square Root Property with i",
            prompt: "What is \\(y + 3\\) equal to?",
            options: [
              { label: "A", text: "y + 3 = \\pm 7i" },
              { label: "B", text: "y + 3 = \\pm 7" },
              { label: "C", text: "y + 3 = -7i" },
              { label: "D", text: "y + 3 = 7i" }
            ],
            correctIndex: 0, // A
            explanation: "\\(y + 3 = \\pm \\sqrt{-49} = \\pm 7i\\)."
          },
          {
            title: "Step 2: Solve for y",
            prompt: "State the complex solutions for \\(y\\).",
            options: [
              { label: "A", text: "y = 3 \\pm 7i" },
              { label: "B", text: "y = -3 \\pm 7i" },
              { label: "C", text: "y = -3 \\pm 7" },
              { label: "D", text: "y = \\pm 4i" }
            ],
            correctIndex: 1, // B
            explanation: "\\(y = -3 \\pm 7i\\)."
          }
        ]
      },
      {
        id: 20,
        set: "p2",
        setName: "Assignment Problems",
        title: "Multi-Step Isolation with Complex Roots",
        prompt: "Solve the equation: \\[3(2z - 5)^2 + 36 = 0\\]",
        hint: "Subtract 36, divide by 3 to get \\((2z - 5)^2 = -12\\). Note that \\(\\sqrt{-12} = \\pm i\\sqrt{12} = \\pm 2i\\sqrt{3}\\).",
        svg: null,
        steps: [
          {
            title: "Step 1: Isolate the Binomial Square",
            prompt: "What is \\((2z - 5)^2\\) equal to?",
            options: [
              { label: "A", text: "(2z - 5)^2 = 12" },
              { label: "B", text: "(2z - 5)^2 = -36" },
              { label: "C", text: "(2z - 5)^2 = -33" },
              { label: "D", text: "(2z - 5)^2 = -12" }
            ],
            correctIndex: 3, // D
            explanation: "\\(3(2z - 5)^2 = -36 \\implies (2z - 5)^2 = -12\\)."
          },
          {
            title: "Step 2: Take Square Roots and Solve for z",
            prompt: "Solve \\(2z - 5 = \\pm 2i\\sqrt{3}\\) for \\(z\\).",
            options: [
              { label: "A", text: "z = \\frac{-5 \\pm 2i\\sqrt{3}}{2}" },
              { label: "B", text: "z = 5 \\pm 2i\\sqrt{3}" },
              { label: "C", text: "z = \\frac{5 \\pm 2i\\sqrt{3}}{2} \\quad \\text{or} \\quad \\frac{5}{2} \\pm i\\sqrt{3}" },
              { label: "D", text: "z = \\frac{5 \\pm i\\sqrt{12}}{3}" }
            ],
            correctIndex: 2, // C
            explanation: "\\(2z = 5 \\pm 2i\\sqrt{3} \\implies z = \\frac{5 \\pm 2i\\sqrt{3}}{2} = \\frac{5}{2} \\pm i\\sqrt{3}\\)."
          }
        ]
      }
    ];

    /* ==========================================================================
       PERSISTENCE & STATE MANAGEMENT ENGINE
       ========================================================================== */
    const STORAGE_KEY = "algebra_solve_quadratic_I_v1";

    let currentStudentName = "Guest";
    let activeProblemId = 1;
    let currentPaletteFilter = "all";

    let stepProgress = {};

    let audioMuted = false;
    let totalSeconds = 0;
    let timerInterval = null;

    function saveSessionProgress() {
      try {
        const payload = {
          studentName: currentStudentName,
          activeProblemId: activeProblemId,
          totalSeconds: totalSeconds,
          stepProgress: stepProgress
        };
        localStorage.setItem(STORAGE_KEY, JSON.stringify(payload));
      } catch (e) {
        console.warn("Storage save error", e);
      }
    }

    function checkSavedSession() {
      try {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (!raw) return;
        const data = JSON.parse(raw);
        if (data && data.studentName) {
          const alertBox = document.getElementById('resumeAlertBox');
          const detailsSpan = document.getElementById('savedSessionDetails');
          const resumeBtn = document.getElementById('resumeSessionBtn');
          const startBtn = document.getElementById('startSessionBtn');
          const input = document.getElementById('studentNameInput');

          input.value = data.studentName;
          let completedSteps = 0;
          Object.keys(data.stepProgress || {}).forEach(k => {
            if (data.stepProgress[k].resolved) completedSteps++;
          });
          detailsSpan.innerText = `Student: ${data.studentName} • ${completedSteps}/40 Steps Completed • Time: ${Math.floor(data.totalSeconds / 60)}m ${data.totalSeconds % 60}s`;
          alertBox.style.display = 'block';
          resumeBtn.style.display = 'inline-block';
          startBtn.innerText = 'Start Fresh Session';
        }
      } catch (e) {
        console.warn("Session check error", e);
      }
    }

    const AudioEngine = {
      ctx: null,
      init() {
        if (!this.ctx) {
          this.ctx = new (window.AudioContext || window.webkitAudioContext)();
        }
      },
      playTone(freq, type, duration, delay = 0) {
        if (audioMuted || !this.ctx) return;
        setTimeout(() => {
          try {
            const osc = this.ctx.createOscillator();
            const gain = this.ctx.createGain();
            osc.type = type;
            osc.frequency.setValueAtTime(freq, this.ctx.currentTime);
            gain.gain.setValueAtTime(0.12, this.ctx.currentTime);
            gain.gain.exponentialRampToValueAtTime(0.0001, this.ctx.currentTime + duration);
            osc.connect(gain);
            gain.connect(this.ctx.destination);
            osc.start();
            osc.stop(this.ctx.currentTime + duration);
          } catch (e) {
            console.warn(e);
          }
        }, delay * 1000);
      },
      correct() {
        this.init();
        this.playTone(659.25, 'sine', 0.15, 0);
        this.playTone(880.00, 'sine', 0.25, 0.12);
      },
      incorrect() {
        this.init();
        this.playTone(196.00, 'triangle', 0.2, 0);
        this.playTone(146.83, 'triangle', 0.3, 0.12);
      }
    };

    function startTimer() {
      if (timerInterval) clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        totalSeconds++;
        const mins = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const secs = String(totalSeconds % 60).padStart(2, '0');
        document.getElementById('timerChip').innerText = `⏱️ ${mins}:${secs}`;
        saveSessionProgress();
      }, 1000);
    }

    function showToast(msg) {
      const t = document.getElementById('toastMessage');
      t.innerText = msg;
      t.style.display = 'block';
      setTimeout(() => { t.style.display = 'none'; }, 2600);
    }

    function initDirectLogin(isResume = false) {
      const nameInput = document.getElementById('studentNameInput').value.trim() || 'Student';
      
      if (isResume) {
        const raw = localStorage.getItem(STORAGE_KEY);
        if (raw) {
          const data = JSON.parse(raw);
          currentStudentName = data.studentName || nameInput;
          activeProblemId = data.activeProblemId || 1;
          totalSeconds = data.totalSeconds || 0;
          stepProgress = data.stepProgress || {};
          showToast(`Welcome back, ${currentStudentName}!`);
        }
      } else {
        currentStudentName = nameInput;
        totalSeconds = 0;
        activeProblemId = 1;
        stepProgress = {};
        saveSessionProgress();
      }

      document.getElementById('userPill').innerHTML = `<strong>Student: ${currentStudentName}</strong>`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${currentStudentName}</strong>`;
      document.getElementById('loginGateView').style.display = 'none';
      
      AudioEngine.init();
      startTimer();
      renderPalette();
      loadProblem(activeProblemId);
    }

    function resetStudentProgress() {
      if (confirm("Reset all 20 problem attempts and scorecard progress?")) {
        localStorage.removeItem(STORAGE_KEY);
        location.reload();
      }
    }

    function switchMainTab(tab) {
      document.getElementById('tabPracticeBtn').classList.toggle('active', tab === 'practice');
      document.getElementById('tabTheoryBtn').classList.toggle('active', tab === 'theory');
      document.getElementById('tabScorecardBtn').classList.toggle('active', tab === 'scorecard');

      document.getElementById('viewPractice').classList.toggle('active', tab === 'practice');
      document.getElementById('viewTheory').classList.toggle('active', tab === 'theory');
      document.getElementById('viewScorecard').classList.toggle('active', tab === 'scorecard');

      if (tab === 'scorecard') {
        renderScorecard();
      } else if (tab === 'practice') {
        renderPalette();
        loadProblem(activeProblemId);
      }

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function filterPalette(mode) {
      currentPaletteFilter = mode;
      document.getElementById('filterAllBtn').classList.toggle('active', mode === 'all');
      document.getElementById('filterP1Btn').classList.toggle('active', mode === 'p1');
      document.getElementById('filterP2Btn').classList.toggle('active', mode === 'p2');
      renderPalette();
    }

    function renderAlignedTopicBanner() {
      const banner = document.getElementById('topicBannerContainer');
      banner.innerHTML = `
        <h3>📚 Solving Quadratic Equations: Core Concept Reference</h3>
        <p style="font-size:0.94rem; color:var(--text-main); line-height:1.6;">
          A quadratic equation has the general form \\(ax^2 + bx + c = 0\\). In Part I, we master two algebraic tools: the <strong>Zero Factor Property</strong> (which requires a zero on one side) and the <strong>Square Root Property</strong> (which handles perfect squares directly, including complex roots).
        </p>
        
        <div class="formula-box">
          <strong>Key Mathematical Laws:</strong>
          \\[AB = 0 \\iff A = 0 \\quad \\text{or} \\quad B = 0 \\qquad \\text{and} \\qquad u^2 = p \\implies u = \\pm \\sqrt{p}\\]
        </div>

        <div class="paul-notes-container">
          <h4>📖 Paul's Online Notes: Core Rules &amp; Frequent Traps</h4>
          <div class="paul-notes-body">
            <ul>
              <li><strong>Zero on One Side:</strong> The Zero Factor Property is valid <em>only</em> when the product equals zero. If an equation has a non-zero constant on the right, you must expand, move all terms to the left, and factor from scratch!</li>
              <li><strong>Do NOT Divide by the Variable:</strong> In equations such as \\(4y^2 = 12y\\), never divide by \\(y\\). That loses the root \\(y = 0\\). Always move terms to one side and factor out the common factor.</li>
              <li><strong>The Plus-Minus Sign (\\(\\pm\\)):</strong> When taking square roots of both sides, you <em>must</em> include the \\(\\pm\\) sign. Every non-zero number has two square roots.</li>
              <li><strong>Negative Radicands:</strong> If \\(u^2 = -k\\) with \\(k > 0\\), use the imaginary unit: \\(u = \\pm \\sqrt{-k} = \\pm i\\sqrt{k}\\).</li>
            </ul>
          </div>
        </div>
      `;
    }

    function toggleHint(pId) {
      const hintBox = document.getElementById(`hintBox_${pId}`);
      if (hintBox) {
        const isHidden = hintBox.style.display === 'none' || hintBox.style.display === '';
        hintBox.style.display = isHidden ? 'block' : 'none';
      }
    }

    function renderPalette() {
      const grid = document.getElementById('paletteGrid');
      grid.innerHTML = '';

      let completedProblems = 0;

      let filteredList = PROBLEMS_DATA;
      if (currentPaletteFilter === 'p1') filteredList = PROBLEMS_DATA.filter(p => p.set === 'p1');
      if (currentPaletteFilter === 'p2') filteredList = PROBLEMS_DATA.filter(p => p.set === 'p2');

      PROBLEMS_DATA.forEach((prob) => {
        let allResolved = true;
        prob.steps.forEach((_, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (!sp || !sp.resolved) allResolved = false;
        });
        if (allResolved) completedProblems++;
      });

      filteredList.forEach((prob) => {
        let allResolved = true;
        let anyResolved = false;

        prob.steps.forEach((_, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (sp && sp.resolved) anyResolved = true;
          else allResolved = false;
        });

        const btn = document.createElement('button');
        let stateClass = '';
        if (prob.id === activeProblemId) stateClass = 'active';
        else if (allResolved) stateClass = 'completed';
        else if (anyResolved) stateClass = 'partial';

        btn.className = `palette-btn ${stateClass}`;
        btn.innerHTML = `<span>${prob.id}</span>`;
        btn.title = `Problem ${prob.id}: ${prob.title}`;
        btn.onclick = () => loadProblem(prob.id);
        grid.appendChild(btn);
      });

      document.getElementById('paletteCount').innerText = `${completedProblems} / ${PROBLEMS_DATA.length} Solved`;
    }

    function loadProblem(pId) {
      activeProblemId = pId;
      saveSessionProgress();
      renderPalette();

      const prob = PROBLEMS_DATA.find(p => p.id === pId);
      const card = document.getElementById('activeQuestionCard');

      renderAlignedTopicBanner();

      let stepsHtml = '';

      // STRICT STEP GATING:
      // Step k is ONLY rendered if Step k-1 is resolved!
      prob.steps.forEach((step, sIdx) => {
        const key = `${prob.id}_${sIdx}`;
        const sp = stepProgress[key] || { attempts: 0, selectedIndex: null, resolved: false, correct: false };

        let canShow = false;
        if (sIdx === 0) {
          canShow = true;
        } else {
          const prevKey = `${prob.id}_${sIdx - 1}`;
          const prevSp = stepProgress[prevKey];
          if (prevSp && prevSp.resolved) {
            canShow = true;
          }
        }

        if (!canShow) return;

        let optionsHtml = '';
        step.options.forEach((opt, optIdx) => {
          let optClass = '';
          if (sp.resolved) {
            if (optIdx === step.correctIndex) {
              optClass = 'selected-correct';
            } else if (sp.selectedIndex === optIdx) {
              optClass = 'selected-wrong';
            }
          }

          optionsHtml += `
            <button class="mcq-option-btn ${optClass}" 
              onclick="handleStepSelect(${prob.id}, ${sIdx}, ${optIdx})"
              ${sp.resolved ? 'disabled' : ''}>
              <span class="opt-letter">(${opt.label})</span>
              <span>\\(${opt.text}\\)</span>
            </button>
          `;
        });

        let feedbackHtml = '';
        if (sp.resolved) {
          feedbackHtml = `
            <div class="step-feedback-box ${sp.correct ? 'correct' : 'incorrect'}">
              <strong>${sp.correct ? '✓ Step Completed' : '✗ Solution Revealed'}</strong> (Correct Choice: Option ${step.options[step.correctIndex].label})<br/>
              <div style="margin-top: 6px;">${step.explanation}</div>
            </div>
          `;
        }

        stepsHtml += `
          <div class="step-unit ${sp.resolved ? 'completed' : ''}">
            <div class="step-header">
              <div class="step-title">
                <span>${step.title}</span>
                ${sp.resolved ? '<span class="step-badge resolved">Finished</span>' : `<span class="step-badge">Active Step</span>`}
              </div>
              <span class="attempts-badge">Attempts: ${sp.attempts}/2</span>
            </div>
            <div style="font-size: 0.95rem; line-height: 1.6; margin-bottom: 10px;">${step.prompt}</div>
            <div class="mcq-container">${optionsHtml}</div>
            
            ${!sp.resolved && sp.attempts >= 2 ? `
              <button class="btn-reveal-step" onclick="revealStepSolution(${prob.id},${sIdx})">
                Reveal Step Solution &amp; Continue
              </button>
            ` : ''}

            ${feedbackHtml}
          </div>
        `;
      });

      const pIdx = PROBLEMS_DATA.findIndex(p => p.id === prob.id);
      const prevDisabled = pIdx === 0 ? 'disabled' : '';
      const nextDisabled = pIdx === PROBLEMS_DATA.length - 1 ? 'disabled' : '';

      card.innerHTML = `
        <div style="display:flex; justify-content:space-between; align-items:center; flex-wrap:wrap;">
          <span class="concept-tag">${prob.setName}</span>
          <span style="font-size:0.82rem; color:var(--text-muted);">Algebra: Solving Quadratic Equations I</span>
        </div>
        
        <h2 style="color:var(--navy-dark); margin: 6px 0 10px 0;">Problem ${prob.id}: ${prob.title}</h2>
        <div style="margin-top: 8px; line-height: 1.65; font-size:1.02rem;">${prob.prompt}</div>
        
        <div class="hint-container">
          <button class="btn-hint-toggle" onclick="toggleHint(${prob.id})">
            💡 Need a Hint? Click to View / Hide
          </button>
          <div class="hint-box" id="hintBox_${prob.id}">
            <strong>Pedagogical Hint:</strong> ${prob.hint}
          </div>
        </div>

        ${prob.svg ? `<div class="svg-container">${prob.svg}</div>` : ''}
        
        <div style="margin-top: 18px;">${stepsHtml}</div>

        <div class="nav-toolbar">
          <button class="btn-nav-action" onclick="navigateProblem(-1)" ${prevDisabled}>
            ⏮ Previous Problem
          </button>
          <div class="nav-btn-group">
            <button class="btn-nav-action btn-skip" onclick="skipProblem(${prob.id})">
              ⏭ Skip Problem
            </button>
            <button class="btn-nav-action" onclick="navigateProblem(1)" ${nextDisabled}>
              Next Problem ❯
            </button>
          </div>
        </div>
      `;

      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    function handleStepSelect(pId, sIdx, optIdx) {
      const prob = PROBLEMS_DATA.find(p => p.id === pId);
      const step = prob.steps[sIdx];
      const key = `${pId}_${sIdx}`;

      if (!stepProgress[key]) {
        stepProgress[key] = { attempts: 0, selectedIndex: null, resolved: false, correct: false };
      }
      const sp = stepProgress[key];
      if (sp.resolved) return;

      sp.selectedIndex = optIdx;
      sp.attempts++;

      if (optIdx === step.correctIndex) {
        sp.resolved = true;
        sp.correct = true;
        AudioEngine.correct();
        showToast(`Step ${sIdx + 1} Completed! Next step unlocked.`);
      } else {
        AudioEngine.incorrect();
        if (sp.attempts >= 2) {
          showToast(`2 attempts reached. Click 'Reveal Step Solution' to unlock next step.`);
        } else {
          showToast(`Incorrect option. 1 attempt remaining!`);
        }
      }

      saveSessionProgress();
      renderPalette();
      loadProblem(pId);
    }

    function revealStepSolution(pId, sIdx) {
      const key = `${pId}_${sIdx}`;
      if (!stepProgress[key]) {
        stepProgress[key] = { attempts: 2, selectedIndex: null, resolved: false, correct: false };
      }
      const sp = stepProgress[key];
      sp.resolved = true;
      sp.correct = false;
      AudioEngine.incorrect();
      showToast(`Step ${sIdx + 1} solution revealed. Next step unlocked.`);
      saveSessionProgress();
      renderPalette();
      loadProblem(pId);
    }

    function navigateProblem(delta) {
      const pIdx = PROBLEMS_DATA.findIndex(p => p.id === activeProblemId);
      const target = pIdx + delta;
      if (target >= 0 && target < PROBLEMS_DATA.length) {
        loadProblem(PROBLEMS_DATA[target].id);
      }
    }

    function skipProblem(pId) {
      showToast(`Problem ${pId} skipped.`);
      navigateProblem(1);
    }

    function renderScorecard() {
      const container = document.getElementById('completeSolutionsContainer');
      let fullySolvedProblems = 0;
      let totalSteps = 0;
      let correctSteps = 0;

      PROBLEMS_DATA.forEach(p => {
        let probComplete = true;
        p.steps.forEach((_, sIdx) => {
          totalSteps++;
          const key = `${p.id}_${sIdx}`;
          const sp = stepProgress[key];
          if (sp && sp.correct) {
            correctSteps++;
          } else {
            probComplete = false;
          }
        });
        if (probComplete) fullySolvedProblems++;
      });

      const percentage = Math.round((correctSteps / totalSteps) * 100);

      document.getElementById('scoreValue').innerText = `${fullySolvedProblems} / ${PROBLEMS_DATA.length}`;
      document.getElementById('progressBarFill').style.width = `${percentage}%`;
      document.getElementById('reportStudentBadge').innerHTML = `<strong>Student: ${currentStudentName}</strong> (${correctSteps}/${totalSteps} Steps Correct • ${percentage}%)`;

      let html = '';
      PROBLEMS_DATA.forEach(prob => {
        let probStepsHtml = prob.steps.map((step, sIdx) => {
          const key = `${prob.id}_${sIdx}`;
          const sp = stepProgress[key] || { attempts: 0, selectedIndex: null, resolved: false, correct: false };
          
          let badge = `<span style="color:var(--text-muted); font-weight:bold;">Unattempted</span>`;
          if (sp.resolved) {
            badge = sp.correct 
              ? `<span style="color:var(--green-ok); font-weight:bold;">✓ Correct (Attempt ${sp.attempts})</span>` 
              : `<span style="color:var(--red-fail); font-weight:bold;">✗ Solution Revealed</span>`;
          }

          const userChoiceText = (sp.selectedIndex !== null && step.options[sp.selectedIndex]) 
            ? `(${step.options[sp.selectedIndex].label}) \\(${step.options[sp.selectedIndex].text}\\)` 
            : 'None';

          return `
            <div style="background:#f8fafc; border-left:4px solid var(--brand-blue); padding:12px; margin-top:10px; border-radius:0 6px 6px 0;">
              <div style="display:flex; justify-content:space-between; margin-bottom:4px;">
                <strong>${step.title}</strong>
                ${badge}
              </div>
              <p style="font-size:0.9rem; margin-bottom:4px;"><strong>Target:</strong> ${step.prompt}</p>
              <p style="font-size:0.88rem;"><strong>Your Choice:</strong> ${userChoiceText}</p>
              <p style="font-size:0.88rem;"><strong>Correct Option:</strong> (${step.options[step.correctIndex].label}) \\(${step.options[step.correctIndex].text}\\)</p>
              <p style="font-size:0.86rem; color:var(--text-muted); margin-top:4px;">${step.explanation}</p>
            </div>
          `;
        }).join('');

        html += `
          <div class="theory-card" style="margin-bottom:20px;">
            <div style="display:flex; justify-content:space-between; align-items:center;">
              <span class="concept-tag">${prob.setName}</span>
              <span style="font-size:0.85rem; color:var(--text-muted);">Problem ${prob.id} of ${PROBLEMS_DATA.length}</span>
            </div>
            <h3 style="margin-top:6px;">Problem ${prob.id}: ${prob.title}</h3>
            <div style="margin: 8px 0; font-size:0.95rem;">${prob.prompt}</div>
            ${prob.svg ? `<div class="svg-container" style="max-width:320px; margin:12px 0;">${prob.svg}</div>` : ''}
            <div>${probStepsHtml}</div>
          </div>
        `;
      });

      container.innerHTML = html;
      if (window.MathJax && window.MathJax.typesetPromise) {
        MathJax.typesetPromise();
      }
    }

    document.getElementById('audioToggleBtn').onclick = () => {
      audioMuted = !audioMuted;
      document.getElementById('audioToggleBtn').innerText = audioMuted ? '🔇' : '🔊';
    };

    window.addEventListener('DOMContentLoaded', checkSavedSession);
  </script>
</body>
</html>
