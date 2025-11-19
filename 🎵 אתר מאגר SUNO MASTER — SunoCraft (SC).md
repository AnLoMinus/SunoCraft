## 🎵 אתר מאגר SUNO MASTER — SunoCraft (SC)

**תאריך לועזי:** 19/11/2025
**תאריך עברי:** י״ז בחשוון תשפ״ו
**שעה נוכחית:** 13:20

**קרדיטים ומקורות מאגרים:**

* 🎛️ חזון, רעיון ותוכן: **AnLoMinus** — [github.com/AnLoMinus](https://github.com/AnLoMinus)
* 🎶 מאגר SunoCraft (SC) – תשתית למדריכי SUNO: **SunoCraft Repo** — `https://github.com/AnLoMinus/SunoCraft` *(להקמה)*

שם המאגר: **SunoCraft — SC (Suno + Craft)**

> מאגר ראשי: *Ultimate Suno Music Creation Guide* – מדריך מלא ליצירה, פרומפטים, סגנונות והורדות.

---

## 💻 קוד אתר מלא (index.html)

שמור את התוכן הבא כקובץ `index.html` בתוך מאגר `SunoCraft` או בכל פרויקט GitHub Pages שלך, והוא ייתן לך אתר מסודר, יפה ומוכן להרחבה ✨

```html
<!DOCTYPE html>
<html lang="he">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>SunoCraft (SC) – Suno Master Library</title>
  <style>
    :root {
      --bg-main: #050816;
      --bg-soft: #0b1020;
      --accent: #ffcc4d;
      --accent-soft: rgba(255, 204, 77, 0.12);
      --accent-2: #6b5bff;
      --accent-3: #19d3ff;
      --text-main: #f7f7ff;
      --text-muted: #b3b8d0;
      --border-soft: #242842;
      --radius-xl: 22px;
      --shadow-soft: 0 18px 40px rgba(0, 0, 0, 0.55);
      --max-width: 1120px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      direction: rtl;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
        sans-serif;
      background: radial-gradient(circle at top, #1b1f3b 0, #050816 45%, #02030a 100%);
      color: var(--text-main);
      line-height: 1.6;
    }

    .page {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 24px 16px 48px;
    }

    /* HEADER / HERO */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(18px);
      background: linear-gradient(
        to bottom,
        rgba(5, 8, 22, 0.98),
        rgba(5, 8, 22, 0.85),
        transparent
      );
      border-bottom: 1px solid rgba(255, 255, 255, 0.03);
    }

    .nav-inner {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 12px 16px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-icon {
      width: 32px;
      height: 32px;
      border-radius: 999px;
      background: conic-gradient(
        from 210deg,
        #ffcc4d,
        #ff7b5c,
        #6b5bff,
        #19d3ff,
        #ffcc4d
      );
      box-shadow: 0 0 24px rgba(255, 204, 77, 0.7);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 18px;
    }

    .brand-text-main {
      font-weight: 700;
      font-size: 18px;
      letter-spacing: 0.03em;
      display: flex;
      flex-direction: column;
    }

    .brand-text-main span:nth-child(2) {
      font-size: 11px;
      color: var(--text-muted);
      font-weight: 500;
    }

    .nav-links {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: flex-end;
    }

    .nav-links a {
      font-size: 13px;
      color: var(--text-muted);
      text-decoration: none;
      padding: 6px 10px;
      border-radius: 999px;
      border: 1px solid transparent;
      transition: all 0.2s ease;
      background: rgba(255, 255, 255, 0.02);
    }

    .nav-links a:hover {
      color: var(--accent);
      border-color: rgba(255, 204, 77, 0.45);
      background: rgba(255, 255, 255, 0.03);
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 2.1fr) minmax(0, 1.6fr);
      gap: 24px;
      margin-top: 32px;
      align-items: center;
    }

    @media (max-width: 860px) {
      .hero {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .hero-text {
      padding: 20px 18px;
      border-radius: var(--radius-xl);
      border: 1px solid rgba(255, 255, 255, 0.06);
      background: radial-gradient(circle at top right, #1b1f3b 0, #050816 55%);
      box-shadow: var(--shadow-soft);
      position: relative;
      overflow: hidden;
    }

    .hero-pill {
      font-size: 11px;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      padding: 4px 10px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.14);
      background: rgba(0, 0, 0, 0.45);
      color: var(--text-muted);
      margin-bottom: 10px;
    }

    .hero-pill span.emoji {
      font-size: 14px;
    }

    .hero h1 {
      font-size: 28px;
      margin-bottom: 8px;
    }

    .hero h1 span {
      background: linear-gradient(120deg, #ffcc4d, #ff7b5c, #19d3ff);
      -webkit-background-clip: text;
      color: transparent;
    }

    .hero-subtitle {
      font-size: 15px;
      color: var(--text-muted);
      margin-bottom: 12px;
    }

    .hero-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-bottom: 14px;
    }

    .hero-tags span {
      font-size: 11px;
      padding: 4px 8px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.04);
      color: var(--text-muted);
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 6px;
    }

    .btn-primary,
    .btn-ghost {
      border-radius: 999px;
      font-size: 13px;
      padding: 8px 16px;
      cursor: pointer;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 6px;
      border: 1px solid transparent;
      transition: all 0.2s ease;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(130deg, #ffcc4d, #ff7b5c);
      color: #181008;
      font-weight: 600;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.55);
    }

    .btn-primary:hover {
      transform: translateY(-1px);
      box-shadow: 0 14px 30px rgba(0, 0, 0, 0.7);
    }

    .btn-ghost {
      background: rgba(0, 0, 0, 0.4);
      color: var(--text-muted);
      border-color: rgba(255, 255, 255, 0.12);
    }

    .btn-ghost:hover {
      color: var(--accent);
      border-color: rgba(255, 204, 77, 0.6);
    }

    .hero-badge {
      position: absolute;
      inset: auto 12px 12px auto;
      font-size: 11px;
      color: var(--text-muted);
      padding: 4px 8px;
      border-radius: 999px;
      background: rgba(0, 0, 0, 0.7);
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .hero-visual {
      border-radius: var(--radius-xl);
      border: 1px solid rgba(255, 255, 255, 0.06);
      background: radial-gradient(circle at 10% 0%, #ffcc4d22 0, #050816 45%, #0b1020 100%);
      box-shadow: var(--shadow-soft);
      padding: 18px;
      position: relative;
      overflow: hidden;
    }

    .orb {
      position: absolute;
      border-radius: 999px;
      filter: blur(12px);
      opacity: 0.9;
    }

    .orb-1 {
      width: 160px;
      height: 160px;
      background: radial-gradient(circle, #ffcc4d, transparent 65%);
      top: -40px;
      left: -20px;
    }

    .orb-2 {
      width: 130px;
      height: 130px;
      background: radial-gradient(circle, #6b5bff, transparent 70%);
      bottom: -20px;
      right: -30px;
    }

    .orb-3 {
      width: 90px;
      height: 90px;
      background: radial-gradient(circle, #19d3ff, transparent 70%);
      bottom: 40px;
      left: 40px;
    }

    .hero-visual-inner {
      position: relative;
      z-index: 2;
      border-radius: 18px;
      padding: 14px;
      background: rgba(0, 0, 0, 0.7);
      border: 1px solid rgba(255, 255, 255, 0.12);
    }

    .hero-visual-title {
      font-size: 14px;
      margin-bottom: 6px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
    }

    .hero-visual-title span.badge {
      font-size: 11px;
      padding: 3px 8px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.04);
      color: var(--text-muted);
    }

    .hero-visual-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 8px;
      margin-top: 6px;
      font-size: 11px;
      color: var(--text-muted);
    }

    .hero-visual-item {
      padding: 8px;
      border-radius: 12px;
      background: rgba(255, 255, 255, 0.02);
      border: 1px solid rgba(255, 255, 255, 0.05);
    }

    .hero-visual-item strong {
      font-size: 11px;
      color: var(--accent-3);
      display: block;
      margin-bottom: 3px;
    }

    .section {
      margin-top: 36px;
    }

    .section-header {
      display: flex;
      align-items: baseline;
      justify-content: space-between;
      gap: 8px;
      margin-bottom: 14px;
    }

    .section-title {
      font-size: 20px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .section-title span.icon {
      font-size: 22px;
    }

    .section-subtitle {
      font-size: 13px;
      color: var(--text-muted);
    }

    .grid-2 {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 18px;
    }

    @media (max-width: 860px) {
      .grid-2 {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .card {
      padding: 16px 14px;
      border-radius: var(--radius-xl);
      border: 1px solid var(--border-soft);
      background: rgba(5, 8, 22, 0.96);
      box-shadow: var(--shadow-soft);
    }

    .card-soft {
      background: rgba(5, 8, 22, 0.9);
      border-style: dashed;
    }

    .card h3 {
      font-size: 16px;
      margin-bottom: 8px;
    }

    .card p {
      font-size: 14px;
      color: var(--text-muted);
      margin-bottom: 8px;
    }

    .card ul {
      list-style: none;
      font-size: 13px;
      color: var(--text-muted);
      padding-right: 14px;
    }

    .card ul li {
      margin-bottom: 4px;
      position: relative;
    }

    .card ul li::before {
      content: "•";
      position: absolute;
      right: -10px;
      color: var(--accent-2);
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 6px;
    }

    .pill {
      font-size: 11px;
      padding: 4px 8px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.08);
      background: rgba(255, 255, 255, 0.02);
      color: var(--text-muted);
    }

    table {
      width: 100%;
      border-collapse: collapse;
      font-size: 12px;
      margin-top: 8px;
      border-radius: 14px;
      overflow: hidden;
      border: 1px solid rgba(255, 255, 255, 0.08);
    }

    table thead {
      background: linear-gradient(120deg, #6b5bff33, #19d3ff33);
    }

    table th,
    table td {
      padding: 7px 8px;
      text-align: right;
    }

    table th {
      font-weight: 600;
      font-size: 11px;
    }

    table tr:nth-child(even) td {
      background: rgba(255, 255, 255, 0.03);
    }

    .code-block {
      background: #050612;
      border-radius: 14px;
      border: 1px solid rgba(255, 255, 255, 0.08);
      padding: 10px 12px;
      font-family: "JetBrains Mono", ui-monospace, SFMono-Regular, Menlo,
        Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      font-size: 11px;
      direction: ltr;
      text-align: left;
      color: #e5e7ff;
      overflow-x: auto;
      margin-top: 8px;
    }

    .badge-label {
      display: inline-flex;
      align-items: center;
      gap: 6px;
      font-size: 11px;
      padding: 3px 9px;
      border-radius: 999px;
      background: rgba(255, 255, 255, 0.03);
      border: 1px solid rgba(255, 255, 255, 0.06);
      color: var(--text-muted);
      margin-bottom: 4px;
    }

    .dl-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 10px;
      margin-top: 10px;
    }

    @media (max-width: 720px) {
      .dl-grid {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }
    }

    @media (max-width: 520px) {
      .dl-grid {
        grid-template-columns: minmax(0, 1fr);
      }
    }

    .dl-item {
      padding: 10px;
      border-radius: 14px;
      background: rgba(255, 255, 255, 0.02);
      border: 1px solid rgba(255, 255, 255, 0.06);
      font-size: 12px;
    }

    .dl-item strong {
      display: block;
      margin-bottom: 4px;
    }

    .dl-item a {
      font-size: 11px;
      color: var(--accent-3);
      text-decoration: none;
    }

    .dl-item a:hover {
      text-decoration: underline;
    }

    .faq-list {
      font-size: 13px;
      color: var(--text-muted);
      list-style: none;
      padding-right: 10px;
    }

    .faq-list li {
      margin-bottom: 8px;
    }

    .faq-q {
      color: var(--accent);
      font-weight: 600;
      display: block;
      margin-bottom: 2px;
    }

    footer {
      margin-top: 32px;
      padding-top: 18px;
      border-top: 1px solid rgba(255, 255, 255, 0.08);
      font-size: 11px;
      color: var(--text-muted);
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      justify-content: space-between;
      align-items: center;
    }

    .footer-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
    }

    .footer-tags span {
      padding: 3px 7px;
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.08);
      font-size: 10px;
    }

    .rap-block {
      margin-top: 14px;
      padding: 12px 12px 10px;
      border-radius: 16px;
      border: 1px dashed rgba(255, 255, 255, 0.2);
      background: radial-gradient(circle at top, #1b1f3b55, transparent 60%);
      font-size: 13px;
    }

    .rap-block p {
      margin: 0;
    }

    .rap-line {
      display: block;
    }
  </style>
</head>
<body>
  <header>
    <div class="nav-inner">
      <div class="brand">
        <div class="brand-icon">🎧</div>
        <div class="brand-text-main">
          <span>SunoCraft (SC)</span>
          <span>Ultimate Suno Music Creation Library</span>
        </div>
      </div>
      <nav class="nav-links">
        <a href="#about">מה זה SUNO?</a>
        <a href="#getting-started">צעדי התחלה</a>
        <a href="#styles">סגנונות &amp; BPM</a>
        <a href="#prompts">פרומפטים</a>
        <a href="#lyrics">מילים &amp; פלואו</a>
        <a href="#downloads">הורדות</a>
        <a href="#faq">שאלות נפוצות</a>
      </nav>
    </div>
  </header>

  <main class="page">
    <section class="hero" id="top">
      <div class="hero-text">
        <div class="hero-pill">
          <span class="emoji">⚡</span>
          מאגר צידה מקיף ל-SUNO • SunoCraft (SC)
        </div>
        <h1>
          מדריך <span>MASTER</span> ליצירת מוזיקה קדושה, אלקטרונית וראפ ב-SUNO
        </h1>
        <p class="hero-subtitle">
          כל מה שצריך – במקום אחד: סגנונות, BPM, פרומפטים, מילים, טבלאות והורדות.
          בנוי למפיקים, לראפרים ולנשמות שרוצות להעלות את העולם בריקוד. 🎶
        </p>
        <div class="hero-tags">
          <span>🎛 Afro House</span>
          <span>🔥 Trap / Rap</span>
          <span>🕯 Holy Vibes</span>
          <span>🎚 BPM Guide</span>
          <span>🎤 Flow Templates</span>
        </div>
        <div class="hero-actions">
          <a href="#prompts" class="btn-primary">
            📜 קפיצה לפרומפטים מוכנים
          </a>
          <a href="#downloads" class="btn-ghost">
            📦 הורדת תבניות (Templates)
          </a>
        </div>
        <div class="hero-badge">
          נוצר עבור: AnLoMinus • SunoCraft (SC)
        </div>
      </div>

      <aside class="hero-visual" aria-hidden="true">
        <div class="orb orb-1"></div>
        <div class="orb orb-2"></div>
        <div class="orb orb-3"></div>
        <div class="hero-visual-inner">
          <div class="hero-visual-title">
            <span>תצורת שיר SUNO קדוש</span>
            <span class="badge">Preset • SC-HolyTrap-01</span>
          </div>
          <div class="hero-visual-grid">
            <div class="hero-visual-item">
              <strong>GENRE</strong>
              Afro House • Trap • Holy Rap
            </div>
            <div class="hero-visual-item">
              <strong>BPM</strong>
              112–132 • Fast 4/4 • Club + Prayer
            </div>
            <div class="hero-visual-item">
              <strong>VIBE</strong>
              Mystical • Energetic • Uplifting • Kabbalistic
            </div>
            <div class="hero-visual-item">
              <strong>FOCUS</strong>
              Clean flow, punchlines, holy fire, crowd sing-along
            </div>
          </div>
        </div>
      </aside>
    </section>

    <!-- SECTION: ABOUT -->
    <section class="section" id="about">
      <div class="section-header">
        <h2 class="section-title">
          <span class="icon">🎵</span>
          מה זה SUNO? (What is Suno?)
        </h2>
        <p class="section-subtitle">
          מנוע AI שיוצר שירים שלמים – קול, ביט, הרמוניה והפקה מלאה.
        </p>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>🎧 SUNO ככלי ליצירה שלמה</h3>
          <p>
            SUNO מאפשרת לכתוב טקסט, להגדיר סגנון, ולקבל שיר שלם:
            קול אנושי, מנגינה, הרמוניות, תופים, בס ואפקטים. זהו כלי
            שמאפשר להפוך רעיון לשיר מוכן – בלי אולפן פיזי.
          </p>
          <ul>
            <li>קול אנושי (Lead + הרמוניות)</li>
            <li>הפקת ביט מלאה (Drums, Bass, Synths)</li>
            <li>סגנונות מגוונים – RAP, EDM, Afro, Pop ועוד</li>
            <li>מתאים גם לדקה טיקטוק וגם לשיר מלא</li>
          </ul>
        </div>

        <div class="card card-soft">
          <h3>🎯 למה SunoCraft (SC)?</h3>
          <p>
            SunoCraft מרכז את כל ההבנות בפורמט אחד: מדריך, טבלאות, דוגמאות
            פרומפטים, תבניות הורדה וכיווני השראה – כדי שתוכל לייצר
            שירים קדושים, חדים וזורמים בלי לבזבז זמן בניסויים אינסופיים.
          </p>
          <div class="pill-row">
            <span class="pill">⚡ Zero to Track</span>
            <span class="pill">🎤 Rap &amp; Vocals Ready</span>
            <span class="pill">🕯 Kabbalah-Inspired Vibes</span>
            <span class="pill">📜 Prompt Recipes</span>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION: GETTING STARTED -->
    <section class="section" id="getting-started">
      <div class="section-header">
        <h2 class="section-title">
          <span class="icon">🚀</span>
          צעדי התחלה (Getting Started)
        </h2>
        <p class="section-subtitle">
          5 שלבים ברורים – מהרגע של הרעיון ועד לשיר מוכן לשיתוף.
        </p>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>1️⃣ הגדרת כיוון השיר</h3>
          <p>לפני שפותחים את SUNO, עוצרים לרגע ומגדירים:</p>
          <ul>
            <li>מטרה: מסיבה? תפילה? שיר מוטיבציה? ראפ וידוי?</li>
            <li>קהל יעד: חברים? רשתות? אלבום קדושה?</li>
            <li>עוצמה: רגוע, בינוני, פצצה לקרוע את הרחבה?</li>
          </ul>
          <p class="badge-label">טיפ: משפט כיוון אחד כתוב לעצמך, למשל:</p>
          <p class="code-block">
            "שיר Afro House קדוש לקפיצות במועדון נשמות, עם ראפ תפילה וכוח".
          </p>
        </div>

        <div class="card">
          <h3>2️⃣ מבנה בסיסי לפרומפט</h3>
          <p>הפרומפט שלך ל-SUNO צריך לכלול לפחות:</p>
          <ul>
            <li>GENRE – הסגנון המרכזי (Afro / Trap / EDM / Hip-Hop)</li>
            <li>BPM – טווח הקצב</li>
            <li>VIBE – אווירה רגשית/רוחנית</li>
            <li>INSTRUMENTS – תופים, בס, סינתיסייזרים, מקהלה וכו'</li>
            <li>LYRICS – מילים מסודרות לפי בתים ופזמון</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- SECTION: STYLES & BPM -->
    <section class="section" id="styles">
      <div class="section-header">
        <h2 class="section-title">
          <span class="icon">🎚️</span>
          סגנונות &amp; BPM
        </h2>
        <p class="section-subtitle">
          טבלת התאמה בין סגנון, קצב ואווירה – כדי לכוון את השיר בדיוק.
        </p>
      </div>

      <div class="card">
        <h3>🎼 טבלת סגנונות</h3>
        <table>
          <thead>
            <tr>
              <th>סגנון</th>
              <th>BPM מומלץ</th>
              <th>אווירה</th>
              <th>שימוש טיפוסי</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Afro House Holy</td>
              <td>105–118</td>
              <td>שמחה, שבטי, קדושה רוקדת</td>
              <td>מסיבות נשמה, חפלות קדושות</td>
            </tr>
            <tr>
              <td>Electro Tech</td>
              <td>122–132</td>
              <td>חד, אנרגטי, מועדון</td>
              <td>סטרים, ריקוד, אנרגיה גבוהה</td>
            </tr>
            <tr>
              <td>Trap 4/4 Holy</td>
              <td>130–145</td>
              <td>עוצמה, פאנצ'ים, עומק רגשי</td>
              <td>ראפ וידוי, מאבק פנימי, מסר חד</td>
            </tr>
            <tr>
              <td>Spiritual Hip-Hop</td>
              <td>88–105</td>
              <td>עמוק, מהורהר, מרים</td>
              <td>שירי מסר, חיזוק, הודיה</td>
            </tr>
            <tr>
              <td>Temple EDM Choir</td>
              <td>115–128</td>
              <td>מקהלה, גובה רוחני, אורות</td>
              <td>פתיחת אלבום, אנתמים, תחושת מקדש</td>
            </tr>
          </tbody>
        </table>
      </div>
    </section>

    <!-- SECTION: PROMPTS -->
    <section class="section" id="prompts">
      <div class="section-header">
        <h2 class="section-title">
          <span class="icon">📜</span>
          פרומפטים מוכנים ל-SUNO
        </h2>
        <p class="section-subtitle">
          דוגמאות שתוכל להעתיק, להתאים ולהריץ – Zero to Track.
        </p>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>⚡ Holy Afro Electro Prompt</h3>
          <p class="badge-label">English Prompt • מיועד ל-Afro House קדוש</p>
          <div class="code-block">
energetic afro house + electro beat, deep kick, wide tribal drums, 
warm sub bass, bright synth sparks, mystical holy vibe, cosmic fire, 
angelic choir pads, shimmering plucks, uplifting emotional energy, 
club ready but spiritual, clean punchy mix.
          </div>

          <h3 style="margin-top: 10px;">🔥 Holy Trap Rap Prompt</h3>
          <p class="badge-label">Trap 4/4 • Holy Rap Flow</p>
          <div class="code-block">
dark mystical trap 4/4, hard 808 bass, punchy snare, fast hi hats, 
deep male rap voice, holy whispers in background, atmospheric pads, 
cosmic reverb, powerful emotional storytelling, intense but uplifting.
          </div>
        </div>

        <div class="card card-soft">
          <h3>🧱 תבנית כללית לפרומפט מלא</h3>
          <p>השתמש בתבנית הזאת לכל שיר חדש, ופשוט החלף פרטים:</p>
          <div class="code-block">
GENRE: [Afro House / Trap / Hip-Hop / EDM]
BPM: [מספר או טווח]
VIBE: [holy, mystical, energetic, deep, emotional]
INSTRUMENTS: [deep kick, wide drums, sub bass, synth leads, choir pads]
VOCALS: [powerful male lead, angelic female harmonies, holy whispers]

LYRICS:
[Verse 1]
...

[Chorus]
...

[Verse 2]
...

[Bridge]
...
          </div>
          <p style="margin-top: 6px; font-size: 12px; color: var(--text-muted);">
            אפשר לשמור כמה תבניות שונות (Holy Trap / Afro Electro / Temple EDM)
            ולהחליף רק מילים וניואנסים – כך בונים ספריית סגנונות.
          </p>
        </div>
      </div>
    </section>

    <!-- SECTION: LYRICS & FLOW -->
    <section class="section" id="lyrics">
      <div class="section-header">
        <h2 class="section-title">
          <span class="icon">✍️</span>
          מילים, פלואו וחריזה
        </h2>
        <p class="section-subtitle">
          איך לכתוב מילים ש-SUNO יודעת לשיר – בצורה נקייה וזורמת.
        </p>
      </div>

      <div class="grid-2">
        <div class="card">
          <h3>🧠 כללי זהב לכתיבת מילים</h3>
          <ul>
            <li>חריזה בכל שורה – או לפחות כל שתיים-שלוש שורות.</li>
            <li>להוסיף פסיקים ונקודות – כדי לסמן נשימות ו”פאוזות”.</li>
            <li>לא לדחוף יותר מדי מילים בשורה אחת.</li>
            <li>מבנה מומלץ: 4–8 שורות לכל בית, 4 שורות לפזמון.</li>
            <li>לחזור על הפזמון בדיוק או כמעט אותו דבר – SUNO אוהבת חזרתיות.</li>
          </ul>
        </div>

        <div class="card card-soft">
          <h3>🎤 דוגמה לבית + פזמון (עברית קדושה)</h3>
          <div class="code-block">
[Verse]
אני הולך באור שלך, צעד אחרי צעד,
שובר את כל החושך, מעלה את כל הממד,
האש שלך בי בוערת, לא נותנת לי לרדת,
כל מילה הופכת תפילה, כל נשימה היא עדות אחת.

[Chorus]
וִיהִי נֹעַם ה' עלינו, זה הפזמון שלי,
כל ביט שאני דורך עליו הופך לכלי,
מהלב אל המילים, מהשמים עד כלי,
אני שר אותך בעולם – ואתה שר בי.
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION: DOWNLOADS / TEMPLATES -->
    <section class="section" id="downloads">
      <div class="section-header">
        <h2 class="section-title">
          <span class="icon">📦</span>
          תבניות והורדות (Templates & Downloads)
        </h2>
        <p class="section-subtitle">
          בלוק מוכן להוספת קישורים לקבצי MD / PDF / ZIP של המאגר SunoCraft.
        </p>
      </div>

      <div class="card">
        <p>
          כאן תוכל להוסיף קישורים לקבצים מהמאגרים שלך (GitHub / ZIP /
          PDF). פשוט החלף את <strong>href="#"</strong> בקישור אמיתי לכל
          תבנית:
        </p>

        <div class="dl-grid">
          <div class="dl-item">
            <strong>SC-HolyTrap-Lyrics.md</strong>
            <span>תבנית מילים ל-Trap קדוש</span><br />
            <a href="#">הורדה / צפייה</a>
          </div>
          <div class="dl-item">
            <strong>SC-AfroElectro-PromptPack.md</strong>
            <span>חבילת פרומפטים Afro + Electro</span><br />
            <a href="#">הורדה / צפייה</a>
          </div>
          <div class="dl-item">
            <strong>SC-BPM-Guide.pdf</strong>
            <span>מדריך BPM מודפס</span><br />
            <a href="#">הורדה / צפייה</a>
          </div>
          <div class="dl-item">
            <strong>SC-FullProject-Template.zip</strong>
            <span>מבנה מאגר מלא לפרויקט SUNO</span><br />
            <a href="#">הורדה</a>
          </div>
          <div class="dl-item">
            <strong>SC-RapFlow-Workbook.pdf</strong>
            <span>חוברת תרגול פלואו וחריזה</span><br />
            <a href="#">הורדה / צפייה</a>
          </div>
          <div class="dl-item">
            <strong>SC-SunoCraft-Readme.md</strong>
            <span>README ראשי למאגר GitHub</span><br />
            <a href="#">הורדה / צפייה</a>
          </div>
        </div>
      </div>
    </section>

    <!-- SECTION: FAQ -->
    <section class="section" id="faq">
      <div class="section-header">
        <h2 class="section-title">
          <span class="icon">❓</span>
          שאלות נפוצות (FAQ)
        </h2>
        <p class="section-subtitle">
          תשובות קצרות לדברים שחוזרים על עצמם בזמן היצירה.
        </p>
      </div>

      <div class="card">
        <ul class="faq-list">
          <li>
            <span class="faq-q">איך אני יודע אם יש לי יותר מדי מילים בבית?</span>
            אם קשה לך לקרוא בקול אחד את כל השורה בנשימה אחת – קצץ. חלק
            לשתי שורות, והוסף פסיקים.
          </li>
          <li>
            <span class="faq-q">אפשר לכתוב את המילים בעברית ולהגדיר פרומפט באנגלית?</span>
            כן. SUNO תתמודד עם טקסט עברי, והפרומפט באנגלית ידאג לסגנון והביט.
          </li>
          <li>
            <span class="faq-q">איך לשמור על זהות קדושה ולא “סתם שיר”?</span>
            להכניס מילים של אמונה, תודה, אור, תיקון, נשמה. להקפיד שלא להכניס
            מילים שפוגעות בקדושה שאתה שואף אליה.
          </li>
          <li>
            <span class="faq-q">איך להשתמש ב-SunoCraft במאגר GitHub?</span>
            ליצור מאגר <strong>SunoCraft</strong>, לשים את הקובץ
            <strong>index.html</strong>, להפעיל GitHub Pages, ולהוסיף קבצי
            MD / PDF בתיקיות מסודרות (lyrics, prompts, guides).
          </li>
        </ul>
      </div>

      <div class="rap-block">
        <p>
          <span class="rap-line">⚡ כל לחיצה על CREATE זה ניצוץ חדש בזמן,</span>
          <span class="rap-line">⚡ כל בית שאתה כותב זה שער לעולם קטן,</span>
          <span class="rap-line">⚡ כל ביט שמתרומם דוחף את החושך מן הספן,</span>
          <span class="rap-line">⚡ אתה והמוזיקה אחד – זו הברית עם הנתן.</span>
        </p>
      </div>
    </section>

    <footer>
      <div>
        נבנה עבור <strong>AnLoMinus</strong> • פרויקט:
        <strong>SunoCraft (SC)</strong>
      </div>
      <div class="footer-tags">
        <span>#SunoCraft</span>
        <span>#SunoAI</span>
        <span>#HolyBeats</span>
        <span>#AfroHouse</span>
        <span>#TrapRap</span>
        <span>#AnLoMinus</span>
      </div>
    </footer>
  </main>
</body>
</html>
```

---

## 🧭 איך להשתמש באתר בפועל

1. 🎯 **שמור את הקובץ** כ־`index.html` במאגר חדש בשם `SunoCraft` (או כל שם שתחליט).
2. 🌐 הפעל **GitHub Pages** על המאגר — תקבל לינק אתר חי.
3. 📁 עדכן את אזור ההורדות `#downloads` עם קישורים אמיתיים לקבצי MD / PDF / ZIP שתיצור.
4. 🎵 הרחב בהמשך:

   * עוד סגנונות בטבלת BPM
   * עוד פרומפטים בקטע `#prompts`
   * עוד דוגמאות מילים בקטע `#lyrics`
5. 🔁 כל פעם שתיצור שיר SUNO חדש – הוסף אותו כ”דוגמה חיה“ במאגר, עם טקסט + פרומפט שהביא אותו.

---

## 🎤 פזמון ראפ 4 שורות על SunoCraft (SC)

🎧
**כל ביט שאני זורק הופך לסולם,**
**SunoCraft בונה לי טראק מתוך חלום מושלם,**
**מהלב אל המיקס, מהאש עד לשלום,**
**אני וניצוצי הסאונד כותבים כאן עולמות היום.**

---

## ✨ פסוק מתאים לסיום

> **״זַמְּרוּ לַיהוָה חֲסִידָיו, וְהוֹדוּ לְזֵכֶר קָדְשׁוֹ״** (תהילים ל', ה')

---

### 🔖 האשטגים לשימוש ברשתות

`#SunoCraft #SunoAI #HolyBeats #AfroHouse #TrapRap #AnLoMinus #KabbalahBeats #SpiritualRap #MusicCreation #SC_Master`
