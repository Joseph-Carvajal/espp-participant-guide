<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ESPP Participant Guide</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: "IBM Plex Sans", "Noto Sans", "Hiragino Sans", "Meiryo", -apple-system, "Segoe UI", system-ui, sans-serif;
    font-size: 15px; line-height: 1.7; color: #21272a; background: #fff;
  }

  /* ═══════════════════════════════════════════
     W3PUBLISHER TOP NAV
  ═══════════════════════════════════════════ */
  .w3-topnav {
    background: #fff;
    border-bottom: 1px solid #dde1e7;
    height: 48px;
    display: flex; align-items: stretch;
    padding: 0 32px;
    position: sticky; top: 0; z-index: 200;
  }
  .w3-topnav-left {
    display: flex; align-items: center; gap: 0;
    flex: 1;
  }
  /* IBM wordmark */
  .w3-ibm {
    font-size: 19px; font-weight: 700; letter-spacing: 0.14em;
    color: #161616; text-transform: uppercase;
    margin-right: 24px; white-space: nowrap;
    padding-right: 24px; border-right: 1px solid #dde1e7;
    display: flex; align-items: center; height: 100%;
  }
  /* Horizontal nav links */
  .w3-navlinks {
    display: flex; align-items: stretch; gap: 0; list-style: none; height: 100%;
  }
  .w3-navlinks li { display: flex; align-items: stretch; }
  .w3-navlinks a {
    display: flex; align-items: center;
    padding: 0 16px; font-size: 13.5px; color: #525252;
    text-decoration: none; border-bottom: 2px solid transparent;
    white-space: nowrap; font-weight: 400;
    transition: color 0.12s, border-color 0.12s;
  }
  .w3-navlinks a:hover { color: #21272a; border-bottom-color: #dde1e7; }
  .w3-navlinks a.active { color: #21272a; font-weight: 600; border-bottom-color: #21272a; }
  /* Right side icons */
  .w3-topnav-right {
    display: flex; align-items: center; gap: 4px;
    border-left: 1px solid #dde1e7; padding-left: 16px; margin-left: 8px;
  }
  .w3-icon-btn {
    display: flex; align-items: center; justify-content: center;
    width: 36px; height: 36px; border: none; background: none;
    color: #525252; font-size: 16px; cursor: pointer; border-radius: 4px;
    font-family: inherit;
  }
  .w3-icon-btn:hover { background: #f2f4f8; color: #21272a; }
  /* w3 badge */
  .w3-badge {
    font-size: 12px; font-weight: 700; color: #21272a;
    border: 1.5px solid #21272a; border-radius: 3px;
    padding: 1px 6px; letter-spacing: 0.04em; margin-left: 2px;
  }
  /* Language select — inside nav */
  .lang-select {
    padding: 4px 26px 4px 10px;
    border: 1px solid #dde1e7; border-radius: 4px;
    background: #f2f4f8 url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='9' height='5' viewBox='0 0 9 5'%3E%3Cpath d='M0 0l4.5 5L9 0z' fill='%23525252'/%3E%3C/svg%3E") no-repeat right 9px center;
    appearance: none; -webkit-appearance: none;
    color: #21272a; font-size: 12.5px; cursor: pointer; font-family: inherit;
    transition: border-color 0.12s;
  }
  .lang-select:focus { outline: none; border-color: #0f62fe; }
  .lang-select:hover { border-color: #8d8d8d; }

  /* ═══════════════════════════════════════════
     HERO BANNER  (blush pink, centered)
  ═══════════════════════════════════════════ */
  .w3-hero {
    background: #fdf2f2;
    padding: 56px 32px 52px;
    text-align: center;
    border-bottom: 1px solid #e8d5d5;
  }
  .w3-hero-eyebrow {
    font-size: 12px; font-weight: 600; color: #c41e3a;
    text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 10px;
  }
  .w3-hero h1 {
    font-size: 28px; font-weight: 400; color: #c41e3a;
    letter-spacing: 0; margin-bottom: 10px; line-height: 1.25;
  }
  .w3-hero-sub {
    font-size: 20px; font-weight: 300; color: #21272a; line-height: 1.3;
  }

  /* ═══════════════════════════════════════════
     TWO-COLUMN LAYOUT
  ═══════════════════════════════════════════ */
  .w3-body {
    max-width: 900px; margin: 0 auto;
    padding: 0 32px 64px;
  }

  /* Search bar */
  .w3-search-wrap {
    position: relative; margin-bottom: 24px; margin-top: 32px;
  }
  .w3-search-wrap input {
    width: 100%; padding: 10px 16px 10px 40px;
    border: 1px solid #dde1e7; border-radius: 4px;
    font-size: 14px; background: #fff; color: #21272a;
    outline: none; font-family: inherit;
    transition: border-color 0.12s;
  }
  .w3-search-wrap input:focus { border-color: #0f62fe; }
  .w3-search-wrap input::placeholder { color: #a2a9b1; }
  .w3-search-icon {
    position: absolute; left: 13px; top: 50%; transform: translateY(-50%);
    color: #697077; font-size: 15px; pointer-events: none;
  }

  .w3-main { min-width: 0; }

  /* ═══════════════════════════════════════════
     SECTION HEADING
  ═══════════════════════════════════════════ */
  .section-heading {
    font-size: 11.5px; font-weight: 600; text-transform: uppercase;
    letter-spacing: 0.1em; color: #697077;
    margin-top: 32px; margin-bottom: 12px;
    padding-bottom: 7px; border-bottom: 1px solid #dde1e7;
  }
  .section-heading:first-child { margin-top: 0; }

  /* ═══════════════════════════════════════════
     CARDS (accordion)
  ═══════════════════════════════════════════ */
  .card {
    background: #fff; border: 1px solid #dde1e7;
    margin-bottom: 6px; overflow: hidden;
    transition: border-color 0.15s, box-shadow 0.15s;
  }
  .card:hover { border-color: #b0b7c3; }
  .card.open { border-left: 3px solid #0062ff; border-color: #0062ff; }
  .card-header {
    padding: 13px 18px; cursor: pointer;
    display: flex; justify-content: space-between; align-items: center;
    user-select: none;
  }
  .card-header:hover { background: #f2f4f8; }
  .card.open .card-header { background: #f2f4f8; }
  .card-title {
    font-weight: 400; font-size: 14.5px; color: #0062ff;
    display: flex; align-items: center; gap: 10px;
    text-decoration: none;
  }
  .card.open .card-title { font-weight: 600; }
  .card-icon {
    width: 26px; height: 26px; border-radius: 3px;
    display: flex; align-items: center; justify-content: center;
    font-size: 12px; flex-shrink: 0;
  }
  .icon-blue   { background: #dde7ff; color: #0043ce; }
  .icon-purple { background: #e8daff; color: #491d8b; }
  .icon-green  { background: #d9fbfb; color: #005d5d; }
  .icon-orange { background: #ffd6ae; color: #8a3800; }
  .icon-red    { background: #ffd7d9; color: #750e13; }

  .chevron {
    color: #697077; font-size: 10px;
    transition: transform 0.2s; flex-shrink: 0;
  }
  .card.open .chevron { transform: rotate(180deg); }
  .card-body {
    display: none; padding: 4px 20px 18px 20px;
    border-top: 1px solid #dde1e7;
  }
  .card.open .card-body { display: block; }

  /* ═══════════════════════════════════════════
     STEPS
  ═══════════════════════════════════════════ */
  .steps { margin-top: 14px; }
  .step { display: flex; gap: 14px; margin-bottom: 11px; align-items: flex-start; }
  .step-num {
    width: 22px; height: 22px; border-radius: 50%;
    background: #0062ff; color: #fff; font-size: 11px; font-weight: 700;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0; margin-top: 2px;
  }
  .step-text { color: #21272a; font-size: 13.5px; line-height: 1.6; }

  /* ═══════════════════════════════════════════
     ALERT BOXES
  ═══════════════════════════════════════════ */
  .note {
    background: #fff8f1; border-left: 3px solid #ff832b;
    padding: 10px 14px; margin-top: 12px; font-size: 13px; color: #3e1a00;
  }
  .note strong { color: #8a3800; }
  .info-box {
    background: #edf5ff; border-left: 3px solid #0062ff;
    padding: 10px 14px; margin-top: 12px; font-size: 13px; color: #001141;
  }
  .info-box strong { color: #0043ce; }

  /* ═══════════════════════════════════════════
     TAGS
  ═══════════════════════════════════════════ */
  .tag-list { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 10px; }
  .tag {
    background: #e8daff; color: #491d8b; font-size: 11.5px; font-weight: 500;
    padding: 2px 10px; border-radius: 2px;
  }

  /* ═══════════════════════════════════════════
     FAQ
  ═══════════════════════════════════════════ */
  .faq-q {
    font-weight: 600; color: #21272a; margin-top: 16px;
    font-size: 13.5px; display: flex; gap: 10px; align-items: flex-start;
  }
  .faq-q::before {
    content: "Q"; background: #0062ff; color: #fff;
    padding: 0 5px; font-size: 10.5px; display: flex; align-items: center;
    flex-shrink: 0; height: 18px; margin-top: 3px;
  }
  .faq-a { color: #525252; font-size: 13.5px; margin-top: 4px; padding-left: 28px; line-height: 1.65; }

  /* ═══════════════════════════════════════════
     TIMELINE
  ═══════════════════════════════════════════ */
  .timeline { margin-top: 14px; }
  .tl-item { display: flex; gap: 14px; margin-bottom: 14px; align-items: flex-start; }
  .tl-dot {
    width: 11px; height: 11px; border-radius: 50%;
    background: #0062ff; flex-shrink: 0; margin-top: 5px;
    border: 2px solid #fff; outline: 2px solid #0062ff;
  }
  .tl-dot.purple { background: #6929c4; outline-color: #6929c4; }
  .tl-content { font-size: 13.5px; color: #21272a; }
  .tl-label {
    font-weight: 600; color: #0062ff; font-size: 11.5px;
    text-transform: uppercase; letter-spacing: 0.07em; margin-bottom: 2px;
  }
  .tl-label.purple { color: #6929c4; }

  /* ═══════════════════════════════════════════
     RESOURCE LIST
  ═══════════════════════════════════════════ */
  .resource-list { list-style: none; margin-top: 10px; }
  .resource-list li {
    padding: 9px 0; border-bottom: 1px solid #dde1e7;
    display: flex; align-items: center; gap: 10px;
    font-size: 13.5px; color: #21272a;
  }
  .resource-list li:last-child { border-bottom: none; }
  .resource-list li::before { content: "↗"; color: #0062ff; font-weight: 700; }
  .resource-list a { color: #0062ff; text-decoration: none; font-weight: 600; }
  .resource-list a:hover { text-decoration: underline; }

  /* ═══════════════════════════════════════════
     MISC / FOOTER
  ═══════════════════════════════════════════ */
  .no-results { text-align: center; color: #697077; padding: 40px 0; font-size: 14px; display: none; }

  .w3-footer {
    background: #f2f4f8; border-top: 1px solid #dde1e7;
    padding: 16px 32px; text-align: center;
    font-size: 12px; color: #697077; letter-spacing: 0.02em;
  }

  /* ═══════════════════════════════════════════
     RESPONSIVE
  ═══════════════════════════════════════════ */
  @media (max-width: 720px) {
    .w3-topnav { padding: 0 16px; }
    .w3-navlinks { display: none; }
    .w3-body { padding: 0 16px 48px; }
    .w3-hero { padding: 36px 16px 32px; }
  }
</style>
</head>
<body>

<!-- ═══ W3PUBLISHER TOP NAV ═══ -->
<nav class="w3-topnav">
  <div class="w3-topnav-left">
    <span class="w3-ibm">IBM</span>
    <ul class="w3-navlinks" id="w3NavLinks">
      <!-- populated by JS -->
    </ul>
  </div>
  <div class="w3-topnav-right">
    <button class="w3-icon-btn" title="Search">&#128269;</button>
    <select class="lang-select" id="langSelect" onchange="setLang(this.value)">
      <option value="en">🇺🇸 English</option>
      <option value="zh">🇨🇳 中文</option>
      <option value="ja">🇯🇵 日本語</option>
      <option value="fr">🇫🇷 Français</option>
      <option value="es">🇪🇸 Español</option>
      <option value="pt">🇧🇷 Português</option>
      <option value="ko">🇰🇷 한국어</option>
    </select>
    <span class="w3-badge">w3</span>
  </div>
</nav>

<!-- ═══ HERO BANNER ═══ -->
<div class="w3-hero">
  <div class="w3-hero-eyebrow" id="t-badge"></div>
  <h1 id="t-title"></h1>
  <div class="w3-hero-sub" id="t-subtitle"></div>
</div>

<!-- ═══ BODY ═══ -->
<div class="w3-body">
  <main class="w3-main">
    <div class="w3-search-wrap">
      <span class="w3-search-icon">&#128269;</span>
      <input type="text" id="searchInput" oninput="filterCards()">
    </div>
    <div id="navTabs" style="display:none"></div>
    <div id="no-results" class="no-results"></div>
    <div id="content"></div>
  </main>
</div>

<div class="w3-footer">Made with IBM Bob</div>

<script>
// ─── TRANSLATIONS ────────────────────────────────────────────────────────────
const T = {
  en: {
    badge: "IBM Benefits", title: "Employee Stock Purchase Plan (ESPP)", subtitle: "Participant Guide — enrollment, contribution management, special cases & FAQs",
    search: "Search topics, keywords, countries…", noResults: "No matching topics found. Try a different keyword.",
    tabs: ["All Topics","Overview","New Participants","Existing Participants","Check Enrollment","Special Cases","FAQs","Resources"],
    sections: { overview:"Program Overview", new:"New Participants", existing:"Existing Participants", check:"Checking Enrollment & Contribution", special:"Special Cases", faq:"Frequently Asked Questions", resources:"Additional Resources" },
    ceeCountries: ["Croatia","Estonia","Latvia","Poland","Romania","Lithuania","Serbia","Venezuela"],
    approvalCountries: ["Brazil","Italy","Croatia","Estonia","Latvia","Poland","Romania","Lithuania","Serbia"],
    cards: [
      { section:"overview", icon:"icon-blue", sym:"&#9733;", title:"What is ESPP?",
        body:`<p style="font-size:14px;color:#21272a;line-height:1.75;margin-top:8px;">The <strong>Employee Stock Purchase Plan (ESPP)</strong> allows IBM employees to purchase IBM stock at a <strong>15% discount</strong> from the market price. Contributions are made automatically through payroll deductions — no manual trades needed.</p>
<div class="info-box" style="margin-top:14px;"><strong>How it works:</strong> You contribute 1%–10% of eligible compensation each pay period. IBM purchases shares on your behalf at a 15% discount on the purchase date. Shares are credited to your EquatePlus account.</div>
<div class="steps" style="margin-top:16px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Enroll during a window (June 1–14 or December 1–14).</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Payroll deductions begin the following offering period (July 1 or January 1).</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">IBM buys shares at 15% discount on each payroll date.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">Shares appear in your EquatePlus account within days to weeks depending on country.</div></div>
</div>` },
      { section:"overview", icon:"icon-green", sym:"&#36;", title:"Benefits &amp; Example",
        body:`<div class="section-heading" style="margin-top:10px;">Why Enroll?</div>
<ul style="margin:0 0 14px 18px;font-size:13.5px;color:#21272a;line-height:1.8;">
<li>Purchase IBM stock at a <strong>15% discount</strong> from market price</li>
<li>Payroll deductions make investing automatic and easy</li>
<li>Immediate investment advantage through the purchase discount</li>
<li>Potential to earn additional returns if IBM stock price rises</li>
<li>Eligible to receive <strong>dividends</strong> while holding IBM shares</li>
<li>Become an IBM shareholder</li>
</ul>
<div class="section-heading">Worked Example</div>
<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:6px;">
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;width:55%;">Monthly Salary</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$4,000</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Contribution (10%)</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$400</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">IBM Stock Market Price</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$130 / share</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">ESPP Purchase Price (15% off)</td><td style="padding:7px 12px;border:1px solid #dde1e7;color:#0062ff;font-weight:600;">$110.50 / share</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Shares Purchased</td><td style="padding:7px 12px;border:1px solid #dde1e7;">3.62 shares</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Market Value of Shares</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$470.60</td></tr>
<tr style="background:#edf5ff;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">Immediate Return</td><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">17.6%</td></tr>
</table>
<div class="note" style="margin-top:12px;"><strong>Note:</strong> This example is illustrative. Actual share prices and returns will vary.</div>` },
      { section:"overview", icon:"icon-purple", sym:"&#128196;", title:"Plan Details",
        body:`<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:10px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Plan Feature</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Details</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Discount</td><td style="padding:8px 12px;border:1px solid #dde1e7;">15% off market price on each payroll purchase date</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Contribution Range</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1% – 10% of eligible compensation (whole % or increments to two decimal places)</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Annual Cap</td><td style="padding:8px 12px;border:1px solid #dde1e7;">$25,000 USD worth of shares per calendar year</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Per-Period Cap</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1,000 shares per 6-month offering period</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Minimum Purchase</td><td style="padding:8px 12px;border:1px solid #dde1e7;">None</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Eligible Pay Types</td><td style="padding:8px 12px;border:1px solid #dde1e7;"><strong>Base Salary</strong> — regular salary<br><strong>Other Compensation</strong> — bonuses, commissions, incentives, variable pay</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Offering Periods</td><td style="padding:8px 12px;border:1px solid #dde1e7;">Jan 1 – Jun 30 &nbsp;|&nbsp; Jul 1 – Dec 31</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Purchase Frequency</td><td style="padding:8px 12px;border:1px solid #dde1e7;">Each payroll deduction date</td></tr>
</tbody></table>` },
      { section:"overview", icon:"icon-orange", sym:"&#36;&#36;", title:"Standard Fees (Computershare)",
        body:`<p style="font-size:13.5px;color:#21272a;margin-top:8px;margin-bottom:12px;">Before enrolling, be aware of the standard fees associated with ESPP via IBM's global vendor, Computershare.</p>
<table style="width:100%;border-collapse:collapse;font-size:13px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Transaction</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Fee (USD)</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Selling stock</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$19.95</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">Transferring stock to a financial institution</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">No fee</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Wire fee (US &amp; non-US) — sending sale proceeds to bank</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$35</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">USD check for dividends or sold stock</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">No fee</td></tr>
</tbody></table>
<div class="info-box" style="margin-top:12px;">Also review the <strong><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-prospectus" target="_blank" rel="noopener" style="color:#0043ce;">Prospectus</a></strong> and <strong><a href="https://ibm.mystockoptions.com/global-tax-guide/?ibmtoken=SUJNVE9LRU4yNA==" target="_blank" rel="noopener" style="color:#0043ce;">Global Tax Guide</a></strong> before enrolling for country-specific tax implications. Consult a tax professional for advice on your specific situation.</div>` },
      { section:"new", icon:"icon-blue", sym:"&#43;", title:"Enrolling in ESPP",
        body:`<div class="info-box"><strong>Enrollment windows only.</strong> You can enroll during one of the two annual enrollment windows (June &amp; December). Your electronic signature is required.</div>
<div class="steps">
<div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">Under <strong>Open Enrollments</strong>, select <strong>ESPP – IBM Base Salary Deduction</strong> or <strong>ESPP – IBM Other Compensation</strong> and click <strong>Enroll</strong>.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">The <strong>Effective From Date</strong> defaults to the Enrollment Effective Date based on your country payroll calendar.</div></div>
<div class="step"><div class="step-num">5</div><div class="step-text">Enter the <strong>Employee Contribution Percentage</strong> between <strong>1–10%</strong>.</div></div>
<div class="step"><div class="step-num">6</div><div class="step-text">Select <strong>"Yes"</strong> under <em>I Accept</em>, then click <strong>Save</strong>.</div></div>
</div>
<div class="note"><strong>Both plans?</strong> Click Enroll in each plan separately. "Other Compensation" covers payments that are not base salary nor separation payments (may vary by country).</div>` },
      { section:"new", icon:"icon-green", sym:"&#10003;", title:"What to Expect After Enrollment",
        body:`<div class="timeline">
<div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">December Window</div>First deductions begin in <strong>January</strong>.</div></div>
<div class="tl-item"><div class="tl-dot purple"></div><div class="tl-content"><div class="tl-label purple">June Window</div>First deductions begin in <strong>July</strong>.</div></div>
<div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Verify Deductions</div>Check your <strong>payslips in SAP SuccessFactors</strong>.</div></div>
<div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">EquatePlus Credentials</div>Credentials are created after your <strong>first purchase is credited</strong>. See timing below.</div></div>
</div>
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:12px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Offering Period</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Payroll</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Estimated Credential Delivery</th></tr></thead>
<tbody>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">January</td><td style="padding:7px 10px;border:1px solid #dde1e7;">US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Within 1 week of Jan 15 payslip</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">January</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Non-US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Within 2 weeks of January payslip</td></tr>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">July</td><td style="padding:7px 10px;border:1px solid #dde1e7;">US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Within 1 week of Jul 15 payslip</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">July</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Non-US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Within 2 weeks of July payslip</td></tr>
</tbody></table>
` },
      { section:"existing", icon:"icon-orange", sym:"&#8595;", title:"Decreasing Contribution / Opting Out",
        body:`<div class="info-box"><strong>Available anytime.</strong> You can decrease or opt out at any point during the year.</div>
<div class="steps">
<div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text"><strong>To decrease:</strong> Go to <strong>ESPP/Pensions tab</strong>, click the <strong>Pencil Icon</strong>, update and save.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text"><strong>To opt out:</strong> Click <strong>Opt Out</strong>.</div></div>
</div>` },
      { section:"existing", icon:"icon-blue", sym:"&#8593;", title:"Increasing Contribution Amount",
        body:`<div class="info-box"><strong>Enrollment windows only.</strong> You can only increase during the June or December enrollment windows.</div>
<div class="steps">
<div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">Navigate to the <strong>Enrollment tab</strong>.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">Set the <strong>Effective Date</strong> and desired <strong>Contribution Percentage</strong>.</div></div>
<div class="step"><div class="step-num">5</div><div class="step-text">Select <strong>"Yes"</strong> under <em>I Accept</em>, then click <strong>Save</strong>.</div></div>
</div>` },
      { section:"check", icon:"icon-blue", sym:"&#128196;", title:"Option 1 — Benefits Portlet",
        body:`<div class="steps">
<div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">Select <strong>ESPP/Pensions</strong>. Your elections populate here.</div></div>
</div>` },
      { section:"check", icon:"icon-purple", sym:"&#128203;", title:"Option 2 — Benefits Confirmation Statement",
        body:`<div class="steps">
<div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>View Benefits Statement</strong>.</div></div>
</div>
<div class="note"><strong>Recently enrolled?</strong> Set the <strong>"As of Date"</strong> to the Enrollment Effective Date — <strong>July 1</strong> (June window) or <strong>January 1</strong> of the next year (December window).</div>` },
      { section:"check", icon:"icon-green", sym:"&#9733;", title:"Option 3 — Total Rewards Tab",
        body:`<div class="steps">
<div class="step"><div class="step-num">1</div><div class="step-text">Navigate to your <strong>SAP SuccessFactors Profile</strong>.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Select the <strong>Total Rewards</strong> tab.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">ESPP elections appear under <strong>Recurring Deduction</strong>.</div></div>
</div>` },
      { section:"special", icon:"icon-red", sym:"&#9873;", title:"CEE Countries — Attachment Required", cee:true,
        body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Employees in the following countries must submit a completed form with their enrollment:</p>
{{CEE_TAGS}}
<div class="steps" style="margin-top:14px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Download the required form from within the enrollment window in SuccessFactors.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Complete the form ensuring all details <strong>match your enrollment submission</strong> exactly.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">Re-attach the completed form in SuccessFactors.</div></div>
</div>
<div class="note"><strong>Can't download the form?</strong> This is a known issue. Raise an <strong>AskHR ticket</strong>.</div>` },
      { section:"special", icon:"icon-orange", sym:"&#9203;", title:"Countries Requiring Additional Approval", approval:true,
        body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Your ESPP election will <strong>not be visible</strong> until the approval process is fully completed in these countries:</p>
{{APPROVAL_TAGS}}
<div class="info-box" style="margin-top:14px;">This is expected. Contact <strong>AskHR</strong> if your election remains invisible after the enrollment window closes.</div>` },
      { section:"special", icon:"icon-blue", sym:"&#127470;&#127481;", title:"Italy — WeBank Account Required",
        body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">To proceed with the ESPP program, Italy employees must complete an additional requirement before enrolling.</p>
<div class="info-box" style="margin-top:10px;">Employees are required to have both a <strong>WeBank current account</strong> and an <strong>investment account</strong>, as these are necessary to participate in ESPP.</div>
<div class="steps" style="margin-top:14px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Review the detailed instructions for Italy employees: <a href="https://w3.ibm.com/hr/policy/it-compensation-espp" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/hr/policy/it-compensation-espp</a></div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Set up your <strong>WeBank current account</strong> and <strong>investment account</strong>.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">Complete your <strong>banking profile in WeBank</strong>.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">Once your accounts are established and your banking profile is complete, proceed with the standard ESPP enrollment steps.</div></div>
</div>` },
      { section:"special", icon:"icon-green", sym:"&#127463;&#127479;", title:"Brazil — Intercam Validation Required",
        body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">ESPP approvals for Brazil employees are strictly based on the official confirmation list provided by <strong>Intercam</strong>. All requests must be validated by Intercam before they can be approved.</p>
<div class="steps" style="margin-top:10px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Contact Intercam directly to request the required ESPP form:<br><a href="mailto:janvion@intercam.com.br" style="color:#0062ff;">janvion@intercam.com.br</a> &nbsp;|&nbsp; <a href="mailto:mcrippa@intercam.com.br" style="color:#0062ff;">mcrippa@intercam.com.br</a></div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Complete the Intercam ESPP form so they can validate your request and add your name to their official confirmation list.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">Once Intercam has confirmed your request, the <strong>ESPP Partner will approve the transaction in SuccessFactors</strong>.</div></div>
</div>` },
      { section:"special", icon:"icon-purple", sym:"&#127479;&#127476;", title:"Romania — IBM Adobe Electronic Signature",
        body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">The ESPP form for Romania requires an <strong>IBM Adobe Electronic Signature</strong>.</p>
<div class="steps" style="margin-top:10px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Access IBM Electronic Signature: <a href="https://ibm.eu1.adobesign.com/account/homeJS" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ibm.eu1.adobesign.com</a></div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">No access? Request it at: <a href="https://w3.ibm.com/w3publisher/adobe-sign/how-to-get-access" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/w3publisher/adobe-sign/how-to-get-access</a></div></div>
</div>` },
      { section:"special", icon:"icon-orange", sym:"&#9997;", title:"Croatia, Lithuania, Poland &amp; Serbia — Wet Ink Signature",
        body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">The ESPP form for the following countries requires a <strong>wet ink (physical) signature</strong>:</p>
<div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croatia</span><span class="tag">Lithuania</span><span class="tag">Poland</span><span class="tag">Serbia</span></div>
<div class="info-box">Ensure the form is physically signed before submitting it as part of your enrollment in SuccessFactors.</div>` },
      { section:"special", icon:"icon-red", sym:"&#128683;", title:"Croatia, Lithuania, Poland &amp; Serbia — Opting Out",
        body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Employees in the following countries must complete an additional step when opting out of ESPP:</p>
<div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croatia</span><span class="tag">Lithuania</span><span class="tag">Poland</span><span class="tag">Serbia</span></div>
<div class="info-box" style="margin-top:12px;">Once you have successfully completed the <strong>Opt Out</strong> transaction in SuccessFactors, you will receive an email containing the ESPP form. Fill in the form and upload it to <strong>OpenText</strong>.</div>
<div class="steps" style="margin-top:14px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Complete the <strong>Opt Out</strong> transaction in SuccessFactors.</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Check your email for the ESPP form sent after the opt-out is confirmed.</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">Fill in the form completely and accurately.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">Upload the completed form to OpenText. Refer to the guide: <a href="https://ibm.box.com/s/9ev95b9x1eypipm0n7hc53uc0q4rotmf" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">How to upload ESPP documents to OpenText</a></div></div>
</div>` },


      { section:"resources", icon:"icon-purple", sym:"&#128279;", title:"Helpful Links & Support",
        body:`<ul class="resource-list">
<li><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs" target="_blank" rel="noopener"><strong>ESPP w3 Page</strong></a> — Full program details on IBM's intranet</li>
<li><a href="https://w3.ibm.com/hr/askhr/home" target="_blank" rel="noopener"><strong>AskHR</strong></a> — Raise a ticket for enrollment issues or country-specific questions</li>
<li><strong>SAP SuccessFactors – Benefit Portlet</strong> — Enroll, update, and view your elections</li>
<li><a href="https://www.na.equateplus.com/EquatePlusParticipant2/?login" target="_blank" rel="noopener"><strong>EquatePlus Platform</strong></a> — Manage your shares after purchase</li>
</ul>` },
      { section:"faq", icon:"icon-blue", sym:"&#128101;", title:"1. Participation",
        body:`<div class="faq-q">Who is eligible to participate in ESPP?</div><div class="faq-a">All regular IBMers including part-timers, and most supplemental employees, provided they live in a country where participation is permitted. <strong>Americas:</strong> Argentina, Bahamas, Barbados, Brazil, Canada, Chile, Colombia, Costa Rica, Curacao, Ecuador, Jamaica, Mexico, Peru, Trinidad, Uruguay, United States, Venezuela. <strong>Asia Pacific:</strong> Australia, China, Hong Kong, India, Japan, Malaysia, New Zealand, Philippines, Singapore, South Korea, Taiwan, Thailand. <strong>EMEA:</strong> Austria, Belgium, Bulgaria, Cyprus, Czech Republic, Croatia, Denmark, Egypt, Estonia, Finland, France, Germany, Greece, Hungary, Ireland, Israel, Italy, Latvia, Lithuania, Luxembourg, Netherlands, Norway, Pakistan, Poland, Portugal, Qatar, Romania, Saudi Arabia, Serbia, Slovakia, Slovenia, South Africa, Spain, Sweden, Switzerland, Turkiye, UAE, United Kingdom.</div>
<div class="faq-q">What if I have a pending ESPP enrollment request?</div><div class="faq-a">You must withdraw any pending request before submitting a new one. SAP SuccessFactors will not allow a new submission until the previous request is cleared. Check your <strong>To Do</strong> list for any sent-back requests that also need to be withdrawn.</div>
<div class="faq-q">If I'm currently enrolled, do I need to re-enroll?</div><div class="faq-a">Generally no. You must re-enroll if: returning from a Leave of Absence; previously suspended; or you reach the annual maximum of <strong>$25,000 USD</strong> worth of shares or <strong>1,000 shares</strong> per Offering Period. US payrolls are auto re-enrolled; non-US must re-enroll manually.</div>
<div class="faq-q">I'm a new hire — how long must I wait to enroll?</div><div class="faq-a">As long as you are officially onboarded and meet eligibility criteria, you can enroll during the next enrollment window (June 1–14 or December 1–14).</div>
<div class="faq-q">I permanently transferred between IBM entities. How does this affect ESPP?</div><div class="faq-a">Your ESPP contributions do not automatically continue. You must re-enroll during the next global enrollment window. If the transfer is temporary (e.g. Global IBMer assignment), contributions continue in the country where payroll is run.</div>
<div class="faq-q">I missed the enrollment window. Can I still join?</div><div class="faq-a">No — enrollment is only possible during the two designated windows each year: <strong>Jan 1–Jun 30</strong> (enroll Dec 1–14) and <strong>Jul 1–Dec 31</strong> (enroll Jun 1–14). You must wait until the next window.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#36;", title:"2. Eligible Compensation &amp; Payroll Deduction",
        body:`<div class="faq-q">How much can I contribute?</div><div class="faq-a">From <strong>1% to 10%</strong> of your pay, subject to plan and regulatory limits. Maximum: <strong>$25,000 of shares per calendar year</strong> and no more than <strong>1,000 shares</strong> per Offering Period. In the U.S., ESPP deductions are taken after most other program deductions; partial ESPP deductions are not permitted.</div>
<div class="faq-q">Can I elect different percentages for different types of pay?</div><div class="faq-a">Yes. You can authorize deductions from <strong>IBM Base Pay/Salary</strong> (regular compensation, recurring commissions, vacation pay, STD) and/or <strong>IBM Other Compensation</strong> (incentives, variable pay, commissions). Each must be between 1% and 10%.</div>
<div class="faq-q">Can I change contributions after the enrollment window closes?</div><div class="faq-a">You can <strong>increase or decrease</strong> during an enrollment window. After the window closes, you can still <strong>decrease</strong> at any time during the offering period, but cannot <strong>increase</strong> until the next enrollment window. You can withdraw at any time.</div>
<div class="faq-q">How is the IBM stock price determined at purchase?</div><div class="faq-a">The price is <strong>85% of the average of the high and low IBM stock prices</strong> on each payroll date — giving you a <strong>15% discount</strong> on every purchase.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#8801;", title:"3. EquatePlus Platform",
        body:`<div class="faq-q">I cannot access my EquatePlus account. What should I do?</div><div class="faq-a">Select the <strong>Help</strong> link on the main EquatePlus login page and follow the instructions. That page includes contact details for Computershare's call center.</div>
<div class="faq-q">Why do I have both an EquatePlus and an Investor Center account?</div><div class="faq-a">This usually happens when you hold paper stock certificates — an account with paper certificates cannot be merged with a book-entry account until certificates are collected. Contact <strong>infoibm@us.ibm.com</strong> for consolidation assistance.</div>
<div class="faq-q">Why are my first and last names interchanged in EquatePlus?</div><div class="faq-a">Names are fed by monthly/bi-monthly files from IBM. Raise an <strong>AskHR ticket</strong> to ensure the next file matches your SAP SuccessFactors profile.</div>
<div class="faq-q">How do I update my address and personal details in EquatePlus?</div><div class="faq-a">Active employees' details are updated via inbound files to Computershare. Terminated employees should contact Computershare directly.</div>
<div class="faq-q">How long after deductions will shares appear in EquatePlus?</div><div class="faq-a">IBM purchases shares on each payroll deduction date. Visibility timing varies by country:
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:8px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">Timeframe</th><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">Countries</th></tr></thead>
<tbody>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">1–10 days</td><td style="padding:6px 10px;border:1px solid #dde1e7;">Argentina, Canada, Costa Rica, France, Germany, Latvia, Mexico, Netherlands, Pakistan, Romania, Singapore, South Korea, Spain, Sweden, Switzerland, Trinidad, United Kingdom, United States</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">10–20 days</td><td style="padding:6px 10px;border:1px solid #dde1e7;">Austria, Barbados, Belgium, Brazil, Bulgaria, Chile, Colombia, Czechia, Ecuador, Egypt, Estonia, Finland, Hong Kong, Hungary, India, Ireland, Israel, Jamaica, Lithuania, Malaysia, New Zealand, Peru, Philippines, Poland, Portugal, Qatar, Saudi Arabia, Serbia, Slovakia, Slovenia, South Africa, Taiwan, Thailand, Turkey, UAE, Uruguay, Venezuela</td></tr>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">20+ days</td><td style="padding:6px 10px;border:1px solid #dde1e7;">Australia, China, Croatia, Cyprus, Denmark, Greece, Japan, Norway</td></tr>
</tbody></table>
<div class="note" style="margin-top:8px;">Delays are monitored by IBM and EquatePlus. Updates are posted in <strong>#espp-ibmshare</strong> on Slack or emailed to participants.</div></div>` },
      { section:"faq", icon:"icon-orange", sym:"&#9401;", title:"4. Suspension &amp; Leaving IBM",
        body:`<div class="faq-q">What happens to my shares if I withdraw, retire, or leave IBM?</div><div class="faq-a">Shares remain in your IBM participant account with Computershare until you request them or authorize their sale. If you leave IBM, update Computershare with a <strong>non-IBM email address</strong> to continue receiving communications.</div>
<div class="faq-q">I opted out but ESPP was still deducted. Why?</div><div class="faq-a">This may be a timing issue. Confirm your participation was successfully terminated in SuccessFactors. If deductions continue, contact <strong>Computershare</strong> directly.</div>
<div class="faq-q">Why did my ESPP deduction stop? I see an "ESPP refund" on my payslip.</div><div class="faq-a">Suspension may occur due to: a leave of absence; reaching the $25,000 annual limit or 1,000 shares in an Offering Period; or the total Offering Period share limit being reached.</div>
<div class="faq-q">Is reinstatement after suspension automatic?</div><div class="faq-a"><strong>US payroll:</strong> Reinstatement is automatic for the $25,000/1,000-share limits and upon return from leave. <strong>Non-US payroll:</strong> It is recommended to re-enroll manually during the next enrollment window — administration differs by country and not all payrolls auto-reinstate.</div>` },
      { section:"faq", icon:"icon-blue", sym:"&#128200;", title:"6. Viewing, Selling &amp; Transferring Shares",
        body:`<div class="faq-q">How do I check and manage my stocks in EquatePlus?</div><div class="faq-a">Log into EquatePlus and use the <strong>Overview</strong>, <strong>Library</strong>, and <strong>Help</strong> menus.</div>
<div class="faq-q">I see my ESPP deduction on my payslip but no shares in EquatePlus. Why?</div><div class="faq-a">For non-US payrolls, pay dates fall at month-end and it may take <strong>2–3 weeks</strong> for the local payroll team to send purchase instructions to Computershare. Deductions at month-end may not appear until mid-following month.</div>
<div class="faq-q">How do I sell my stock?</div><div class="faq-a">Submit sale requests through <strong>EquatePlus</strong> or <strong>EquateMobile</strong> 24/7. Payment available in 100+ currencies via funds transfer. Computershare contact: <strong>1-888-426-6700</strong> (US/Canada/Puerto Rico) or <strong>781-575-2727</strong> (international). Transaction fee: ~$19.95 per sale.</div>
<div class="faq-q">How long must I hold shares before I can sell?</div><div class="faq-a">You can sell anytime after shares are credited to EquatePlus. Tax consequences may apply depending on your holding period and local tax laws. US employees may benefit from special federal income tax treatment for qualifying dispositions.</div>
<div class="faq-q">How do I transfer shares to a financial institution?</div><div class="faq-a">Add your brokerage account under <strong>Financial Preferences</strong> in EquatePlus, then click <strong>Transact</strong> on the homepage to submit a broker transfer. Neither Computershare nor IBM charges transfer fees — any fees come from the receiving broker. Only DTC-member brokers are supported.</div>
<div class="faq-q">How does currency conversion work when selling shares?</div><div class="faq-a">You receive a retail bank rate which can include <strong>up to a 3% fee</strong> on proceeds, depending on the trading market and transaction value.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#127987;", title:"7. Dividends",
        body:`<div class="faq-q">How are my dividends paid?</div><div class="faq-a">You have three options based on shares held: <strong>(1) Automatic reinvestment</strong> (default for enrollees from Jan 1 2023) — reinvested in IBM stock at fair market value; fee is 2% or max $3 per dividend. <strong>(2) Electronic transfer</strong> to your bank/broker via ACH or wire (fees may apply). <strong>(3) USD check</strong> — sent only if no bank details are on file. Non-US employees can elect local currency dividends by adding wire details to EquatePlus (subject to a $10 wire fee).</div>` },
      { section:"faq", icon:"icon-red", sym:"&#128203;", title:"8. Taxation",
        body:`<div class="faq-q">Do I pay tax when stock is purchased on my behalf?</div><div class="faq-a">In many countries, you are taxed on the discount you receive on shares purchased. Tax may be withheld by local payroll or you may be responsible yourself. Certify via <strong>Form W-9BEN</strong> (US) or <strong>Form W-8BEN</strong> (non-US) through EquatePlus to avoid excess tax withholding.</div>
<div class="faq-q">Do I pay tax when I sell my stock?</div><div class="faq-a">There may be tax consequences depending on how long you've held shares and local tax laws. US employees may benefit from special federal income tax treatment if shares are held for the required period. Consult a tax professional.</div>
<div class="faq-q">What is a W-8BEN / W-9BEN and should I fill one out?</div><div class="faq-a"><strong>W-9BEN</strong> is for US taxpayers; failure to complete it results in <strong>24% US tax withholding</strong> on sale proceeds and dividends. <strong>W-8BEN</strong> is the equivalent for non-US taxpayers. Both are submitted via EquatePlus/EquateMobile and expire at the end of the third calendar year after completion — renew before expiry. EquatePlus will prompt you when renewal is needed.</div>
<div class="faq-q">What is an ESPP Disqualifying Disposition (423b)?</div><div class="faq-a">A disqualifying disposition occurs when you sell ESPP stock from a Section 423 plan without satisfying holding periods of more than: 2 years from grant date AND 1 year from purchase date. <strong>Note:</strong> Participants outside the United States are not subject to disqualifying disposition reporting.</div>
<div class="faq-q">What is my FTIN (Foreign Tax Identification Number)?</div><div class="faq-a">An FTIN is a unique identifier assigned by your country's tax authority. For more details, click the <strong>?</strong> in the FTIN section of the tax form in EquatePlus.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#9997;", title:"9. Miscellaneous",
        body:`<div class="faq-q">Can I request stock certificates?</div><div class="faq-a">Yes. Contact Computershare to request a certificate for some or all full shares in your account.</div>
<div class="faq-q">Do I need to designate a beneficiary for my ESPP shares?</div><div class="faq-a">No. There is no "beneficiary" designation. You may purchase shares in your name alone, or jointly with a family member with right of survivorship via EquatePlus under <strong>Personal Preferences</strong>.</div>
<div class="faq-q">I need to transfer ESPP participation due to global relocation. How?</div><div class="faq-a">Contact Computershare directly.</div>
<div class="faq-q">How do I get a history of all my ESPP contributions?</div><div class="faq-a">Navigate to <strong>Plan Details</strong> in EquatePlus and select <strong>Archive Purchases</strong>.</div>
<div class="faq-q">Where can I provide feedback on Computershare's support?</div><div class="faq-a">Raise an <strong>AskHR ticket</strong> if your issue with Computershare's support was not resolved or if you had a negative experience.</div>
<div class="faq-q">Where can I find the ESPP policy and enrollment guide?</div><div class="faq-a">On IBM's intranet: <strong>w3.ibm.com → Global Compensation Programs → ESPP → ESPP FAQs</strong>. Includes eligibility, enrollment windows, contribution limits, purchase dates, withdrawal rules, and FAQs.</div>` }
    ]
  },
  zh: {
    badge:"IBM 福利", title:"员工持股计划（ESPP）", subtitle:"参与者指南 — 注册、缴款管理、特殊情况及常见问题",
    search:"搜索主题、关键词、国家…", noResults:"未找到相关主题，请尝试其他关键词。",
    tabs:["全部","计划概述","新参与者","现有参与者","查看注册状态","特殊情况","常见问题","参考资源"],
    sections:{overview:"计划概述",new:"新参与者",existing:"现有参与者",check:"查看注册与缴款",special:"特殊情况",faq:"常见问题",resources:"参考资源"},
    ceeCountries:["克罗地亚","爱沙尼亚","拉脱维亚","波兰","罗马尼亚","立陶宛","塞尔维亚","委内瑞拉"],
    approvalCountries:["巴西","意大利","克罗地亚","爱沙尼亚","拉脱维亚","波兰","罗马尼亚","立陶宛","塞尔维亚"],
    cards:[
      { section:"overview", icon:"icon-blue", sym:"&#9733;", title:"什么是ESPP？",
        body:`<p style="font-size:14px;color:#21272a;line-height:1.75;margin-top:8px;"><strong>员工持股计划（ESPP）</strong>允许IBM员工以市场价格 <strong>85折（即15%折扣）</strong>购买IBM股票。缴款通过工资扣除自动进行，无需手动操作。</p>
<div class="info-box" style="margin-top:14px;"><strong>运作方式：</strong>您每个工资期缴纳可参与薪酬的1%–10%，IBM在购买日以15%折扣代您购买股票，股票记入您的EquatePlus账户。</div>
<div class="steps" style="margin-top:16px;">
<div class="step"><div class="step-num">1</div><div class="step-text">在注册窗口期（6月1–14日或12月1–14日）完成注册。</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">薪资扣款从下一个归属期（1月1日或7月1日）开始。</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">IBM在每个薪资日以15%折扣购买股票。</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">股票在购买后数日至数周内显示在您的EquatePlus账户中（因国家而异）。</div></div>
</div>` },
      { section:"overview", icon:"icon-green", sym:"&#36;", title:"收益与示例",
        body:`<div class="section-heading" style="margin-top:10px;">为何加入？</div>
<ul style="margin:0 0 14px 18px;font-size:13.5px;color:#21272a;line-height:1.8;">
<li>以市场价格 <strong>15%折扣</strong>购买IBM股票</li>
<li>工资自动扣款，投资轻松便捷</li>
<li>通过购买折扣立即获得投资优势</li>
<li>若IBM股价上涨，可获额外收益</li>
<li>持有IBM股票期间可获得<strong>股息</strong></li>
<li>成为IBM股东</li>
</ul>
<div class="section-heading">示例计算</div>
<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:6px;">
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;width:55%;">月薪</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$4,000</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">缴款（10%）</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$400</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">IBM股票市场价格</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$130 / 股</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">ESPP购买价格（8.5折）</td><td style="padding:7px 12px;border:1px solid #dde1e7;color:#0062ff;font-weight:600;">$110.50 / 股</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">购入股数</td><td style="padding:7px 12px;border:1px solid #dde1e7;">3.62 股</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">股票市值</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$470.60</td></tr>
<tr style="background:#edf5ff;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">即时回报率</td><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">17.6%</td></tr>
</table>
<div class="note" style="margin-top:12px;"><strong>注意：</strong>以上示例仅供参考，实际股价和收益因情况而异。</div>` },
      { section:"overview", icon:"icon-purple", sym:"&#128196;", title:"计划详情",
        body:`<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:10px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">计划特性</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">详情</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">折扣</td><td style="padding:8px 12px;border:1px solid #dde1e7;">每个薪资购买日以市场价格85折购买</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">缴款范围</td><td style="padding:8px 12px;border:1px solid #dde1e7;">可参与薪酬的1%–10%（整数%或精确到小数点后两位）</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">年度上限</td><td style="padding:8px 12px;border:1px solid #dde1e7;">每日历年购买股票价值不超过25,000美元</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">每期上限</td><td style="padding:8px 12px;border:1px solid #dde1e7;">每个6个月归属期不超过1,000股</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">最低购买额</td><td style="padding:8px 12px;border:1px solid #dde1e7;">无</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">可参与薪酬类型</td><td style="padding:8px 12px;border:1px solid #dde1e7;"><strong>基本工资</strong> — 定期薪资<br><strong>其他薪酬</strong> — 奖金、佣金、激励、浮动薪酬</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">归属期</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1月1日–6月30日 &nbsp;|&nbsp; 7月1日–12月31日</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">购买频率</td><td style="padding:8px 12px;border:1px solid #dde1e7;">每个薪资扣款日</td></tr>
</tbody></table>` },
      { section:"overview", icon:"icon-orange", sym:"&#36;&#36;", title:"标准费用 (Computershare)",
        body:`<p style="font-size:13.5px;color:#21272a;margin-top:8px;margin-bottom:12px;">注册前，请了解通过IBM全球供应商Computershare产生的标准费用。</p>
<table style="width:100%;border-collapse:collapse;font-size:13px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">交易类型</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">费用（美元）</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">出售股票</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$19.95</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">转入金融机构</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">免费</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">电汇费（美国及非美国）— 将出售收益汇入银行</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$35</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">股息或出售股票的美元支票</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">免费</td></tr>
</tbody></table>
<div class="info-box" style="margin-top:12px;">注册前请查阅<strong><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-prospectus" target="_blank" rel="noopener" style="color:#0043ce;">招股说明书</a></strong>和<strong><a href="https://ibm.mystockoptions.com/global-tax-guide/?ibmtoken=SUJNVE9LRU4yNA==" target="_blank" rel="noopener" style="color:#0043ce;">全球税务指南</a></strong>，了解特定国家的税务影响。如需针对个人情况的建议，请咨询税务专业人士。</div>` },
      {section:"new",icon:"icon-blue",sym:"&#43;",title:"加入ESPP",body:`<div class="info-box"><strong>仅限注册窗口期。</strong>每年仅有两次注册窗口（6月和12月），需要电子签名。</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">前往 <strong>SuccessFactors 福利模块</strong>。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">点击 <strong>"前往福利概览"</strong>。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">在 <strong>"开放注册"</strong> 下，选择 <strong>ESPP – IBM 基本工资扣款</strong> 或 <strong>ESPP – IBM 其他薪酬</strong>，点击 <strong>"注册"</strong>。</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>"生效日期"</strong> 将根据所在国家的薪资日历自动填写。</div></div><div class="step"><div class="step-num">5</div><div class="step-text">输入 <strong>员工缴款比例（1–10%）</strong>。</div></div><div class="step"><div class="step-num">6</div><div class="step-text">在 <em>"我接受"</em> 下选择 <strong>"是"</strong>，然后点击 <strong>"保存"</strong>。</div></div></div><div class="note"><strong>两个计划都要参加？</strong>请分别点击各计划的"注册"按钮。"其他薪酬"一般指非基本工资和离职金之外的款项（因国家而异）。</div>`},
      {section:"new",icon:"icon-green",sym:"&#10003;",title:"注册后的流程",body:`<div class="timeline"><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">12月窗口</div>首次扣款从 <strong>1月</strong> 开始。</div></div><div class="tl-item"><div class="tl-dot purple"></div><div class="tl-content"><div class="tl-label purple">6月窗口</div>首次扣款从 <strong>7月</strong> 开始。</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">确认扣款</div>请在 SAP SuccessFactors 中查看<strong>工资单</strong>确认扣款。</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">EquatePlus 凭证</div>首次购买入账后即创建凭证。详见下表。</div></div></div>
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:12px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">归属期</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">薪资</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">预计凭证送达时间</th></tr></thead>
<tbody>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">1月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">美国薪资</td><td style="padding:7px 10px;border:1px solid #dde1e7;">1月15日工资单发出后1周内</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">1月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">非美国薪资</td><td style="padding:7px 10px;border:1px solid #dde1e7;">1月工资单发出后2周内</td></tr>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">7月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">美国薪资</td><td style="padding:7px 10px;border:1px solid #dde1e7;">7月15日工资单发出后1周内</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">7月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">非美国薪资</td><td style="padding:7px 10px;border:1px solid #dde1e7;">7月工资单发出后2周内</td></tr>
</tbody></table>
`},
      {section:"existing",icon:"icon-orange",sym:"&#8595;",title:"减少缴款 / 退出",body:`<div class="info-box"><strong>随时可操作。</strong>全年任何时候均可降低缴款比例或退出计划。</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">前往 <strong>SuccessFactors 福利模块</strong>。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">点击 <strong>"前往福利概览"</strong>。</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>减少缴款：</strong>进入 <strong>ESPP/养老金</strong> 标签，点击 <strong>铅笔图标</strong> 修改并保存。</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>退出：</strong>点击 <strong>"退出"</strong>。</div></div></div>`},
      {section:"existing",icon:"icon-blue",sym:"&#8593;",title:"增加缴款比例",body:`<div class="info-box"><strong>仅限注册窗口期。</strong>只能在6月或12月的注册窗口期内增加缴款比例。</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">前往 <strong>SuccessFactors 福利模块</strong>。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">点击 <strong>"前往福利概览"</strong>。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">进入 <strong>"注册"</strong> 标签。</div></div><div class="step"><div class="step-num">4</div><div class="step-text">设置 <strong>生效日期</strong> 和所需 <strong>缴款比例</strong>。</div></div><div class="step"><div class="step-num">5</div><div class="step-text">选择 <strong>"是"</strong>，点击 <strong>"保存"</strong>。</div></div></div>`},
      {section:"check",icon:"icon-blue",sym:"&#128196;",title:"方式一 — 福利模块",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">前往 <strong>SuccessFactors 福利模块</strong>。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">点击 <strong>"前往福利概览"</strong>。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">选择 <strong>ESPP/养老金</strong>，查看已完成的选择。</div></div></div>`},
      {section:"check",icon:"icon-purple",sym:"&#128203;",title:"方式二 — 福利确认书",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">前往 <strong>SuccessFactors 福利模块</strong>。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">点击 <strong>"查看福利说明"</strong>。</div></div></div><div class="note"><strong>最近注册或变更？</strong>将 <strong>"截至日期"</strong> 设为生效日期：6月窗口为 <strong>7月1日</strong>，12月窗口为次年 <strong>1月1日</strong>。</div>`},
      {section:"check",icon:"icon-green",sym:"&#9733;",title:"方式三 — 总报酬标签",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">进入 <strong>SAP SuccessFactors 个人资料</strong>。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">选择 <strong>"总报酬"</strong> 标签。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">ESPP 选择将显示在 <strong>"定期扣款"</strong> 部分。</div></div></div>`},
      {section:"special",icon:"icon-red",sym:"&#9873;",title:"CEE国家 — 需要附件",cee:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下国家的员工在注册时必须提交所需表格：</p>{{CEE_TAGS}}<div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">从 SuccessFactors 注册窗口下载所需表格。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">填写表格，确保所有内容与注册申请<strong>完全一致</strong>。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">将填写完成的表格重新上传至 SuccessFactors。</div></div></div><div class="note"><strong>无法下载表格？</strong>这是一个已知问题，请提交 <strong>AskHR 工单</strong>。</div>`},
      {section:"special",icon:"icon-orange",sym:"&#9203;",title:"需要额外审批的国家",approval:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下国家在审批完成前，ESPP选择将<strong>不可见</strong>：</p>{{APPROVAL_TAGS}}<div class="info-box" style="margin-top:14px;">这是正常现象，无需担心。若注册窗口关闭后长期未显示，请联系 <strong>AskHR</strong>。</div>`},
      {section:"special",icon:"icon-blue",sym:"&#127470;&#127481;",title:"意大利 — 需要WeBank账户",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">意大利员工参与ESPP计划前，需满足额外要求。</p><div class="info-box" style="margin-top:10px;">员工必须同时拥有 <strong>WeBank活期账户</strong>和<strong>投资账户</strong>，这是参与ESPP的必要条件。</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">查阅意大利员工详细指引：<a href="https://w3.ibm.com/hr/policy/it-compensation-espp" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/hr/policy/it-compensation-espp</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">开设 <strong>WeBank活期账户</strong>和<strong>投资账户</strong>。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">在WeBank中完善您的<strong>银行档案</strong>。</div></div><div class="step"><div class="step-num">4</div><div class="step-text">账户开设完成并完善银行档案后，按标准步骤继续完成ESPP注册。</div></div></div>`},
      {section:"special",icon:"icon-green",sym:"&#127463;&#127479;",title:"巴西 — 需要Intercam验证",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">巴西员工的ESPP审批严格依据<strong>Intercam</strong>提供的官方确认名单，所有申请须经Intercam验证方可审批。</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">直接联系Intercam索取所需ESPP表格：<br><a href="mailto:janvion@intercam.com.br" style="color:#0062ff;">janvion@intercam.com.br</a> &nbsp;|&nbsp; <a href="mailto:mcrippa@intercam.com.br" style="color:#0062ff;">mcrippa@intercam.com.br</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">填写Intercam ESPP表格，以便他们验证您的申请并将您添加至官方确认名单。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Intercam确认后，<strong>ESPP合作伙伴将在SuccessFactors中审批交易</strong>。</div></div></div>`},
      {section:"special",icon:"icon-purple",sym:"&#127479;&#127476;",title:"罗马尼亚 — IBM Adobe电子签名",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">罗马尼亚的ESPP表格需要 <strong>IBM Adobe电子签名</strong>。</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">访问IBM电子签名：<a href="https://ibm.eu1.adobesign.com/account/homeJS" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ibm.eu1.adobesign.com</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">没有访问权限？在此申请：<a href="https://w3.ibm.com/w3publisher/adobe-sign/how-to-get-access" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/w3publisher/adobe-sign/how-to-get-access</a></div></div></div>`},
      {section:"special",icon:"icon-orange",sym:"&#9997;",title:"克罗地亚、立陶宛、波兰和塞尔维亚 — 需要手写签名",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下国家的ESPP表格需要<strong>手写（实体）签名</strong>：</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">克罗地亚</span><span class="tag">立陶宛</span><span class="tag">波兰</span><span class="tag">塞尔维亚</span></div><div class="info-box">请确保在SuccessFactors提交注册时，表格已完成手写签名。</div>`},
      {section:"special",icon:"icon-red",sym:"&#128683;",title:"克罗地亚、立陶宛、波兰和塞尔维亚 — 退出ESPP",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下国家的员工在退出ESPP时需要完成额外步骤：</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">克罗地亚</span><span class="tag">立陶宛</span><span class="tag">波兰</span><span class="tag">塞尔维亚</span></div><div class="info-box" style="margin-top:12px;">在SuccessFactors中成功完成<strong>退出</strong>操作后，您将收到一封包含ESPP表格的电子邮件。请填写表格并上传至<strong>OpenText</strong>。</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">在SuccessFactors中完成<strong>退出</strong>操作。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">确认退出后，查收包含ESPP表格的电子邮件。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">完整、准确地填写表格。</div></div><div class="step"><div class="step-num">4</div><div class="step-text">将填写完成的表格上传至OpenText。参考指南：<a href="https://ibm.box.com/s/9ev95b9x1eypipm0n7hc53uc0q4rotmf" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">如何将ESPP文件上传至OpenText</a></div></div></div>`},


      { section:"faq", icon:"icon-blue", sym:"&#128101;", title:"1. 参与资格",
        body:`<div class="faq-q">谁有资格参与ESPP？</div><div class="faq-a">所有正式IBM员工（含兼职）及大多数临时员工，须居住在允许参与的国家/地区。<strong>美洲：</strong>阿根廷、巴哈马、巴巴多斯、巴西、加拿大、智利、哥伦比亚、哥斯达黎加、库拉索、厄瓜多尔、牙买加、墨西哥、秘鲁、特立尼达、乌拉圭、美国、委内瑞拉。<strong>亚太地区：</strong>澳大利亚、中国、香港、印度、日本、马来西亚、新西兰、菲律宾、新加坡、韩国、台湾、泰国。<strong>欧非中东：</strong>奥地利、比利时、保加利亚、塞浦路斯、捷克、克罗地亚、丹麦、埃及、爱沙尼亚、芬兰、法国、德国、希腊、匈牙利、爱尔兰、以色列、意大利、拉脱维亚、立陶宛、卢森堡、荷兰、挪威、巴基斯坦、波兰、葡萄牙、卡塔尔、罗马尼亚、沙特阿拉伯、塞尔维亚、斯洛伐克、斯洛文尼亚、南非、西班牙、瑞典、瑞士、土耳其、阿联酋、英国。</div>
<div class="faq-q">如果我有待处理的ESPP注册申请怎么办？</div><div class="faq-a">您必须撤回所有待处理的申请才能提交新申请。SAP SuccessFactors不允许在未清除上一申请的情况下提交新申请。请检查您的<strong>待办事项</strong>列表，查找是否有需要撤回的已退回申请。</div>
<div class="faq-q">如果我目前已注册，是否需要重新注册？</div><div class="faq-a">通常不需要。以下情况需重新注册：从休假返回；曾被暂停；或已达到年度上限（购买价值25,000美元的股票或每个归属期1,000股）。美国薪资系统自动重新注册；非美国薪资系统需手动重新注册。</div>
<div class="faq-q">我是新员工，需要等多久才能注册？</div><div class="faq-a">只要您已正式入职并符合资格要求，即可在下一个注册窗口（6月1–14日或12月1–14日）注册。</div>
<div class="faq-q">我在IBM实体之间永久调动，对ESPP有何影响？</div><div class="faq-a">您的ESPP缴款不会自动延续，需在下一个全球注册窗口重新注册。若属临时调动（如全球IBMer项目），缴款在薪资所在国家继续进行。</div>
<div class="faq-q">我错过了注册窗口，还能加入吗？</div><div class="faq-a">不能——注册仅在每年两个指定窗口内开放：<strong>1月1日–6月30日</strong>（12月1–14日注册）和<strong>7月1日–12月31日</strong>（6月1–14日注册）。请等待下一个窗口。</div>` },
      { section:"faq", icon:"icon-green", sym:"&#36;", title:"2. 合格薪酬与薪资扣款",
        body:`<div class="faq-q">我可以缴纳多少？</div><div class="faq-a">您可缴纳薪资的<strong>1%至10%</strong>，须符合计划及监管规定。上限：每日历年购买价值<strong>25,000美元</strong>的股票，每个归属期不超过<strong>1,000股</strong>。美国员工：ESPP扣款在大多数其他项目扣款之后进行，不允许部分扣款。</div>
<div class="faq-q">我能对不同类型的薪酬设置不同的比例吗？</div><div class="faq-a">可以。您可授权从<strong>IBM基本工资/薪水</strong>（定期薪酬、定期佣金、假期工资、STD）和/或<strong>IBM其他薪酬</strong>（激励、浮动薪酬、佣金）中扣款，各项须在1%至10%之间。</div>
<div class="faq-q">注册窗口关闭后能否调整缴款？</div><div class="faq-a">注册窗口期间可<strong>增加或减少</strong>缴款。窗口关闭后，您仍可随时<strong>减少</strong>缴款，但不能<strong>增加</strong>，直至下一个注册窗口。您可随时退出。</div>
<div class="faq-q">IBM股票购买价格如何确定？</div><div class="faq-a">价格为每个薪资日IBM股票最高价和最低价平均值的<strong>85%</strong>——即每次购买享有<strong>15%折扣</strong>。</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#8801;", title:"3. EquatePlus平台",
        body:`<div class="faq-q">无法登录EquatePlus账户怎么办？</div><div class="faq-a">在EquatePlus登录主页选择<strong>帮助</strong>链接并按照说明操作，该页面包含Computershare客服中心联系方式。</div>
<div class="faq-q">为何我同时拥有EquatePlus和Investor Center账户？</div><div class="faq-a">这通常发生在您持有纸质股票证书时——纸质证书账户在收回证书前无法与电子账户合并。请联系<strong>infoibm@us.ibm.com</strong>获取整合协助。</div>
<div class="faq-q">为何EquatePlus中我的姓名顺序颠倒了？</div><div class="faq-a">姓名通过IBM的月度/双月文件更新。请提交<strong>AskHR工单</strong>，确保下次文件与SAP SuccessFactors档案一致。</div>
<div class="faq-q">如何更新EquatePlus中的地址和个人信息？</div><div class="faq-a">在职员工的信息通过Computershare的入站文件更新。离职员工请直接联系Computershare。</div>
<div class="faq-q">扣款后多久股票会显示在EquatePlus中？</div><div class="faq-a">IBM在每个薪资扣款日购买股票，各国显示时间不同：
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:8px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">时间</th><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">国家</th></tr></thead>
<tbody>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">1–10天</td><td style="padding:6px 10px;border:1px solid #dde1e7;">阿根廷、加拿大、哥斯达黎加、法国、德国、拉脱维亚、墨西哥、荷兰、巴基斯坦、罗马尼亚、新加坡、韩国、西班牙、瑞典、瑞士、特立尼达、英国、美国</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">10–20天</td><td style="padding:6px 10px;border:1px solid #dde1e7;">奥地利、巴巴多斯、比利时、巴西、保加利亚、智利、哥伦比亚、捷克、厄瓜多尔、埃及、爱沙尼亚、芬兰、香港、匈牙利、印度、爱尔兰、以色列、牙买加、立陶宛、马来西亚、新西兰、秘鲁、菲律宾、波兰、葡萄牙、卡塔尔、沙特阿拉伯、塞尔维亚、斯洛伐克、斯洛文尼亚、南非、台湾、泰国、土耳其、阿联酋、乌拉圭、委内瑞拉</td></tr>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">20天以上</td><td style="padding:6px 10px;border:1px solid #dde1e7;">澳大利亚、中国、克罗地亚、塞浦路斯、丹麦、希腊、日本、挪威</td></tr>
</tbody></table>
<div class="note" style="margin-top:8px;">IBM和EquatePlus会监控延迟情况，更新信息会通过Slack的<strong>#espp-ibmshare</strong>频道或电子邮件通知参与者。</div></div>` },
      { section:"faq", icon:"icon-orange", sym:"&#9401;", title:"4. 暂停与离职",
        body:`<div class="faq-q">若我退出、退休或离开IBM，我的股票会怎样？</div><div class="faq-a">股票将保留在您的Computershare参与者账户中，直至您提取或授权出售。若您离开IBM，请将Computershare中的联系邮箱更新为<strong>非IBM邮箱</strong>以继续接收通讯。</div>
<div class="faq-q">我已退出但仍被扣款，原因是什么？</div><div class="faq-a">可能是时间差问题。请在SuccessFactors中确认参与状态已成功终止。若扣款持续，请直接联系<strong>Computershare</strong>。</div>
<div class="faq-q">为何ESPP扣款停止？工资单上显示"ESPP退款"。</div><div class="faq-a">可能原因：休假；达到年度25,000美元上限或归属期1,000股上限；或达到归属期总股份上限。</div>
<div class="faq-q">暂停后是否自动恢复？</div><div class="faq-a"><strong>美国薪资：</strong>因达到25,000美元/1,000股上限或从休假返回后自动恢复。<strong>非美国薪资：</strong>建议在下一个注册窗口手动重新注册——各国管理方式不同，并非所有薪资系统都会自动恢复。</div>` },
      { section:"faq", icon:"icon-blue", sym:"&#128200;", title:"6. 查看、出售与转让股票",
        body:`<div class="faq-q">如何在EquatePlus中查看和管理股票？</div><div class="faq-a">登录EquatePlus，使用<strong>概览</strong>、<strong>资料库</strong>和<strong>帮助</strong>菜单。</div>
<div class="faq-q">工资单上有ESPP扣款，但EquatePlus中没有显示股票，原因是什么？</div><div class="faq-a">非美国薪资系统的发薪日通常在月末，当地薪资团队向Computershare发送购买指令可能需要<strong>2–3周</strong>。月末扣款可能在次月中旬才会显示。</div>
<div class="faq-q">如何出售股票？</div><div class="faq-a">通过<strong>EquatePlus</strong>或<strong>EquateMobile</strong>全天候提交出售申请，支持100多种货币付款。Computershare联系方式：<strong>1-888-426-6700</strong>（美国/加拿大/波多黎各）或<strong>781-575-2727</strong>（国际）。每次交易手续费约$19.95。</div>
<div class="faq-q">持有多久才能出售股票？</div><div class="faq-a">股票入账EquatePlus后即可随时出售。根据持有期限和当地税法，可能存在税务影响。美国员工符合条件的处置可享受特殊联邦所得税待遇。</div>
<div class="faq-q">如何将股票转入金融机构？</div><div class="faq-a">在EquatePlus的<strong>财务偏好</strong>中添加您的经纪账户，然后在主页点击<strong>交易</strong>提交经纪转账。Computershare和IBM均不收取转账费——任何费用均来自接收经纪商。仅支持DTC成员经纪商。</div>
<div class="faq-q">出售股票时货币兑换如何运作？</div><div class="faq-a">您将获得零售银行汇率，根据交易市场和交易金额，手续费最高可达收益的<strong>3%</strong>。</div>` },
      { section:"faq", icon:"icon-green", sym:"&#127987;", title:"7. 股息",
        body:`<div class="faq-q">股息如何支付？</div><div class="faq-a">根据持有股份，您有三种选择：<strong>（1）自动再投资</strong>（2023年1月1日起注册者的默认方式）——以公平市值再投资于IBM股票，手续费为每次股息的2%或最高3美元；<strong>（2）电子转账</strong>——通过ACH或电汇转入您的银行/经纪账户（可能收取手续费）；<strong>（3）美元支票</strong>——仅在未存档银行信息时发送。非美国员工可在EquatePlus中添加电汇信息以选择当地货币股息（需支付10美元电汇费）。</div>` },
      { section:"faq", icon:"icon-red", sym:"&#128203;", title:"8. 税务",
        body:`<div class="faq-q">代我购买股票时需要纳税吗？</div><div class="faq-a">在许多国家，您需就购买折扣缴税。税款可能由当地薪资系统代扣，也可能需要您自行申报。请通过EquatePlus填写<strong>W-9BEN表格</strong>（美国纳税人）或<strong>W-8BEN表格</strong>（非美国纳税人），以避免多扣税款。</div>
<div class="faq-q">出售股票时需要纳税吗？</div><div class="faq-a">根据持有期限和当地税法，可能存在税务影响。美国员工在满足持有期限要求时可享受特殊联邦所得税待遇。请咨询税务专业人士。</div>
<div class="faq-q">什么是W-8BEN / W-9BEN，我需要填写吗？</div><div class="faq-a"><strong>W-9BEN</strong>适用于美国纳税人，未填写将导致出售收益和股息被<strong>预扣24%美国税款</strong>。<strong>W-8BEN</strong>为非美国纳税人的等效表格。两者均通过EquatePlus/EquateMobile提交，自完成之日起第三个日历年末到期——请在到期前续签，EquatePlus将提醒您。</div>
<div class="faq-q">什么是ESPP取消资格处置（423b）？</div><div class="faq-a">当您出售第423条款计划的ESPP股票，且未满足以下持有期限时，即发生取消资格处置：自授予日起超过2年且自购买日起超过1年。<strong>注意：</strong>美国以外的参与者不受取消资格处置报告要求约束。</div>
<div class="faq-q">什么是FTIN（外国税务识别号）？</div><div class="faq-a">FTIN是由您所在国家税务机关分配的唯一标识符。详情请在EquatePlus税务表格的FTIN部分点击<strong>?</strong>查看。</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#9997;", title:"9. 其他问题",
        body:`<div class="faq-q">我可以申请股票证书吗？</div><div class="faq-a">可以。请联系Computershare申请账户中部分或全部完整股份的证书。</div>
<div class="faq-q">我需要为ESPP股票指定受益人吗？</div><div class="faq-a">不需要。ESPP没有"受益人"指定。您可以单独以自己名义购买股份，或通过EquatePlus的<strong>个人偏好</strong>与家庭成员以生存者权益共同购买。</div>
<div class="faq-q">因全球调动需要转移ESPP参与权，如何操作？</div><div class="faq-a">请直接联系Computershare。</div>
<div class="faq-q">如何查询我的ESPP缴款历史？</div><div class="faq-a">在EquatePlus中导航至<strong>计划详情</strong>，选择<strong>历史购买记录</strong>。</div>
<div class="faq-q">如何对Computershare的服务提供反馈？</div><div class="faq-a">若您与Computershare的问题未得到解决或有不良体验，请提交<strong>AskHR工单</strong>。</div>
<div class="faq-q">在哪里可以找到ESPP政策和注册指南？</div><div class="faq-a">在IBM内网：<strong>w3.ibm.com → 全球薪酬计划 → ESPP → ESPP常见问题</strong>。包含资格要求、注册窗口、缴款上限、购买日期、退出规则及常见问题。</div>` },
      {section:"resources",icon:"icon-purple",sym:"&#128279;",title:"参考链接与支持",body:`<ul class="resource-list"><li><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs" target="_blank" rel="noopener"><strong>ESPP w3 页面</strong></a> — IBM内网上的完整计划说明</li><li><a href="https://w3.ibm.com/hr/askhr/home" target="_blank" rel="noopener"><strong>AskHR</strong></a> — 提交注册问题或国家特定问题的工单</li><li><strong>SAP SuccessFactors – 福利模块</strong> — 注册、更新和查看您的选择</li><li><a href="https://www.na.equateplus.com/EquatePlusParticipant2/?login" target="_blank" rel="noopener"><strong>EquatePlus 平台</strong></a> — 购买后管理您的股票</li></ul>`}
    ]
  },
  ja: {
    badge:"IBM ベネフィット", title:"従業員持株購入制度（ESPP）", subtitle:"参加者ガイド — 加入手続き・拠出金管理・特別ケース・よくある質問",
    search:"キーワード、国名などで検索…", noResults:"該当するトピックが見つかりませんでした。",
    tabs:["すべて","制度概要","新規加入","既存参加者","加入状況の確認","特別ケース","よくある質問","参考リンク"],
    sections:{overview:"制度概要",new:"新規加入者",existing:"既存参加者",check:"加入状況・拠出率の確認",special:"特別ケース",faq:"よくある質問（FAQ）",resources:"参考リンク・サポート"},
    ceeCountries:["クロアチア","エストニア","ラトビア","ポーランド","ルーマニア","リトアニア","セルビア","ベネズエラ"],
    approvalCountries:["ブラジル","イタリア","クロアチア","エストニア","ラトビア","ポーランド","ルーマニア","リトアニア","セルビア"],
    cards:[
      { section:"overview", icon:"icon-blue", sym:"&#9733;", title:"ESPPとは？",
        body:`<p style="font-size:14px;color:#21272a;line-height:1.75;margin-top:8px;"><strong>従業員持株購入制度（ESPP）</strong>は、IBM従業員が市場価格から<strong>15%割引</strong>でIBM株を購入できる制度です。拠出は給与控除により自動的に行われるため、手動での取引は不要です。</p>
<div class="info-box" style="margin-top:14px;"><strong>仕組み：</strong>給与期間ごとに対象報酬の1%〜10%を拠出します。IBMが購入日に15%割引で代わりに株式を購入し、EquatePlusアカウントに記録されます。</div>
<div class="steps" style="margin-top:16px;">
<div class="step"><div class="step-num">1</div><div class="step-text">受付期間（6月1〜14日または12月1〜14日）に加入手続きを行います。</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">次の提供期間（1月1日または7月1日）から給与控除が始まります。</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">IBMは各給与支払日に15%割引で株式を購入します。</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">購入後、数日〜数週間以内にEquatePlusアカウントに株式が反映されます（国によって異なります）。</div></div>
</div>` },
      { section:"overview", icon:"icon-green", sym:"&#36;", title:"メリットと例",
        body:`<div class="section-heading" style="margin-top:10px;">なぜ加入するのか？</div>
<ul style="margin:0 0 14px 18px;font-size:13.5px;color:#21272a;line-height:1.8;">
<li>IBM株を市場価格から<strong>15%割引</strong>で購入できる</li>
<li>給与控除により自動的に投資できる</li>
<li>購入割引による即座の投資メリット</li>
<li>IBM株価上昇時に追加リターンを得られる可能性がある</li>
<li>IBM株保有中に<strong>配当金</strong>を受け取れる</li>
<li>IBMの株主になれる</li>
</ul>
<div class="section-heading">計算例</div>
<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:6px;">
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;width:55%;">月給</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$4,000</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">拠出額（10%）</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$400</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">IBM株市場価格</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$130 / 株</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">ESPP購入価格（15%割引）</td><td style="padding:7px 12px;border:1px solid #dde1e7;color:#0062ff;font-weight:600;">$110.50 / 株</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">購入株数</td><td style="padding:7px 12px;border:1px solid #dde1e7;">3.62 株</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">株式の市場価値</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$470.60</td></tr>
<tr style="background:#edf5ff;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">即時リターン</td><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">17.6%</td></tr>
</table>
<div class="note" style="margin-top:12px;"><strong>注：</strong>この例はあくまでも参考です。実際の株価やリターンは異なります。</div>` },
      { section:"overview", icon:"icon-purple", sym:"&#128196;", title:"制度詳細",
        body:`<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:10px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">制度の特徴</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">詳細</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">割引率</td><td style="padding:8px 12px;border:1px solid #dde1e7;">各給与購入日に市場価格から15%割引</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">拠出率の範囲</td><td style="padding:8px 12px;border:1px solid #dde1e7;">対象報酬の1%〜10%（整数%または小数点以下2桁まで）</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">年間上限</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1暦年あたり株式購入額$25,000 USD相当</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">期間別上限</td><td style="padding:8px 12px;border:1px solid #dde1e7;">6か月の提供期間あたり1,000株</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">最低購入額</td><td style="padding:8px 12px;border:1px solid #dde1e7;">なし</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">対象報酬の種類</td><td style="padding:8px 12px;border:1px solid #dde1e7;"><strong>基本給</strong> — 定期的な給与<br><strong>その他報酬</strong> — ボーナス、コミッション、インセンティブ、変動報酬</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">提供期間</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1月1日〜6月30日 &nbsp;|&nbsp; 7月1日〜12月31日</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">購入頻度</td><td style="padding:8px 12px;border:1px solid #dde1e7;">各給与控除日</td></tr>
</tbody></table>` },
      { section:"overview", icon:"icon-orange", sym:"&#36;&#36;", title:"標準手数料 (Computershare)",
        body:`<p style="font-size:13.5px;color:#21272a;margin-top:8px;margin-bottom:12px;">加入前に、IBMのグローバルベンダーであるComputershareを通じたESPPの標準手数料をご確認ください。</p>
<table style="width:100%;border-collapse:collapse;font-size:13px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">取引</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">手数料（USD）</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">株式売却</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$19.95</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">金融機関への株式移管</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">無料</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">電信送金手数料（米国・非米国）— 売却代金の銀行送金</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$35</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">配当金または売却代金のUSD小切手</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">無料</td></tr>
</tbody></table>
<div class="info-box" style="margin-top:12px;">加入前に<strong><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-prospectus" target="_blank" rel="noopener" style="color:#0043ce;">目論見書</a></strong>と<strong><a href="https://ibm.mystockoptions.com/global-tax-guide/?ibmtoken=SUJNVE9LRU4yNA==" target="_blank" rel="noopener" style="color:#0043ce;">グローバル税務ガイド</a></strong>もご確認いただき、各国の税務上の影響をご理解ください。個別の状況については税務の専門家にご相談ください。</div>` },
      {section:"new",icon:"icon-blue",sym:"&#43;",title:"ESPPへの加入方法",body:`<div class="info-box"><strong>加入期間限定。</strong>年2回の加入受付期間（6月・12月）のみ加入可能です。電子署名が必要です。</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors ベネフィットポートレット</strong>にアクセスします。</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「ベネフィット概要へ」</strong>をクリックします。</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>「オープン加入」</strong>より<strong>「ESPP – IBM 基本給控除」</strong>または<strong>「ESPP – IBM その他報酬」</strong>の<strong>「加入」</strong>をクリックします。</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>「有効開始日」</strong>は各国の給与カレンダーに基づいて自動設定されます。</div></div><div class="step"><div class="step-num">5</div><div class="step-text"><strong>従業員拠出率（1〜10%）</strong>を入力します。</div></div><div class="step"><div class="step-num">6</div><div class="step-text"><strong>「同意する」</strong>欄で<strong>「はい」</strong>を選択し、<strong>「保存」</strong>をクリックします。</div></div></div><div class="note"><strong>両プランに加入する場合：</strong>それぞれ個別に「加入」をクリックしてください。</div>`},
      {section:"new",icon:"icon-green",sym:"&#10003;",title:"加入後の流れ",body:`<div class="timeline"><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">12月受付期間</div>最初の控除は<strong>1月</strong>から開始。</div></div><div class="tl-item"><div class="tl-dot purple"></div><div class="tl-content"><div class="tl-label purple">6月受付期間</div>最初の控除は<strong>7月</strong>から開始。</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">控除の確認</div>SAP SuccessFactors の<strong>給与明細</strong>で確認してください。</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">EquatePlus 認証情報</div>最初の購入が入金された後に認証情報が作成されます。下表参照。</div></div></div>
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:12px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">付与期間</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">給与</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">認証情報の送付目安</th></tr></thead>
<tbody>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">1月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">米国給与</td><td style="padding:7px 10px;border:1px solid #dde1e7;">1月15日給与明細発行後1週間以内</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">1月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">非米国給与</td><td style="padding:7px 10px;border:1px solid #dde1e7;">1月給与明細発行後2週間以内</td></tr>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">7月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">米国給与</td><td style="padding:7px 10px;border:1px solid #dde1e7;">7月15日給与明細発行後1週間以内</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">7月</td><td style="padding:7px 10px;border:1px solid #dde1e7;">非米国給与</td><td style="padding:7px 10px;border:1px solid #dde1e7;">7月給与明細発行後2週間以内</td></tr>
</tbody></table>
`},
      {section:"existing",icon:"icon-orange",sym:"&#8595;",title:"拠出率の引き下げ・脱退",body:`<div class="info-box"><strong>いつでも変更可能。</strong>年間を通じていつでも引き下げ・脱退ができます。</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors ベネフィットポートレット</strong>にアクセスします。</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「ベネフィット概要へ」</strong>をクリックします。</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>引き下げ：</strong>「ESPP/年金」タブで<strong>鉛筆アイコン</strong>をクリックして変更・保存。</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>脱退：</strong><strong>「脱退」</strong>をクリック。</div></div></div>`},
      {section:"existing",icon:"icon-blue",sym:"&#8593;",title:"拠出率の引き上げ",body:`<div class="info-box"><strong>加入受付期間限定。</strong>6月または12月の受付期間中のみ引き上げ可能です。</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors ベネフィットポートレット</strong>にアクセスします。</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「ベネフィット概要へ」</strong>をクリックします。</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>「加入」タブ</strong>に移動します。</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>有効日</strong>と<strong>従業員拠出率</strong>を設定します。</div></div><div class="step"><div class="step-num">5</div><div class="step-text"><strong>「はい」</strong>を選択して<strong>「保存」</strong>をクリック。</div></div></div>`},
      {section:"check",icon:"icon-blue",sym:"&#128196;",title:"方法1 — ベネフィットポートレット",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors ベネフィットポートレット</strong>にアクセスします。</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「ベネフィット概要へ」</strong>をクリックします。</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>「ESPP/年金」</strong>を選択して内容を確認。</div></div></div>`},
      {section:"check",icon:"icon-purple",sym:"&#128203;",title:"方法2 — ベネフィット確認書",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors ベネフィットポートレット</strong>にアクセスします。</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「ベネフィット明細を見る」</strong>をクリックします。</div></div></div><div class="note"><strong>最近変更した場合：</strong>「基準日」を加入有効日に設定（6月受付→<strong>7月1日</strong>、12月受付→翌年<strong>1月1日</strong>）。</div>`},
      {section:"check",icon:"icon-green",sym:"&#9733;",title:"方法3 — トータルリワードタブ",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SAP SuccessFactors のプロフィール</strong>に移動します。</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「トータルリワード」タブ</strong>を選択します。</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>「定期控除」</strong>セクションに選択内容が表示されます。</div></div></div>`},
      {section:"special",icon:"icon-red",sym:"&#9873;",title:"CEE諸国 — 書類添付が必要",cee:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下の国の従業員は所定の書類を添付する必要があります：</p>{{CEE_TAGS}}<div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">加入画面内からフォームをダウンロードします。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">内容が加入申請と<strong>一致するよう</strong>記入します。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">SuccessFactors に再添付します。</div></div></div><div class="note"><strong>ダウンロードできない場合：</strong>既知の問題です。<strong>AskHR チケット</strong>を起票してください。</div>`},
      {section:"special",icon:"icon-orange",sym:"&#9203;",title:"追加承認が必要な国",approval:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下の国では承認完了まで選択内容が<strong>表示されません</strong>：</p>{{APPROVAL_TAGS}}<div class="info-box" style="margin-top:14px;">これは正常な動作です。長期間表示されない場合は<strong>AskHR</strong>にお問い合わせください。</div>`},
      {section:"special",icon:"icon-blue",sym:"&#127470;&#127481;",title:"イタリア — WeBankアカウント必須",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">イタリア従業員がESPPに参加するには、登録前に追加要件を満たす必要があります。</p><div class="info-box" style="margin-top:10px;">参加には<strong>WeBankの普通預金口座</strong>と<strong>投資口座</strong>の両方が必要です。</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">イタリア従業員向け詳細手順を確認：<a href="https://w3.ibm.com/hr/policy/it-compensation-espp" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/hr/policy/it-compensation-espp</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>WeBank普通預金口座</strong>と<strong>投資口座</strong>を開設します。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">WeBankで<strong>銀行プロフィール</strong>を完成させます。</div></div><div class="step"><div class="step-num">4</div><div class="step-text">口座開設と銀行プロフィールの完成後、通常のESPP加入手順に進んでください。</div></div></div>`},
      {section:"special",icon:"icon-green",sym:"&#127463;&#127479;",title:"ブラジル — Intercam検証必須",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">ブラジル従業員のESPP承認は、<strong>Intercam</strong>が提供する公式確認リストに基づいて行われます。すべての申請はIntercamの検証が必要です。</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">IntercamにESPPフォームを直接請求：<br><a href="mailto:janvion@intercam.com.br" style="color:#0062ff;">janvion@intercam.com.br</a> &nbsp;|&nbsp; <a href="mailto:mcrippa@intercam.com.br" style="color:#0062ff;">mcrippa@intercam.com.br</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">IntercamのESPPフォームに記入し、申請を検証してもらい公式確認リストに追加してもらいます。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Intercamの確認後、<strong>ESPPパートナーがSuccessFactorsで取引を承認</strong>します。</div></div></div>`},
      {section:"special",icon:"icon-purple",sym:"&#127479;&#127476;",title:"ルーマニア — IBM Adobe電子署名",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">ルーマニアのESPPフォームには<strong>IBM Adobe電子署名</strong>が必要です。</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">IBM電子署名にアクセス：<a href="https://ibm.eu1.adobesign.com/account/homeJS" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ibm.eu1.adobesign.com</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">アクセス権がない場合はこちらで申請：<a href="https://w3.ibm.com/w3publisher/adobe-sign/how-to-get-access" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/w3publisher/adobe-sign/how-to-get-access</a></div></div></div>`},
      {section:"special",icon:"icon-orange",sym:"&#9997;",title:"クロアチア・リトアニア・ポーランド・セルビア — 直筆署名必須",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下の国では、ESPPフォームに<strong>直筆（物理的な）署名</strong>が必要です：</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">クロアチア</span><span class="tag">リトアニア</span><span class="tag">ポーランド</span><span class="tag">セルビア</span></div><div class="info-box">SuccessFactorsで登録書類として提出する前に、フォームに直筆署名が済んでいることを確認してください。</div>`},
      {section:"special",icon:"icon-red",sym:"&#128683;",title:"クロアチア・リトアニア・ポーランド・セルビア — ESPP脱退手続き",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">以下の国の従業員がESPPを脱退する際は、追加の手順が必要です：</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">クロアチア</span><span class="tag">リトアニア</span><span class="tag">ポーランド</span><span class="tag">セルビア</span></div><div class="info-box" style="margin-top:12px;">SuccessFactorsで<strong>脱退</strong>手続きが完了すると、ESPPフォームが添付されたメールが届きます。フォームを記入し、<strong>OpenText</strong>にアップロードしてください。</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">SuccessFactorsで<strong>脱退</strong>手続きを完了します。</div></div><div class="step"><div class="step-num">2</div><div class="step-text">脱退確認後、ESPPフォームが添付されたメールを確認します。</div></div><div class="step"><div class="step-num">3</div><div class="step-text">フォームに完全かつ正確に記入します。</div></div><div class="step"><div class="step-num">4</div><div class="step-text">記入済みフォームをOpenTextにアップロードします。手順はこちら：<a href="https://ibm.box.com/s/9ev95b9x1eypipm0n7hc53uc0q4rotmf" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ESPPドキュメントをOpenTextにアップロードする方法</a></div></div></div>`},


      { section:"faq", icon:"icon-blue", sym:"&#128101;", title:"1. 参加資格",
        body:`<div class="faq-q">ESPPに参加できるのは誰ですか？</div><div class="faq-a">パートタイムを含む正規のIBM社員および大多数の補助的従業員で、参加が認められている国に居住していることが条件です。<strong>アメリカ：</strong>アルゼンチン、バハマ、バルバドス、ブラジル、カナダ、チリ、コロンビア、コスタリカ、キュラソー、エクアドル、ジャマイカ、メキシコ、ペルー、トリニダード、ウルグアイ、米国、ベネズエラ。<strong>アジア太平洋：</strong>オーストラリア、中国、香港、インド、日本、マレーシア、ニュージーランド、フィリピン、シンガポール、韓国、台湾、タイ。<strong>EMEA：</strong>オーストリア、ベルギー、ブルガリア、キプロス、チェコ、クロアチア、デンマーク、エジプト、エストニア、フィンランド、フランス、ドイツ、ギリシャ、ハンガリー、アイルランド、イスラエル、イタリア、ラトビア、リトアニア、ルクセンブルク、オランダ、ノルウェー、パキスタン、ポーランド、ポルトガル、カタール、ルーマニア、サウジアラビア、セルビア、スロバキア、スロベニア、南アフリカ、スペイン、スウェーデン、スイス、トルコ、UAE、英国。</div>
<div class="faq-q">ESPP加入申請が処理待ちの場合はどうすればいいですか？</div><div class="faq-a">新しい申請を提出する前に、処理待ちの申請をすべて取り消す必要があります。前回の申請がクリアされるまで、SAP SuccessFactorsでは新たな申請ができません。取り消しが必要な差し戻し申請がないか<strong>ToDo</strong>リストを確認してください。</div>
<div class="faq-q">すでに加入している場合、再加入は必要ですか？</div><div class="faq-a">通常は不要です。再加入が必要な場合：休職から復帰する場合；以前に停止された場合；年間上限（株式$25,000 USD相当または提供期間あたり1,000株）に達した場合。米国給与はシステムが自動的に再加入しますが、非米国給与は手動で再加入が必要です。</div>
<div class="faq-q">新入社員ですが、加入までどのくらい待てばよいですか？</div><div class="faq-a">正式に入社手続きが完了し、資格要件を満たしていれば、次の加入受付期間（6月1〜14日または12月1〜14日）に加入できます。</div>
<div class="faq-q">IBM間で恒久的に異動した場合、ESPPはどうなりますか？</div><div class="faq-a">ESPP拠出は自動的に継続されません。次のグローバル加入受付期間に再加入する必要があります。一時的な異動（例：グローバルIBMer赴任）の場合は、給与が処理される国で拠出が継続されます。</div>
<div class="faq-q">加入受付期間を逃した場合、加入できますか？</div><div class="faq-a">いいえ——加入は年2回の指定期間中のみ可能です：<strong>1月1日〜6月30日</strong>（12月1〜14日加入受付）と<strong>7月1日〜12月31日</strong>（6月1〜14日加入受付）。次の期間をお待ちください。</div>` },
      { section:"faq", icon:"icon-green", sym:"&#36;", title:"2. 対象報酬・給与控除",
        body:`<div class="faq-q">いくら拠出できますか？</div><div class="faq-a">給与の<strong>1%〜10%</strong>（制度・規制上の上限に従う）。上限：1暦年あたり<strong>$25,000相当の株式</strong>、提供期間あたり<strong>1,000株</strong>以内。米国では、ESPP控除は他の多くの控除の後に行われ、一部控除は認められません。</div>
<div class="faq-q">種類別の報酬に異なる割合を指定できますか？</div><div class="faq-a">はい。<strong>IBM基本給</strong>（定期報酬、定期コミッション、休暇給、STD）および/または<strong>IBMその他報酬</strong>（インセンティブ、変動報酬、コミッション）から控除を設定できます。それぞれ1%〜10%の範囲内です。</div>
<div class="faq-q">加入受付期間終了後に拠出率を変更できますか？</div><div class="faq-a">加入受付期間中は<strong>増減</strong>できます。期間終了後は提供期間中いつでも<strong>減額</strong>は可能ですが、<strong>増額</strong>は次の加入受付期間まで不可です。いつでも脱退可能です。</div>
<div class="faq-q">IBM株の購入価格はどのように決まりますか？</div><div class="faq-a">各給与支払日のIBM株の高値と安値の平均の<strong>85%</strong>——すべての購入で<strong>15%割引</strong>が適用されます。</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#8801;", title:"3. EquatePlus プラットフォーム",
        body:`<div class="faq-q">EquatePlusアカウントにアクセスできません。どうすればいいですか？</div><div class="faq-a">EquatePlusログインページの<strong>ヘルプ</strong>リンクを選択し、指示に従ってください。そのページにはComputershareのコールセンター連絡先が記載されています。</div>
<div class="faq-q">EquatePlusとInvestor Centerの両方のアカウントがあるのはなぜですか？</div><div class="faq-a">これは通常、紙の株券を保有している場合に発生します——紙の株券がある口座は、株券が回収されるまで電子口座と統合できません。統合のサポートは<strong>infoibm@us.ibm.com</strong>にお問い合わせください。</div>
<div class="faq-q">EquatePlusで姓名が逆になっているのはなぜですか？</div><div class="faq-a">名前はIBMからの月次/隔月ファイルで更新されます。次回のファイルがSAP SuccessFactorsプロフィールと一致するよう<strong>AskHRチケット</strong>を作成してください。</div>
<div class="faq-q">EquatePlusの住所や個人情報を更新するにはどうすればいいですか？</div><div class="faq-a">在職中の従業員の情報はComputershareへの入力ファイルで更新されます。退職した従業員は直接Computershareにお問い合わせください。</div>
<div class="faq-q">控除後、EquatePlusに株式が反映されるまでどのくらいかかりますか？</div><div class="faq-a">IBMは各給与控除日に株式を購入します。表示までの時間は国によって異なります：
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:8px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">期間</th><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">国</th></tr></thead>
<tbody>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">1〜10日</td><td style="padding:6px 10px;border:1px solid #dde1e7;">アルゼンチン、カナダ、コスタリカ、フランス、ドイツ、ラトビア、メキシコ、オランダ、パキスタン、ルーマニア、シンガポール、韓国、スペイン、スウェーデン、スイス、トリニダード、英国、米国</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">10〜20日</td><td style="padding:6px 10px;border:1px solid #dde1e7;">オーストリア、バルバドス、ベルギー、ブラジル、ブルガリア、チリ、コロンビア、チェコ、エクアドル、エジプト、エストニア、フィンランド、香港、ハンガリー、インド、アイルランド、イスラエル、ジャマイカ、リトアニア、マレーシア、ニュージーランド、ペルー、フィリピン、ポーランド、ポルトガル、カタール、サウジアラビア、セルビア、スロバキア、スロベニア、南アフリカ、台湾、タイ、トルコ、UAE、ウルグアイ、ベネズエラ</td></tr>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">20日以上</td><td style="padding:6px 10px;border:1px solid #dde1e7;">オーストラリア、中国、クロアチア、キプロス、デンマーク、ギリシャ、日本、ノルウェー</td></tr>
</tbody></table>
<div class="note" style="margin-top:8px;">遅延はIBMとEquatePlusが監視しています。更新情報はSlackの<strong>#espp-ibmshare</strong>または参加者へのメールで通知されます。</div></div>` },
      { section:"faq", icon:"icon-orange", sym:"&#9401;", title:"4. 停止・退職",
        body:`<div class="faq-q">脱退・退職・IBM退社時、株式はどうなりますか？</div><div class="faq-a">株式は、取り出しまたは売却を承認するまで、ComputershareのIBM参加者口座に保管されます。IBM退社の場合は、引き続き連絡を受けるためにComputershareの連絡先メールを<strong>IBM以外のアドレス</strong>に更新してください。</div>
<div class="faq-q">脱退したのにESPP控除が行われました。なぜですか？</div><div class="faq-a">タイミングの問題かもしれません。SuccessFactorsで参加が正常に終了しているか確認してください。控除が続く場合は直接<strong>Computershare</strong>にお問い合わせください。</div>
<div class="faq-q">ESPP控除が停止しました。給与明細に「ESPPリファンド」と表示されます。</div><div class="faq-a">停止の理由：休職；年間$25,000上限または提供期間の1,000株上限に達した場合；提供期間の総株式上限に達した場合。</div>
<div class="faq-q">停止後の再開は自動的に行われますか？</div><div class="faq-a"><strong>米国給与：</strong>$25,000/1,000株上限到達時および休職からの復帰時は自動再開。<strong>非米国給与：</strong>次の加入受付期間に手動で再加入することをお勧めします——国によって管理方法が異なり、すべての給与で自動再開されるわけではありません。</div>` },
      { section:"faq", icon:"icon-blue", sym:"&#128200;", title:"6. 株式の確認・売却・移転",
        body:`<div class="faq-q">EquatePlusで株式を確認・管理するにはどうすればいいですか？</div><div class="faq-a">EquatePlusにログインし、<strong>概要</strong>、<strong>ライブラリ</strong>、<strong>ヘルプ</strong>メニューを利用してください。</div>
<div class="faq-q">給与明細にESPP控除があるのに、EquatePlusに株式が表示されません。なぜですか？</div><div class="faq-a">非米国給与の場合、支払日は月末となり、現地給与チームがComputershareに購入指示を送るまで<strong>2〜3週間</strong>かかる場合があります。月末の控除は翌月中旬頃まで表示されないことがあります。</div>
<div class="faq-q">株式を売却するにはどうすればいいですか？</div><div class="faq-a"><strong>EquatePlus</strong>または<strong>EquateMobile</strong>から24時間365日売却申請ができます。100以上の通貨で送金可能。Computershare連絡先：<strong>1-888-426-6700</strong>（米国/カナダ/プエルトリコ）または<strong>781-575-2727</strong>（国際）。取引手数料：1回約$19.95。</div>
<div class="faq-q">株式を売却するまでにどのくらい保有する必要がありますか？</div><div class="faq-a">EquatePlusに株式が入金された後はいつでも売却できます。保有期間と現地税法によって税務上の影響が生じる場合があります。米国従業員は適格処分の特別連邦所得税優遇措置を受けられる場合があります。</div>
<div class="faq-q">株式を金融機関に移管するにはどうすればいいですか？</div><div class="faq-a">EquatePlusの<strong>財務設定</strong>で証券会社口座を追加し、ホームページの<strong>取引</strong>をクリックして証券会社へ移管申請を行ってください。ComputershareもIBMも移管手数料は請求しません——手数料は受け取り証券会社から発生する場合があります。DTC加盟証券会社のみ対応。</div>
<div class="faq-q">株式売却時の通貨換算はどのように機能しますか？</div><div class="faq-a">小売銀行レートが適用され、取引市場と取引金額によっては売却額の最大<strong>3%の手数料</strong>が含まれる場合があります。</div>` },
      { section:"faq", icon:"icon-green", sym:"&#127987;", title:"7. 配当",
        body:`<div class="faq-q">配当金はどのように支払われますか？</div><div class="faq-a">保有株式数に応じて3つの選択肢があります：<strong>（1）自動再投資</strong>（2023年1月1日以降の加入者のデフォルト）——公正市場価値でIBM株に再投資；手数料は配当金あたり2%または最大$3。<strong>（2）電子送金</strong>——ACHまたは電信送金で銀行/証券会社口座へ（手数料が発生する場合があります）。<strong>（3）USD小切手</strong>——銀行口座情報が未登録の場合のみ送付。非米国従業員はEquatePlusに電信送金情報を追加することで現地通貨配当を選択できます（電信送金手数料$10が発生）。</div>` },
      { section:"faq", icon:"icon-red", sym:"&#128203;", title:"8. 税務",
        body:`<div class="faq-q">株式が代わりに購入される際に税金を支払いますか？</div><div class="faq-a">多くの国では、購入時に受け取る割引に対して課税されます。現地給与で源泉徴収される場合もあれば、自分で申告が必要な場合もあります。過剰な税務控除を避けるため、EquatePlusを通じて<strong>W-9BENフォーム</strong>（米国納税者）または<strong>W-8BENフォーム</strong>（非米国納税者）で認証してください。</div>
<div class="faq-q">株式を売却した際に税金を支払いますか？</div><div class="faq-a">保有期間と現地税法によっては税務上の影響が生じる場合があります。米国従業員は保有期間要件を満たした場合、特別な連邦所得税優遇措置を受けられる場合があります。税務専門家にご相談ください。</div>
<div class="faq-q">W-8BEN / W-9BENとは何ですか？記入する必要がありますか？</div><div class="faq-a"><strong>W-9BEN</strong>は米国納税者向けで、未提出の場合、売却代金および配当金に対して<strong>24%の米国税が源泉徴収</strong>されます。<strong>W-8BEN</strong>は非米国納税者向けの同等書類です。どちらもEquatePlus/EquateMobileで提出し、提出後第3暦年末に有効期限が切れます——期限前に更新してください。更新が必要な際はEquatePlusから通知されます。</div>
<div class="faq-q">ESPP失格処分（423b）とは何ですか？</div><div class="faq-a">セクション423計画のESPP株式を、付与日から2年超かつ購入日から1年超の保有期間を満たさずに売却した場合に失格処分となります。<strong>注：</strong>米国外の参加者は失格処分の報告義務はありません。</div>
<div class="faq-q">FTIN（外国税務識別番号）とは何ですか？</div><div class="faq-a">FTINはあなたの国の税務当局が割り当てた固有識別番号です。詳細はEquatePlusの税務フォームのFTINセクションの<strong>?</strong>をクリックしてください。</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#9997;", title:"9. その他",
        body:`<div class="faq-q">株券を申請できますか？</div><div class="faq-a">はい。Computershareに連絡して、口座内の一部または全部の完全株式の証書を申請してください。</div>
<div class="faq-q">ESPP株式の受益者を指定する必要がありますか？</div><div class="faq-a">いいえ。ESPPには「受益者」指定はありません。株式は自分の名義のみで購入するか、EquatePlusの<strong>個人設定</strong>から生存者権付きで家族と共同購入することができます。</div>
<div class="faq-q">海外転勤に伴いESPP参加を移管する必要があります。どうすればいいですか？</div><div class="faq-a">Computershareに直接お問い合わせください。</div>
<div class="faq-q">ESPP拠出の履歴を確認するにはどうすればいいですか？</div><div class="faq-a">EquatePlusで<strong>制度詳細</strong>に移動し、<strong>購入履歴</strong>を選択してください。</div>
<div class="faq-q">Computershareのサポートに関するフィードバックはどこで提供できますか？</div><div class="faq-a">Computershareのサポートで問題が解決しなかった場合や不快な経験をした場合は、<strong>AskHRチケット</strong>を作成してください。</div>
<div class="faq-q">ESPPポリシーと加入ガイドはどこで確認できますか？</div><div class="faq-a">IBMイントラネット：<strong>w3.ibm.com → グローバル報酬プログラム → ESPP → ESPP FAQ</strong>。資格要件、加入受付期間、拠出上限、購入日、脱退規則、FAQが含まれています。</div>` },
      {section:"resources",icon:"icon-purple",sym:"&#128279;",title:"役立つリンク・サポート窓口",body:`<ul class="resource-list"><li><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs" target="_blank" rel="noopener"><strong>ESPP w3 ページ</strong></a> — IBMイントラネットのプログラム詳細</li><li><a href="https://w3.ibm.com/hr/askhr/home" target="_blank" rel="noopener"><strong>AskHR</strong></a> — 加入手続き・書類・国固有の問題のチケット窓口</li><li><strong>SAP SuccessFactors – ベネフィットポートレット</strong> — ESPP加入・更新・確認</li><li><a href="https://www.na.equateplus.com/EquatePlusParticipant2/?login" target="_blank" rel="noopener"><strong>EquatePlus プラットフォーム</strong></a> — 購入後の株式管理</li></ul>`}
    ]
  },
  fr: {
    badge:"Avantages IBM", title:"Plan d'Achat d'Actions pour Employés (ESPP)", subtitle:"Guide du participant — inscription, gestion des cotisations, cas particuliers et FAQ",
    search:"Rechercher des sujets, mots-clés, pays…", noResults:"Aucun résultat trouvé. Essayez un autre mot-clé.",
    tabs:["Tous les sujets","Vue d'ensemble","Nouveaux participants","Participants existants","Vérifier l'inscription","Cas particuliers","FAQ","Ressources"],
    sections:{overview:"Vue d'ensemble du programme",new:"Nouveaux participants",existing:"Participants existants",check:"Vérification de l'inscription",special:"Cas particuliers",faq:"Foire aux questions",resources:"Ressources supplémentaires"},
    ceeCountries:["Croatie","Estonie","Lettonie","Pologne","Roumanie","Lituanie","Serbie","Venezuela"],
    approvalCountries:["Brésil","Italie","Croatie","Estonie","Lettonie","Pologne","Roumanie","Lituanie","Serbie"],
    cards:[
      { section:"overview", icon:"icon-blue", sym:"&#9733;", title:"Qu'est-ce que l'ESPP ?",
        body:`<p style="font-size:14px;color:#21272a;line-height:1.75;margin-top:8px;">Le <strong>Plan d'Achat d'Actions pour Employés (ESPP)</strong> permet aux employés IBM d'acheter des actions IBM avec une <strong>remise de 15 %</strong> sur le cours du marché. Les cotisations sont prélevées automatiquement sur le salaire — aucune transaction manuelle n'est nécessaire.</p>
<div class="info-box" style="margin-top:14px;"><strong>Fonctionnement :</strong> Vous cotisez 1 %–10 % de votre rémunération éligible chaque période de paie. IBM achète des actions en votre nom avec une remise de 15 % à la date d'achat. Les actions sont créditées sur votre compte EquatePlus.</div>
<div class="steps" style="margin-top:16px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Inscrivez-vous pendant une fenêtre (1–14 juin ou 1–14 décembre).</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Les retenues sur salaire débutent à la période d'offre suivante (1er janvier ou 1er juillet).</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">IBM achète des actions avec 15 % de remise à chaque date de paie.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">Les actions apparaissent sur votre compte EquatePlus en quelques jours à quelques semaines selon le pays.</div></div>
</div>` },
      { section:"overview", icon:"icon-green", sym:"&#36;", title:"Avantages et exemple",
        body:`<div class="section-heading" style="margin-top:10px;">Pourquoi s'inscrire ?</div>
<ul style="margin:0 0 14px 18px;font-size:13.5px;color:#21272a;line-height:1.8;">
<li>Achetez des actions IBM avec une <strong>remise de 15 %</strong> sur le cours du marché</li>
<li>Les retenues sur salaire rendent l'investissement automatique et facile</li>
<li>Avantage d'investissement immédiat grâce à la remise à l'achat</li>
<li>Possibilité de gains supplémentaires si le cours IBM monte</li>
<li>Éligible aux <strong>dividendes</strong> pendant la détention d'actions IBM</li>
<li>Devenez actionnaire IBM</li>
</ul>
<div class="section-heading">Exemple chiffré</div>
<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:6px;">
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;width:55%;">Salaire mensuel</td><td style="padding:7px 12px;border:1px solid #dde1e7;">4 000 $</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Cotisation (10 %)</td><td style="padding:7px 12px;border:1px solid #dde1e7;">400 $</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Prix marché de l'action IBM</td><td style="padding:7px 12px;border:1px solid #dde1e7;">130 $ / action</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Prix d'achat ESPP (−15 %)</td><td style="padding:7px 12px;border:1px solid #dde1e7;color:#0062ff;font-weight:600;">110,50 $ / action</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Actions achetées</td><td style="padding:7px 12px;border:1px solid #dde1e7;">3,62 actions</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Valeur de marché des actions</td><td style="padding:7px 12px;border:1px solid #dde1e7;">470,60 $</td></tr>
<tr style="background:#edf5ff;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">Rendement immédiat</td><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">17,6 %</td></tr>
</table>
<div class="note" style="margin-top:12px;"><strong>Remarque :</strong> Cet exemple est indicatif. Les cours réels et les rendements varieront.</div>` },
      { section:"overview", icon:"icon-purple", sym:"&#128196;", title:"Détails du plan",
        body:`<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:10px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Caractéristique</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Détails</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Remise</td><td style="padding:8px 12px;border:1px solid #dde1e7;">15 % sur le cours du marché à chaque date de paie</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Fourchette de cotisation</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1 % – 10 % de la rémunération éligible (% entier ou incréments de deux décimales)</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Plafond annuel</td><td style="padding:8px 12px;border:1px solid #dde1e7;">25 000 $ USD d'actions par année civile</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Plafond par période</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1 000 actions par période d'offre de 6 mois</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Achat minimum</td><td style="padding:8px 12px;border:1px solid #dde1e7;">Aucun</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Types de rémunération éligibles</td><td style="padding:8px 12px;border:1px solid #dde1e7;"><strong>Salaire de base</strong> — salaire régulier<br><strong>Autre rémunération</strong> — primes, commissions, incitations, rémunération variable</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Périodes d'offre</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1 janv. – 30 juin &nbsp;|&nbsp; 1 juil. – 31 déc.</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Fréquence d'achat</td><td style="padding:8px 12px;border:1px solid #dde1e7;">À chaque date de retenue sur salaire</td></tr>
</tbody></table>` },
      { section:"overview", icon:"icon-orange", sym:"&#36;&#36;", title:"Frais standard (Computershare)",
        body:`<p style="font-size:13.5px;color:#21272a;margin-top:8px;margin-bottom:12px;">Avant de vous inscrire, prenez connaissance des frais standard applicables via Computershare, le fournisseur mondial d'IBM.</p>
<table style="width:100%;border-collapse:collapse;font-size:13px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Transaction</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Frais (USD)</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Vente d'actions</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">19,95 $</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">Transfert vers un établissement financier</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Gratuit</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Frais de virement (US et non-US) — envoi du produit de la vente à la banque</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">35 $</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">Chèque USD pour dividendes ou actions vendues</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Gratuit</td></tr>
</tbody></table>
<div class="info-box" style="margin-top:12px;">Consultez également le <strong><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-prospectus" target="_blank" rel="noopener" style="color:#0043ce;">Prospectus</a></strong> et le <strong><a href="https://ibm.mystockoptions.com/global-tax-guide/?ibmtoken=SUJNVE9LRU4yNA==" target="_blank" rel="noopener" style="color:#0043ce;">Guide fiscal mondial</a></strong> avant l'inscription pour les implications fiscales par pays. Consultez un professionnel fiscal pour votre situation personnelle.</div>` },
      {section:"new",icon:"icon-blue",sym:"&#43;",title:"S'inscrire à l'ESPP",body:`<div class="info-box"><strong>Fenêtres d'inscription uniquement.</strong> Vous pouvez vous inscrire lors des deux fenêtres annuelles (juin et décembre). Votre signature électronique est requise.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Accédez au <strong>portlet Avantages SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Cliquez sur <strong>« Accéder à la vue d'ensemble des avantages »</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Sous <strong>« Inscriptions ouvertes »</strong>, sélectionnez <strong>ESPP – Déduction salaire de base IBM</strong> ou <strong>ESPP – Autre rémunération IBM</strong> et cliquez sur <strong>« S'inscrire »</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">La <strong>date d'effet</strong> est définie automatiquement selon le calendrier de paie de votre pays.</div></div><div class="step"><div class="step-num">5</div><div class="step-text">Saisissez votre <strong>pourcentage de cotisation (1–10 %)</strong>.</div></div><div class="step"><div class="step-num">6</div><div class="step-text">Sélectionnez <strong>« Oui »</strong> sous <em>J'accepte</em>, puis cliquez sur <strong>« Enregistrer »</strong>.</div></div></div><div class="note"><strong>Les deux plans ?</strong> Cliquez sur « S'inscrire » dans chaque plan séparément. L'« Autre rémunération » désigne généralement les paiements autres que le salaire de base et les indemnités de départ.</div>`},
      {section:"new",icon:"icon-green",sym:"&#10003;",title:"Ce qui se passe après l'inscription",body:`<div class="timeline"><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Fenêtre de décembre</div>Les premières déductions commencent en <strong>janvier</strong>.</div></div><div class="tl-item"><div class="tl-dot purple"></div><div class="tl-content"><div class="tl-label purple">Fenêtre de juin</div>Les premières déductions commencent en <strong>juillet</strong>.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Vérifier les déductions</div>Consultez vos <strong>bulletins de salaire dans SAP SuccessFactors</strong>.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Identifiants EquatePlus</div>Créés après le crédit de votre <strong>premier achat</strong>. Voir tableau ci-dessous.</div></div></div>
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:12px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Période d'offre</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Paie</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Livraison estimée des identifiants</th></tr></thead>
<tbody>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">Janvier</td><td style="padding:7px 10px;border:1px solid #dde1e7;">US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dans la semaine suivant le bulletin de janv. 15</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">Janvier</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Non-US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dans les 2 semaines suivant le bulletin de janvier</td></tr>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">Juillet</td><td style="padding:7px 10px;border:1px solid #dde1e7;">US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dans la semaine suivant le bulletin du 15 juil.</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">Juillet</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Non-US</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dans les 2 semaines suivant le bulletin de juillet</td></tr>
</tbody></table>
`},
      {section:"existing",icon:"icon-orange",sym:"&#8595;",title:"Réduire la cotisation / Se désinscrire",body:`<div class="info-box"><strong>Disponible à tout moment.</strong> Vous pouvez réduire votre cotisation ou vous désinscrire à tout moment.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Accédez au <strong>portlet Avantages SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Cliquez sur <strong>« Accéder à la vue d'ensemble »</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>Réduire :</strong> Onglet <strong>ESPP/Retraite</strong>, cliquez sur l'<strong>icône crayon</strong>, modifiez et enregistrez.</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>Se désinscrire :</strong> Cliquez sur <strong>« Se désinscrire »</strong>.</div></div></div>`},
      {section:"existing",icon:"icon-blue",sym:"&#8593;",title:"Augmenter la cotisation",body:`<div class="info-box"><strong>Fenêtres d'inscription uniquement.</strong> Vous ne pouvez augmenter votre cotisation que lors des fenêtres de juin ou décembre.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Accédez au <strong>portlet Avantages SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Cliquez sur <strong>« Accéder à la vue d'ensemble »</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Naviguez vers l'onglet <strong>« Inscription »</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Définissez la <strong>date d'effet</strong> et le <strong>pourcentage souhaité</strong>.</div></div><div class="step"><div class="step-num">5</div><div class="step-text">Sélectionnez <strong>« Oui »</strong> et cliquez sur <strong>« Enregistrer »</strong>.</div></div></div>`},
      {section:"check",icon:"icon-blue",sym:"&#128196;",title:"Option 1 — Portlet Avantages",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Accédez au <strong>portlet Avantages SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Cliquez sur <strong>« Vue d'ensemble des avantages »</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Sélectionnez <strong>ESPP/Retraite</strong>.</div></div></div>`},
      {section:"check",icon:"icon-purple",sym:"&#128203;",title:"Option 2 — Relevé de confirmation",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Accédez au <strong>portlet Avantages SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Cliquez sur <strong>« Voir le relevé d'avantages »</strong>.</div></div></div><div class="note"><strong>Récemment inscrit ?</strong> Définissez la <strong>« Date au »</strong> : <strong>1er juillet</strong> (fenêtre de juin) ou <strong>1er janvier</strong> de l'année suivante (fenêtre de décembre).</div>`},
      {section:"check",icon:"icon-green",sym:"&#9733;",title:"Option 3 — Onglet Rémunération totale",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Accédez à votre <strong>profil SAP SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Sélectionnez l'onglet <strong>« Rémunération totale »</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Vos choix ESPP apparaissent sous <strong>« Déduction récurrente »</strong>.</div></div></div>`},
      {section:"special",icon:"icon-red",sym:"&#9873;",title:"Pays CEE — Pièce jointe requise",cee:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Les employés des pays suivants doivent soumettre un formulaire complété :</p>{{CEE_TAGS}}<div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Téléchargez le formulaire depuis la fenêtre d'inscription SuccessFactors.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Remplissez-le en vous assurant que les informations <strong>correspondent à votre inscription</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Rattachez le formulaire complété dans SuccessFactors.</div></div></div><div class="note"><strong>Impossible de télécharger ?</strong> Problème connu. Ouvrez un <strong>ticket AskHR</strong>.</div>`},
      {section:"special",icon:"icon-blue",sym:"&#127470;&#127481;",title:"Italie — Compte WeBank requis",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Les employés en Italie doivent remplir une condition supplémentaire avant de s'inscrire à l'ESPP.</p><div class="info-box" style="margin-top:10px;">Les employés doivent disposer à la fois d'un <strong>compte courant WeBank</strong> et d'un <strong>compte d'investissement</strong> pour participer à l'ESPP.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Consultez le guide détaillé pour les employés en Italie : <a href="https://w3.ibm.com/hr/policy/it-compensation-espp" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/hr/policy/it-compensation-espp</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Ouvrez votre <strong>compte courant WeBank</strong> et votre <strong>compte d'investissement</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Complétez votre <strong>profil bancaire dans WeBank</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Une fois les comptes ouverts et le profil bancaire complété, poursuivez les étapes standard d'inscription à l'ESPP.</div></div></div>`},
      {section:"special",icon:"icon-green",sym:"&#127463;&#127479;",title:"Brésil — Validation Intercam requise",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Les approbations ESPP pour le Brésil sont strictement basées sur la liste de confirmation officielle fournie par <strong>Intercam</strong>. Toutes les demandes doivent être validées par Intercam.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">Contactez Intercam directement pour demander le formulaire ESPP :<br><a href="mailto:janvion@intercam.com.br" style="color:#0062ff;">janvion@intercam.com.br</a> &nbsp;|&nbsp; <a href="mailto:mcrippa@intercam.com.br" style="color:#0062ff;">mcrippa@intercam.com.br</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Remplissez le formulaire ESPP Intercam pour qu'ils puissent valider votre demande et vous ajouter à leur liste officielle.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Une fois confirmé par Intercam, le <strong>partenaire ESPP approuvera la transaction dans SuccessFactors</strong>.</div></div></div>`},
      {section:"special",icon:"icon-purple",sym:"&#127479;&#127476;",title:"Roumanie — Signature électronique IBM Adobe",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Le formulaire ESPP pour la Roumanie nécessite une <strong>signature électronique IBM Adobe</strong>.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">Accédez à la signature électronique IBM : <a href="https://ibm.eu1.adobesign.com/account/homeJS" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ibm.eu1.adobesign.com</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Pas d'accès ? Faites une demande ici : <a href="https://w3.ibm.com/w3publisher/adobe-sign/how-to-get-access" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/w3publisher/adobe-sign/how-to-get-access</a></div></div></div>`},
      {section:"special",icon:"icon-orange",sym:"&#9997;",title:"Croatie, Lituanie, Pologne et Serbie — Signature manuscrite",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Le formulaire ESPP pour les pays suivants nécessite une <strong>signature manuscrite (physique)</strong> :</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croatie</span><span class="tag">Lituanie</span><span class="tag">Pologne</span><span class="tag">Serbie</span></div><div class="info-box">Assurez-vous que le formulaire est signé physiquement avant de le soumettre dans SuccessFactors lors de votre inscription.</div>`},
      {section:"special",icon:"icon-red",sym:"&#128683;",title:"Croatie, Lituanie, Pologne et Serbie — Se désinscrire du ESPP",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Les employés des pays suivants doivent effectuer une étape supplémentaire lors de la désinscription du ESPP :</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croatie</span><span class="tag">Lituanie</span><span class="tag">Pologne</span><span class="tag">Serbie</span></div><div class="info-box" style="margin-top:12px;">Une fois la transaction de <strong>désinscription</strong> effectuée dans SuccessFactors, vous recevrez un e-mail contenant le formulaire ESPP. Remplissez le formulaire et téléchargez-le dans <strong>OpenText</strong>.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Effectuez la <strong>désinscription</strong> dans SuccessFactors.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Consultez votre e-mail pour le formulaire ESPP envoyé après confirmation.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Remplissez le formulaire de manière complète et précise.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Téléchargez le formulaire complété dans OpenText. Consultez le guide : <a href="https://ibm.box.com/s/9ev95b9x1eypipm0n7hc53uc0q4rotmf" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">Comment télécharger des documents ESPP dans OpenText</a></div></div></div>`},


      {section:"special",icon:"icon-orange",sym:"&#9203;",title:"Pays nécessitant une approbation supplémentaire",approval:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Dans ces pays, votre choix ESPP ne sera <strong>pas visible</strong> jusqu'à l'approbation :</p>{{APPROVAL_TAGS}}<div class="info-box" style="margin-top:14px;">C'est normal. Contactez <strong>AskHR</strong> si votre choix reste invisible après la clôture de la fenêtre.</div>`},
      { section:"faq", icon:"icon-blue", sym:"&#128101;", title:"1. Participation",
        body:`<div class="faq-q">Qui peut participer à l'ESPP ?</div><div class="faq-a">Tous les IBMers réguliers, y compris les temps partiels, et la plupart des employés supplémentaires, à condition qu'ils résident dans un pays où la participation est autorisée. <strong>Amériques :</strong> Argentine, Bahamas, Barbade, Brésil, Canada, Chili, Colombie, Costa Rica, Curaçao, Équateur, Jamaïque, Mexique, Pérou, Trinité, Uruguay, États-Unis, Venezuela. <strong>Asie-Pacifique :</strong> Australie, Chine, Hong Kong, Inde, Japon, Malaisie, Nouvelle-Zélande, Philippines, Singapour, Corée du Sud, Taïwan, Thaïlande. <strong>EMEA :</strong> Autriche, Belgique, Bulgarie, Chypre, Tchéquie, Croatie, Danemark, Égypte, Estonie, Finlande, France, Allemagne, Grèce, Hongrie, Irlande, Israël, Italie, Lettonie, Lituanie, Luxembourg, Pays-Bas, Norvège, Pakistan, Pologne, Portugal, Qatar, Roumanie, Arabie Saoudite, Serbie, Slovaquie, Slovénie, Afrique du Sud, Espagne, Suède, Suisse, Türkiye, EAU, Royaume-Uni.</div>
<div class="faq-q">Que faire si j'ai une demande d'inscription ESPP en attente ?</div><div class="faq-a">Vous devez retirer toute demande en attente avant d'en soumettre une nouvelle. SAP SuccessFactors ne permet pas une nouvelle soumission tant que la demande précédente n'est pas effacée. Vérifiez votre liste <strong>À faire</strong> pour les demandes renvoyées qui doivent également être retirées.</div>
<div class="faq-q">Si je suis déjà inscrit, dois-je me réinscrire ?</div><div class="faq-a">En général non. Vous devez vous réinscrire si : vous revenez d'un congé ; vous avez été suspendu ; ou vous atteignez le maximum annuel de <strong>25 000 $ USD</strong> d'actions ou <strong>1 000 actions</strong> par période d'offre. Les paies US sont réinscrites automatiquement ; les non-US doivent se réinscrire manuellement.</div>
<div class="faq-q">Je suis une nouvelle recrue — combien de temps dois-je attendre pour m'inscrire ?</div><div class="faq-a">Dès que vous êtes officiellement intégré et remplissez les critères d'éligibilité, vous pouvez vous inscrire lors de la prochaine fenêtre (1–14 juin ou 1–14 décembre).</div>
<div class="faq-q">J'ai été transféré définitivement entre entités IBM. Comment cela affecte-t-il l'ESPP ?</div><div class="faq-a">Vos cotisations ne continuent pas automatiquement. Vous devez vous réinscrire lors de la prochaine fenêtre mondiale. Si le transfert est temporaire (ex. : mission Global IBMer), les cotisations continuent dans le pays où la paie est traitée.</div>
<div class="faq-q">J'ai manqué la fenêtre d'inscription. Puis-je encore rejoindre ?</div><div class="faq-a">Non — l'inscription n'est possible que pendant les deux fenêtres désignées chaque année : <strong>1 janv.–30 juin</strong> (inscription 1–14 déc.) et <strong>1 juil.–31 déc.</strong> (inscription 1–14 juin). Vous devez attendre la prochaine fenêtre.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#36;", title:"2. Rémunération éligible et retenues sur salaire",
        body:`<div class="faq-q">Combien puis-je cotiser ?</div><div class="faq-a">De <strong>1 % à 10 %</strong> de votre salaire, dans les limites du plan et de la réglementation. Maximum : <strong>25 000 $ d'actions par année civile</strong> et au maximum <strong>1 000 actions</strong> par période d'offre. Aux États-Unis, les retenues ESPP sont effectuées après la plupart des autres retenues ; les retenues partielles ne sont pas autorisées.</div>
<div class="faq-q">Puis-je définir des pourcentages différents pour différents types de rémunération ?</div><div class="faq-a">Oui. Vous pouvez autoriser des retenues sur le <strong>Salaire de base IBM</strong> (rémunération régulière, commissions récurrentes, indemnités de congés, STD) et/ou sur l'<strong>Autre rémunération IBM</strong> (incitations, rémunération variable, commissions). Chaque taux doit être compris entre 1 % et 10 %.</div>
<div class="faq-q">Puis-je modifier mes cotisations après la fermeture de la fenêtre d'inscription ?</div><div class="faq-a">Vous pouvez <strong>augmenter ou diminuer</strong> pendant une fenêtre d'inscription. Après la fermeture, vous pouvez encore <strong>diminuer</strong> à tout moment pendant la période d'offre, mais ne pouvez pas <strong>augmenter</strong> avant la prochaine fenêtre. Vous pouvez vous retirer à tout moment.</div>
<div class="faq-q">Comment est déterminé le prix d'achat de l'action IBM ?</div><div class="faq-a">Le prix est <strong>85 % de la moyenne du cours le plus haut et le plus bas d'IBM</strong> à chaque date de paie — vous accordant une <strong>remise de 15 %</strong> sur chaque achat.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#8801;", title:"3. Plateforme EquatePlus",
        body:`<div class="faq-q">Je ne peux pas accéder à mon compte EquatePlus. Que faire ?</div><div class="faq-a">Cliquez sur le lien <strong>Aide</strong> sur la page de connexion EquatePlus et suivez les instructions. Cette page indique les coordonnées du centre d'appels de Computershare.</div>
<div class="faq-q">Pourquoi ai-je à la fois un compte EquatePlus et un compte Investor Center ?</div><div class="faq-a">Cela se produit généralement lorsque vous détenez des certificats d'actions papier — un compte avec des certificats papier ne peut pas être fusionné avec un compte dématérialisé tant que les certificats ne sont pas récupérés. Contactez <strong>infoibm@us.ibm.com</strong> pour une aide à la consolidation.</div>
<div class="faq-q">Pourquoi mes prénom et nom sont-ils inversés dans EquatePlus ?</div><div class="faq-a">Les noms sont mis à jour par des fichiers mensuels/bimestriels d'IBM. Créez un <strong>ticket AskHR</strong> pour que le prochain fichier corresponde à votre profil SAP SuccessFactors.</div>
<div class="faq-q">Comment mettre à jour mon adresse et mes informations personnelles dans EquatePlus ?</div><div class="faq-a">Les informations des employés actifs sont mises à jour via des fichiers entrants vers Computershare. Les employés résiliés doivent contacter Computershare directement.</div>
<div class="faq-q">Combien de temps après les retenues les actions apparaissent-elles dans EquatePlus ?</div><div class="faq-a">IBM achète des actions à chaque date de retenue sur salaire. Le délai d'affichage varie selon les pays :
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:8px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">Délai</th><th style="padding:6px 10px;border:1px solid #dde1e7;color:#697077;">Pays</th></tr></thead>
<tbody>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">1–10 jours</td><td style="padding:6px 10px;border:1px solid #dde1e7;">Argentine, Canada, Costa Rica, France, Allemagne, Lettonie, Mexique, Pays-Bas, Pakistan, Roumanie, Singapour, Corée du Sud, Espagne, Suède, Suisse, Trinité, Royaume-Uni, États-Unis</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">10–20 jours</td><td style="padding:6px 10px;border:1px solid #dde1e7;">Autriche, Barbade, Belgique, Brésil, Bulgarie, Chili, Colombie, Tchéquie, Équateur, Égypte, Estonie, Finlande, Hong Kong, Hongrie, Inde, Irlande, Israël, Jamaïque, Lituanie, Malaisie, Nouvelle-Zélande, Pérou, Philippines, Pologne, Portugal, Qatar, Arabie Saoudite, Serbie, Slovaquie, Slovénie, Afrique du Sud, Taïwan, Thaïlande, Turquie, EAU, Uruguay, Venezuela</td></tr>
<tr><td style="padding:6px 10px;border:1px solid #dde1e7;font-weight:600;white-space:nowrap;">20+ jours</td><td style="padding:6px 10px;border:1px solid #dde1e7;">Australie, Chine, Croatie, Chypre, Danemark, Grèce, Japon, Norvège</td></tr>
</tbody></table>
<div class="note" style="margin-top:8px;">Les retards sont surveillés par IBM et EquatePlus. Les mises à jour sont publiées sur <strong>#espp-ibmshare</strong> sur Slack ou envoyées par e-mail aux participants.</div></div>` },
      { section:"faq", icon:"icon-orange", sym:"&#9401;", title:"4. Suspension et départ d'IBM",
        body:`<div class="faq-q">Que deviennent mes actions si je me retire, prends ma retraite ou quitte IBM ?</div><div class="faq-a">Les actions restent dans votre compte participant IBM chez Computershare jusqu'à ce que vous les demandiez ou autorisiez leur vente. Si vous quittez IBM, mettez à jour votre adresse e-mail chez Computershare avec une <strong>adresse non-IBM</strong> pour continuer à recevoir les communications.</div>
<div class="faq-q">Je me suis désinscrit mais l'ESPP a quand même été prélevé. Pourquoi ?</div><div class="faq-a">Il peut s'agir d'un problème de synchronisation. Vérifiez dans SuccessFactors que votre participation a bien été résiliée. Si les retenues continuent, contactez directement <strong>Computershare</strong>.</div>
<div class="faq-q">Pourquoi ma retenue ESPP s'est-elle arrêtée ? Je vois un « remboursement ESPP » sur mon bulletin de salaire.</div><div class="faq-a">La suspension peut survenir en raison d'un congé ; l'atteinte du plafond annuel de 25 000 $ ou de 1 000 actions par période d'offre ; ou l'atteinte du plafond total d'actions de la période d'offre.</div>
<div class="faq-q">Le rétablissement après suspension est-il automatique ?</div><div class="faq-a"><strong>Paie US :</strong> Le rétablissement est automatique pour les plafonds 25 000 $/1 000 actions et lors du retour de congé. <strong>Paie non-US :</strong> Il est recommandé de se réinscrire manuellement lors de la prochaine fenêtre — la gestion varie selon le pays et toutes les paies ne procèdent pas à la réinscription automatique.</div>` },
      { section:"faq", icon:"icon-blue", sym:"&#128200;", title:"6. Consultation, vente et transfert d'actions",
        body:`<div class="faq-q">Comment consulter et gérer mes actions dans EquatePlus ?</div><div class="faq-a">Connectez-vous à EquatePlus et utilisez les menus <strong>Vue d'ensemble</strong>, <strong>Bibliothèque</strong> et <strong>Aide</strong>.</div>
<div class="faq-q">Je vois la retenue ESPP sur mon bulletin de salaire mais pas les actions dans EquatePlus. Pourquoi ?</div><div class="faq-a">Pour les paies non-US, les dates de paie tombent en fin de mois et il peut falloir <strong>2 à 3 semaines</strong> à l'équipe de paie locale pour envoyer les instructions d'achat à Computershare. Les retenues de fin de mois peuvent ne pas apparaître avant la mi-mois suivant.</div>
<div class="faq-q">Comment vendre mes actions ?</div><div class="faq-a">Soumettez des demandes de vente via <strong>EquatePlus</strong> ou <strong>EquateMobile</strong> 24h/24, 7j/7. Paiement disponible dans plus de 100 devises. Contact Computershare : <strong>1-888-426-6700</strong> (US/Canada/Porto Rico) ou <strong>781-575-2727</strong> (international). Frais de transaction : environ 19,95 $ par vente.</div>
<div class="faq-q">Combien de temps dois-je conserver les actions avant de les vendre ?</div><div class="faq-a">Vous pouvez vendre à tout moment après le crédit des actions sur EquatePlus. Des conséquences fiscales peuvent s'appliquer selon la durée de détention et les lois fiscales locales. Les employés US peuvent bénéficier d'un traitement fiscal fédéral spécial pour les cessions qualifiées.</div>
<div class="faq-q">Comment transférer des actions vers un établissement financier ?</div><div class="faq-a">Ajoutez votre compte de courtage sous <strong>Préférences financières</strong> dans EquatePlus, puis cliquez sur <strong>Transaction</strong> sur la page d'accueil pour soumettre un transfert vers un courtier. Ni Computershare ni IBM ne facture de frais de transfert — les frais éventuels proviennent du courtier destinataire. Seuls les courtiers membres DTC sont pris en charge.</div>
<div class="faq-q">Comment fonctionne la conversion de devises lors de la vente d'actions ?</div><div class="faq-a">Vous obtenez un taux bancaire de détail qui peut inclure <strong>jusqu'à 3 % de frais</strong> sur le produit, selon le marché de négociation et la valeur de la transaction.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#127987;", title:"7. Dividendes",
        body:`<div class="faq-q">Comment mes dividendes sont-ils versés ?</div><div class="faq-a">Vous disposez de trois options selon les actions détenues : <strong>(1) Réinvestissement automatique</strong> (option par défaut pour les inscrits depuis le 1er janv. 2023) — réinvesti en actions IBM à la valeur de marché ; frais : 2 % ou max 3 $ par dividende. <strong>(2) Virement électronique</strong> vers votre banque/courtier par ACH ou virement (frais possibles). <strong>(3) Chèque USD</strong> — envoyé uniquement si aucun relevé bancaire n'est enregistré. Les employés non-US peuvent choisir des dividendes en monnaie locale en ajoutant leurs coordonnées de virement sur EquatePlus (sous réserve de 10 $ de frais de virement).</div>` },
      { section:"faq", icon:"icon-red", sym:"&#128203;", title:"8. Fiscalité",
        body:`<div class="faq-q">Dois-je payer des impôts lorsque des actions sont achetées en mon nom ?</div><div class="faq-a">Dans de nombreux pays, vous êtes imposé sur la remise que vous recevez lors des achats d'actions. L'impôt peut être retenu par la paie locale ou vous pouvez en être responsable. Certifiez via le <strong>formulaire W-9BEN</strong> (US) ou <strong>W-8BEN</strong> (non-US) sur EquatePlus pour éviter une retenue excessive.</div>
<div class="faq-q">Dois-je payer des impôts lors de la vente de mes actions ?</div><div class="faq-a">Des conséquences fiscales peuvent s'appliquer selon la durée de détention et les lois fiscales locales. Les employés US peuvent bénéficier d'un traitement fiscal fédéral spécial si les actions sont détenues pendant la période requise. Consultez un professionnel fiscal.</div>
<div class="faq-q">Qu'est-ce qu'un W-8BEN / W-9BEN et dois-je en remplir un ?</div><div class="faq-a">Le <strong>W-9BEN</strong> est pour les contribuables américains ; son absence entraîne une <strong>retenue fiscale américaine de 24 %</strong> sur le produit des ventes et les dividendes. Le <strong>W-8BEN</strong> est l'équivalent pour les non-américains. Les deux sont soumis via EquatePlus/EquateMobile et expirent à la fin de la troisième année civile suivant leur remplissage — renouvelez avant expiration. EquatePlus vous rappellera quand le renouvellement est nécessaire.</div>
<div class="faq-q">Qu'est-ce qu'une cession disqualifiante ESPP (423b) ?</div><div class="faq-a">Une cession disqualifiante survient lorsque vous vendez des actions ESPP d'un plan Section 423 sans respecter les périodes de détention : plus de 2 ans à partir de la date d'attribution ET plus d'1 an à partir de la date d'achat. <strong>Remarque :</strong> Les participants hors États-Unis ne sont pas soumis à l'obligation de déclaration des cessions disqualifiantes.</div>
<div class="faq-q">Qu'est-ce que mon FTIN (Numéro d'identification fiscale étranger) ?</div><div class="faq-a">Un FTIN est un identifiant unique attribué par l'autorité fiscale de votre pays. Pour plus de détails, cliquez sur le <strong>?</strong> dans la section FTIN du formulaire fiscal d'EquatePlus.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#9997;", title:"9. Divers",
        body:`<div class="faq-q">Puis-je demander des certificats d'actions ?</div><div class="faq-a">Oui. Contactez Computershare pour demander un certificat pour tout ou partie des actions entières de votre compte.</div>
<div class="faq-q">Dois-je désigner un bénéficiaire pour mes actions ESPP ?</div><div class="faq-a">Non. Il n'y a pas de désignation de « bénéficiaire ». Vous pouvez acheter des actions uniquement en votre nom, ou conjointement avec un membre de la famille avec droit de survie via EquatePlus sous <strong>Préférences personnelles</strong>.</div>
<div class="faq-q">Je dois transférer ma participation ESPP en raison d'un déménagement international. Comment ?</div><div class="faq-a">Contactez directement Computershare.</div>
<div class="faq-q">Comment obtenir l'historique de toutes mes cotisations ESPP ?</div><div class="faq-a">Naviguez vers <strong>Détails du plan</strong> dans EquatePlus et sélectionnez <strong>Achats archivés</strong>.</div>
<div class="faq-q">Où puis-je donner mon avis sur le support de Computershare ?</div><div class="faq-a">Créez un <strong>ticket AskHR</strong> si votre problème avec le support de Computershare n'a pas été résolu ou si vous avez eu une expérience négative.</div>
<div class="faq-q">Où puis-je trouver la politique ESPP et le guide d'inscription ?</div><div class="faq-a">Sur l'intranet IBM : <strong>w3.ibm.com → Programmes de rémunération mondiaux → ESPP → FAQ ESPP</strong>. Comprend l'éligibilité, les fenêtres d'inscription, les plafonds de cotisation, les dates d'achat, les règles de retrait et les FAQ.</div>` },
      {section:"resources",icon:"icon-purple",sym:"&#128279;",title:"Liens utiles et support",body:`<ul class="resource-list"><li><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs" target="_blank" rel="noopener"><strong>Page ESPP w3</strong></a> — Détails du programme sur l'intranet IBM</li><li><a href="https://w3.ibm.com/hr/askhr/home" target="_blank" rel="noopener"><strong>AskHR</strong></a> — Ouvrir un ticket pour toute question</li><li><strong>SAP SuccessFactors – Portlet Avantages</strong> — Inscription, mise à jour, consultation</li><li><a href="https://www.na.equateplus.com/EquatePlusParticipant2/?login" target="_blank" rel="noopener"><strong>Plateforme EquatePlus</strong></a> — Gestion des actions après achat</li></ul>`}
    ]
  },
  es: {
    badge:"Beneficios IBM", title:"Plan de Compra de Acciones para Empleados (ESPP)", subtitle:"Guía del participante — inscripción, gestión de contribuciones, casos especiales y preguntas frecuentes",
    search:"Buscar temas, palabras clave, países…", noResults:"No se encontraron resultados. Intente con otra palabra clave.",
    tabs:["Todos los temas","Descripción general","Nuevos participantes","Participantes actuales","Verificar inscripción","Casos especiales","Preguntas frecuentes","Recursos"],
    sections:{overview:"Descripción general del programa",new:"Nuevos participantes",existing:"Participantes actuales",check:"Verificación de inscripción",special:"Casos especiales",faq:"Preguntas frecuentes",resources:"Recursos adicionales"},
    ceeCountries:["Croacia","Estonia","Letonia","Polonia","Rumanía","Lituania","Serbia","Venezuela"],
    approvalCountries:["Brasil","Italia","Croacia","Estonia","Letonia","Polonia","Rumanía","Lituania","Serbia"],
    cards:[
      { section:"overview", icon:"icon-blue", sym:"&#9733;", title:"¿Qué es el ESPP?",
        body:`<p style="font-size:14px;color:#21272a;line-height:1.75;margin-top:8px;">El <strong>Plan de Compra de Acciones para Empleados (ESPP)</strong> permite a los empleados de IBM comprar acciones de IBM con un <strong>descuento del 15 %</strong> sobre el precio de mercado. Las contribuciones se realizan automáticamente mediante deducciones de nómina, sin necesidad de transacciones manuales.</p>
<div class="info-box" style="margin-top:14px;"><strong>Cómo funciona:</strong> Usted contribuye del 1 % al 10 % de su compensación elegible cada período de pago. IBM compra acciones en su nombre con un descuento del 15 % en la fecha de compra. Las acciones se acreditan en su cuenta de EquatePlus.</div>
<div class="steps" style="margin-top:16px;">
<div class="step"><div class="step-num">1</div><div class="step-text">Inscríbase durante una ventana (1–14 de junio o 1–14 de diciembre).</div></div>
<div class="step"><div class="step-num">2</div><div class="step-text">Las deducciones de nómina comienzan en el siguiente período de oferta (1 de enero o 1 de julio).</div></div>
<div class="step"><div class="step-num">3</div><div class="step-text">IBM compra acciones con un descuento del 15 % en cada fecha de nómina.</div></div>
<div class="step"><div class="step-num">4</div><div class="step-text">Las acciones aparecen en su cuenta de EquatePlus en días o semanas según el país.</div></div>
</div>` },
      { section:"overview", icon:"icon-green", sym:"&#36;", title:"Beneficios y ejemplo",
        body:`<div class="section-heading" style="margin-top:10px;">¿Por qué inscribirse?</div>
<ul style="margin:0 0 14px 18px;font-size:13.5px;color:#21272a;line-height:1.8;">
<li>Compre acciones de IBM con un <strong>descuento del 15 %</strong> sobre el precio de mercado</li>
<li>Las deducciones de nómina hacen que invertir sea automático y sencillo</li>
<li>Ventaja de inversión inmediata gracias al descuento en la compra</li>
<li>Posibilidad de obtener rendimientos adicionales si el precio de la acción IBM sube</li>
<li>Elegible para recibir <strong>dividendos</strong> mientras se posean acciones IBM</li>
<li>Conviértase en accionista de IBM</li>
</ul>
<div class="section-heading">Ejemplo ilustrativo</div>
<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:6px;">
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;width:55%;">Salario mensual</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$4,000</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Contribución (10 %)</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$400</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Precio de mercado de la acción IBM</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$130 / acción</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Precio de compra ESPP (−15 %)</td><td style="padding:7px 12px;border:1px solid #dde1e7;color:#0062ff;font-weight:600;">$110.50 / acción</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Acciones compradas</td><td style="padding:7px 12px;border:1px solid #dde1e7;">3.62 acciones</td></tr>
<tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Valor de mercado de las acciones</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$470.60</td></tr>
<tr style="background:#edf5ff;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">Rendimiento inmediato</td><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">17.6 %</td></tr>
</table>
<div class="note" style="margin-top:12px;"><strong>Nota:</strong> Este ejemplo es ilustrativo. Los precios reales y los rendimientos variarán.</div>` },
      { section:"overview", icon:"icon-purple", sym:"&#128196;", title:"Detalles del plan",
        body:`<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:10px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Característica</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Detalles</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Descuento</td><td style="padding:8px 12px;border:1px solid #dde1e7;">15 % sobre el precio de mercado en cada fecha de compra de nómina</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Rango de contribución</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1 % – 10 % de la compensación elegible (porcentaje entero o incrementos de dos decimales)</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Límite anual</td><td style="padding:8px 12px;border:1px solid #dde1e7;">$25,000 USD en acciones por año calendario</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Límite por período</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1,000 acciones por período de oferta de 6 meses</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Compra mínima</td><td style="padding:8px 12px;border:1px solid #dde1e7;">Ninguna</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Tipos de pago elegibles</td><td style="padding:8px 12px;border:1px solid #dde1e7;"><strong>Salario base</strong> — salario regular<br><strong>Otra compensación</strong> — bonos, comisiones, incentivos, pago variable</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Períodos de oferta</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1 ene – 30 jun &nbsp;|&nbsp; 1 jul – 31 dic</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Frecuencia de compra</td><td style="padding:8px 12px;border:1px solid #dde1e7;">En cada fecha de deducción de nómina</td></tr>
</tbody></table>` },
      { section:"overview", icon:"icon-orange", sym:"&#36;&#36;", title:"Tarifas estándar (Computershare)",
        body:`<p style="font-size:13.5px;color:#21272a;margin-top:8px;margin-bottom:12px;">Antes de inscribirse, conozca las tarifas estándar del ESPP a través de Computershare, el proveedor global de IBM.</p>
<table style="width:100%;border-collapse:collapse;font-size:13px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Transacción</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Tarifa (USD)</th></tr></thead>
<tbody>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Venta de acciones</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$19.95</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">Transferencia a una institución financiera</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Sin cargo</td></tr>
<tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Tarifa de transferencia bancaria (EE.UU. y no EE.UU.) — envío de ganancias a banco</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$35</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">Cheque en USD por dividendos o acciones vendidas</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Sin cargo</td></tr>
</tbody></table>
<div class="info-box" style="margin-top:12px;">Consulte también el <strong><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-prospectus" target="_blank" rel="noopener" style="color:#0043ce;">Prospecto</a></strong> y la <strong><a href="https://ibm.mystockoptions.com/global-tax-guide/?ibmtoken=SUJNVE9LRU4yNA==" target="_blank" rel="noopener" style="color:#0043ce;">Guía fiscal global</a></strong> antes de inscribirse para conocer las implicaciones fiscales por país. Consulte a un profesional fiscal para asesoramiento específico.</div>` },
      {section:"new",icon:"icon-blue",sym:"&#43;",title:"Inscribirse en el ESPP",body:`<div class="info-box"><strong>Solo en ventanas de inscripción.</strong> Puede inscribirse durante las dos ventanas anuales (junio y diciembre). Se requiere firma electrónica.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acceda al <strong>portlet de Beneficios de SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Haga clic en <strong>«Ir a Resumen de beneficios»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">En <strong>«Inscripciones abiertas»</strong>, seleccione <strong>ESPP – Deducción de salario base de IBM</strong> o <strong>ESPP – Otra compensación de IBM</strong> y haga clic en <strong>«Inscribirse»</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">La <strong>fecha de vigencia</strong> se establece automáticamente según el calendario de nómina de su país.</div></div><div class="step"><div class="step-num">5</div><div class="step-text">Ingrese el <strong>porcentaje de contribución del empleado (1–10 %)</strong>.</div></div><div class="step"><div class="step-num">6</div><div class="step-text">Seleccione <strong>«Sí»</strong> bajo <em>Acepto</em> y haga clic en <strong>«Guardar»</strong>.</div></div></div><div class="note"><strong>¿Ambos planes?</strong> Haga clic en «Inscribirse» en cada plan por separado. La «Otra compensación» generalmente incluye pagos que no son salario base ni indemnizaciones.</div>`},
      {section:"new",icon:"icon-green",sym:"&#10003;",title:"Qué esperar después de la inscripción",body:`<div class="timeline"><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Ventana de diciembre</div>Las primeras deducciones comienzan en <strong>enero</strong>.</div></div><div class="tl-item"><div class="tl-dot purple"></div><div class="tl-content"><div class="tl-label purple">Ventana de junio</div>Las primeras deducciones comienzan en <strong>julio</strong>.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Verificar deducciones</div>Revise sus <strong>recibos de nómina en SAP SuccessFactors</strong>.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Credenciales EquatePlus</div>Creadas tras el crédito de su <strong>primera compra</strong>. Ver tabla abajo.</div></div></div>
<table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:12px;">
<thead><tr style="background:#f2f4f8;"><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Período de oferta</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Nómina</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Entrega estimada de credenciales</th></tr></thead>
<tbody>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">Enero</td><td style="padding:7px 10px;border:1px solid #dde1e7;">EE.UU.</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dentro de 1 semana del recibo de nómina del 15 de enero</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">Enero</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Fuera de EE.UU.</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dentro de 2 semanas del recibo de nómina de enero</td></tr>
<tr><td style="padding:7px 10px;border:1px solid #dde1e7;">Julio</td><td style="padding:7px 10px;border:1px solid #dde1e7;">EE.UU.</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dentro de 1 semana del recibo de nómina del 15 de julio</td></tr>
<tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">Julio</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Fuera de EE.UU.</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Dentro de 2 semanas del recibo de nómina de julio</td></tr>
</tbody></table>
`},
      {section:"existing",icon:"icon-orange",sym:"&#8595;",title:"Reducir contribución / Darse de baja",body:`<div class="info-box"><strong>Disponible en cualquier momento.</strong> Puede reducir su contribución o darse de baja en cualquier momento del año.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acceda al <strong>portlet de Beneficios de SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Haga clic en <strong>«Ir a Resumen de beneficios»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>Para reducir:</strong> Pestaña <strong>ESPP/Pensiones</strong>, haga clic en el <strong>ícono de lápiz</strong>, actualice y guarde.</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>Para darse de baja:</strong> Haga clic en <strong>«Darse de baja»</strong>.</div></div></div>`},
      {section:"existing",icon:"icon-blue",sym:"&#8593;",title:"Aumentar la contribución",body:`<div class="info-box"><strong>Solo en ventanas de inscripción.</strong> Solo puede aumentar su contribución durante las ventanas de junio o diciembre.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acceda al <strong>portlet de Beneficios</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Haga clic en <strong>«Ir a Resumen de beneficios»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Vaya a la pestaña <strong>«Inscripción»</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Configure la <strong>fecha de vigencia</strong> y el <strong>porcentaje deseado</strong>.</div></div><div class="step"><div class="step-num">5</div><div class="step-text">Seleccione <strong>«Sí»</strong> y haga clic en <strong>«Guardar»</strong>.</div></div></div>`},
      {section:"check",icon:"icon-blue",sym:"&#128196;",title:"Opción 1 — Portlet de Beneficios",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acceda al <strong>portlet de Beneficios de SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Haga clic en <strong>«Ir a Resumen»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Seleccione <strong>ESPP/Pensiones</strong>.</div></div></div>`},
      {section:"check",icon:"icon-purple",sym:"&#128203;",title:"Opción 2 — Estado de confirmación de beneficios",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acceda al <strong>portlet de Beneficios de SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Haga clic en <strong>«Ver estado de beneficios»</strong>.</div></div></div><div class="note"><strong>¿Inscripción reciente?</strong> Establezca la <strong>«Fecha hasta»</strong>: <strong>1 de julio</strong> (ventana de junio) o <strong>1 de enero</strong> del año siguiente (ventana de diciembre).</div>`},
      {section:"check",icon:"icon-green",sym:"&#9733;",title:"Opción 3 — Pestaña de Remuneración total",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Vaya a su <strong>perfil de SAP SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Seleccione la pestaña <strong>«Remuneración total»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Sus elecciones ESPP aparecen en <strong>«Deducción recurrente»</strong>.</div></div></div>`},
      {section:"special",icon:"icon-red",sym:"&#9873;",title:"Países CEE — Se requiere adjunto",cee:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Los empleados de los siguientes países deben adjuntar un formulario completado:</p>{{CEE_TAGS}}<div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Descargue el formulario desde la ventana de inscripción de SuccessFactors.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Complételo asegurándose de que los datos <strong>coincidan con su inscripción</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Vuelva a adjuntarlo en SuccessFactors.</div></div></div><div class="note"><strong>¿No puede descargarlo?</strong> Es un problema conocido. Abra un <strong>ticket en AskHR</strong>.</div>`},
      {section:"special",icon:"icon-orange",sym:"&#9203;",title:"Países que requieren aprobación adicional",approval:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">En estos países, su elección ESPP <strong>no será visible</strong> hasta que se complete la aprobación:</p>{{APPROVAL_TAGS}}<div class="info-box" style="margin-top:14px;">Esto es normal. Contacte <strong>AskHR</strong> si su elección permanece invisible tras el cierre de la ventana.</div>`},
      {section:"special",icon:"icon-blue",sym:"&#127470;&#127481;",title:"Italia — Cuenta WeBank requerida",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Los empleados en Italia deben cumplir un requisito adicional antes de inscribirse en el ESPP.</p><div class="info-box" style="margin-top:10px;">Se requiere tener tanto una <strong>cuenta corriente WeBank</strong> como una <strong>cuenta de inversión</strong> para participar en el ESPP.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Consulte las instrucciones detalladas para empleados en Italia: <a href="https://w3.ibm.com/hr/policy/it-compensation-espp" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/hr/policy/it-compensation-espp</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Abra su <strong>cuenta corriente WeBank</strong> y su <strong>cuenta de inversión</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Complete su <strong>perfil bancario en WeBank</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Una vez establecidas las cuentas y completado el perfil bancario, continúe con los pasos estándar de inscripción al ESPP.</div></div></div>`},
      {section:"special",icon:"icon-green",sym:"&#127463;&#127479;",title:"Brasil — Validación de Intercam requerida",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Las aprobaciones de ESPP para Brasil se basan estrictamente en la lista de confirmación oficial de <strong>Intercam</strong>. Todas las solicitudes deben ser validadas por Intercam.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">Contacte a Intercam directamente para solicitar el formulario ESPP:<br><a href="mailto:janvion@intercam.com.br" style="color:#0062ff;">janvion@intercam.com.br</a> &nbsp;|&nbsp; <a href="mailto:mcrippa@intercam.com.br" style="color:#0062ff;">mcrippa@intercam.com.br</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Complete el formulario ESPP de Intercam para que puedan validar su solicitud y añadirle a su lista oficial.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Una vez confirmado por Intercam, el <strong>socio ESPP aprobará la transacción en SuccessFactors</strong>.</div></div></div>`},
      {section:"special",icon:"icon-purple",sym:"&#127479;&#127476;",title:"Rumanía — Firma electrónica IBM Adobe",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">El formulario ESPP para Rumanía requiere una <strong>firma electrónica IBM Adobe</strong>.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">Acceda a la firma electrónica IBM: <a href="https://ibm.eu1.adobesign.com/account/homeJS" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ibm.eu1.adobesign.com</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">¿Sin acceso? Solicítelo en: <a href="https://w3.ibm.com/w3publisher/adobe-sign/how-to-get-access" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/w3publisher/adobe-sign/how-to-get-access</a></div></div></div>`},
      {section:"special",icon:"icon-orange",sym:"&#9997;",title:"Croacia, Lituania, Polonia y Serbia — Firma en tinta húmeda",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">El formulario ESPP para los siguientes países requiere una <strong>firma en tinta húmeda (física)</strong>:</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croacia</span><span class="tag">Lituania</span><span class="tag">Polonia</span><span class="tag">Serbia</span></div><div class="info-box">Asegúrese de que el formulario esté firmado físicamente antes de enviarlo como parte de su inscripción en SuccessFactors.</div>`},
      {section:"special",icon:"icon-red",sym:"&#128683;",title:"Croacia, Lituania, Polonia y Serbia — Darse de baja del ESPP",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Los empleados de los siguientes países deben completar un paso adicional al darse de baja del ESPP:</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croacia</span><span class="tag">Lituania</span><span class="tag">Polonia</span><span class="tag">Serbia</span></div><div class="info-box" style="margin-top:12px;">Una vez completada la transacción de <strong>baja</strong> en SuccessFactors, recibirá un correo electrónico con el formulario ESPP. Complete el formulario y cárguelo en <strong>OpenText</strong>.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Complete la transacción de <strong>baja</strong> en SuccessFactors.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Revise su correo electrónico para el formulario ESPP enviado tras la confirmación.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Complete el formulario de manera completa y precisa.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Cargue el formulario completo en OpenText. Consulte la guía: <a href="https://ibm.box.com/s/9ev95b9x1eypipm0n7hc53uc0q4rotmf" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">Cómo cargar documentos ESPP en OpenText</a></div></div></div>`},


      { section:"faq", icon:"icon-blue", sym:"&#128101;", title:"1. Participación", body:`<div class="faq-q">¿Quién puede participar en el ESPP?</div><div class="faq-a">Todos los IBMers regulares, incluidos los de medio tiempo, y la mayoría de los empleados suplementarios, siempre que residan en un país donde la participación esté permitida. <strong>Américas:</strong> Argentina, Bahamas, Barbados, Brasil, Canadá, Chile, Colombia, Costa Rica, Curazao, Ecuador, Jamaica, México, Perú, Trinidad, Uruguay, EE.UU., Venezuela. <strong>Asia-Pacífico:</strong> Australia, China, Hong Kong, India, Japón, Malasia, Nueva Zelanda, Filipinas, Singapur, Corea del Sur, Taiwán, Tailandia. <strong>EMEA:</strong> Austria, Bélgica, Bulgaria, Chipre, Rep. Checa, Croacia, Dinamarca, Egipto, Estonia, Finlandia, Francia, Alemania, Grecia, Hungría, Irlanda, Israel, Italia, Letonia, Lituania, Luxemburgo, Países Bajos, Noruega, Pakistán, Polonia, Portugal, Catar, Rumanía, Arabia Saudita, Serbia, Eslovaquia, Eslovenia, Sudáfrica, España, Suecia, Suiza, Türkiye, EAU, Reino Unido.</div><div class="faq-q">¿Qué pasa si tengo una solicitud de inscripción pendiente?</div><div class="faq-a">Debe retirar cualquier solicitud pendiente antes de enviar una nueva. SAP SuccessFactors no permitirá una nueva solicitud hasta que se elimine la anterior.</div><div class="faq-q">Si ya estoy inscrito, ¿necesito reinscribirme?</div><div class="faq-a">Generalmente no. Debe reinscribirse si: regresa de una licencia; fue suspendido previamente; o alcanza los límites anuales de $25,000 / 1,000 acciones. Las nóminas de EE.UU. se reinscr. automáticamente; las de otros países deben hacerlo manualmente.</div><div class="faq-q">Perdí la ventana de inscripción. ¿Puedo aún unirme?</div><div class="faq-a">No — espere hasta la próxima ventana.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#36;", title:"2. Compensación elegible y deducciones de nómina", body:`<div class="faq-q">¿Cuánto puedo contribuir?</div><div class="faq-a">Del <strong>1 % al 10 %</strong> de su pago. Máximo: <strong>$25,000 en acciones por año calendario</strong> y no más de <strong>1,000 acciones</strong> por período de oferta.</div><div class="faq-q">¿Puedo cambiar las contribuciones después del cierre de la ventana?</div><div class="faq-a">Puede <strong>reducir</strong> en cualquier momento; solo puede <strong>aumentar</strong> durante una ventana de inscripción.</div><div class="faq-q">¿Cómo se determina el precio de compra de la acción IBM?</div><div class="faq-a">El 85 % del promedio del precio más alto y más bajo de la acción IBM en cada fecha de nómina — un <strong>descuento del 15 %</strong>.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#8801;", title:"3. Plataforma EquatePlus", body:`<div class="faq-q">No puedo acceder a mi cuenta EquatePlus. ¿Qué debo hacer?</div><div class="faq-a">Seleccione el enlace de <strong>Ayuda</strong> en la página de inicio de sesión de EquatePlus.</div><div class="faq-q">¿Cuánto tiempo después de las deducciones aparecerán las acciones en EquatePlus?</div><div class="faq-a">1–10 días (p. ej., EE.UU., Francia, Alemania, España); 10–20 días (p. ej., Brasil, India, Filipinas); 20+ días (p. ej., Australia, Japón, China).</div>` },
      { section:"faq", icon:"icon-orange", sym:"&#9401;", title:"4. Suspensión y salida de IBM", body:`<div class="faq-q">¿Qué pasa con mis acciones si me retiro, jubilo o dejo IBM?</div><div class="faq-a">Las acciones permanecen en su cuenta de Computershare. Si deja IBM, actualice su correo electrónico en Computershare con una dirección no corporativa.</div><div class="faq-q">¿El restablecimiento tras la suspensión es automático?</div><div class="faq-a"><strong>Nómina EE.UU.:</strong> Automático. <strong>Nómina fuera de EE.UU.:</strong> Reinscríbase manualmente en la próxima ventana de inscripción.</div>` },
      { section:"faq", icon:"icon-blue", sym:"&#128200;", title:"6. Consulta, venta y transferencia de acciones", body:`<div class="faq-q">¿Cómo vendo mis acciones?</div><div class="faq-a">Envíe solicitudes de venta a través de <strong>EquatePlus</strong> o <strong>EquateMobile</strong> las 24 horas. Tarifa de transacción: ~$19.95 por venta.</div><div class="faq-q">¿Cómo transfiero acciones a una institución financiera?</div><div class="faq-a">Agregue su cuenta de corretaje en <strong>Preferencias financieras</strong> en EquatePlus y haga clic en <strong>Transaccionar</strong>. Sin cargo de Computershare o IBM.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#127987;", title:"7. Dividendos", body:`<div class="faq-q">¿Cómo se pagan mis dividendos?</div><div class="faq-a"><strong>(1) Reinversión automática</strong> (predeterminado desde el 1 ene. 2023); <strong>(2) Transferencia electrónica</strong>; <strong>(3) Cheque en USD</strong>.</div>` },
      { section:"faq", icon:"icon-red", sym:"&#128203;", title:"8. Fiscalidad", body:`<div class="faq-q">¿Pago impuestos cuando se compran acciones en mi nombre?</div><div class="faq-a">En muchos países, sí — sobre el descuento recibido. Certifique mediante <strong>W-9BEN</strong> (EE.UU.) o <strong>W-8BEN</strong> (fuera de EE.UU.) a través de EquatePlus.</div><div class="faq-q">¿Pago impuestos cuando vendo mis acciones?</div><div class="faq-a">Pueden existir consecuencias fiscales según el período de tenencia y las leyes fiscales locales. Consulte a un profesional fiscal.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#9997;", title:"9. Varios", body:`<div class="faq-q">¿Cómo obtengo el historial de mis contribuciones ESPP?</div><div class="faq-a">Navegue a <strong>Detalles del plan</strong> en EquatePlus y seleccione <strong>Compras archivadas</strong>.</div><div class="faq-q">¿Dónde puedo encontrar la política ESPP y la guía de inscripción?</div><div class="faq-a">En la intranet de IBM: <strong>w3.ibm.com → Programas de compensación global → ESPP → Preguntas frecuentes ESPP</strong>.</div>` },
      {section:"resources",icon:"icon-purple",sym:"&#128279;",title:"Enlaces útiles y soporte",body:`<ul class="resource-list"><li><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs" target="_blank" rel="noopener"><strong>Página ESPP w3</strong></a> — Detalles del programa en la intranet de IBM</li><li><a href="https://w3.ibm.com/hr/askhr/home" target="_blank" rel="noopener"><strong>AskHR</strong></a> — Abrir un ticket para preguntas de inscripción</li><li><strong>SAP SuccessFactors – Portlet de Beneficios</strong> — Inscribirse, actualizar, consultar</li><li><a href="https://www.na.equateplus.com/EquatePlusParticipant2/?login" target="_blank" rel="noopener"><strong>Plataforma EquatePlus</strong></a> — Gestionar acciones tras la compra</li></ul>`}
    ]
  },
  pt: {
    badge:"Benefícios IBM", title:"Plano de Compra de Ações para Funcionários (ESPP)", subtitle:"Guia do participante — inscrição, gestão de contribuições, casos especiais e perguntas frequentes",
    search:"Pesquisar tópicos, palavras-chave, países…", noResults:"Nenhum resultado encontrado. Tente outra palavra-chave.",
    tabs:["Todos os tópicos","Visão geral","Novos participantes","Participantes existentes","Verificar inscrição","Casos especiais","Perguntas frequentes","Recursos"],
    sections:{overview:"Visão geral do programa",new:"Novos participantes",existing:"Participantes existentes",check:"Verificação de inscrição",special:"Casos especiais",faq:"Perguntas frequentes",resources:"Recursos adicionais"},
    ceeCountries:["Croácia","Estônia","Letônia","Polônia","Romênia","Lituânia","Sérvia","Venezuela"],
    approvalCountries:["Brasil","Itália","Croácia","Estônia","Letônia","Polônia","Romênia","Lituânia","Sérvia"],
    cards:[
      { section:"overview", icon:"icon-blue", sym:"&#9733;", title:"O que é o ESPP?", body:`<p style="font-size:14px;color:#21272a;line-height:1.75;margin-top:8px;">O <strong>Plano de Compra de Ações para Funcionários (ESPP)</strong> permite que os funcionários da IBM adquiram ações da IBM com um <strong>desconto de 15%</strong> em relação ao preço de mercado. As contribuições são feitas automaticamente por meio de deduções em folha de pagamento — sem necessidade de negociações manuais.</p><div class="info-box" style="margin-top:14px;"><strong>Como funciona:</strong> Você contribui com 1% a 10% da sua remuneração elegível a cada período de pagamento. A IBM compra ações em seu nome com 15% de desconto na data de compra. As ações são creditadas na sua conta EquatePlus.</div><div class="steps" style="margin-top:16px;"><div class="step"><div class="step-num">1</div><div class="step-text">Inscreva-se durante uma janela de inscrição (1–14 de junho ou 1–14 de dezembro).</div></div><div class="step"><div class="step-num">2</div><div class="step-text">As deduções em folha começam no período de oferta seguinte (1º de julho ou 1º de janeiro).</div></div><div class="step"><div class="step-num">3</div><div class="step-text">A IBM compra ações com 15% de desconto em cada data de pagamento da folha.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">As ações aparecem na sua conta EquatePlus em dias ou semanas, dependendo do país.</div></div></div>` },
      { section:"overview", icon:"icon-green", sym:"&#36;", title:"Benefícios e exemplo", body:`<div class="section-heading" style="margin-top:10px;">Por que se inscrever?</div><ul style="margin:0 0 14px 18px;font-size:13.5px;color:#21272a;line-height:1.8;"><li>Adquira ações da IBM com <strong>15% de desconto</strong> sobre o preço de mercado</li><li>As deduções em folha tornam o investimento automático e simples</li><li>Vantagem imediata de investimento por meio do desconto na compra</li><li>Potencial de retorno adicional se o preço das ações da IBM subir</li><li>Elegível para receber <strong>dividendos</strong> enquanto mantiver ações da IBM</li><li>Torne-se acionista da IBM</li></ul><div class="section-heading">Exemplo prático</div><table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:6px;"><tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;width:55%;">Salário mensal</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$4.000</td></tr><tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Contribuição (10%)</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$400</td></tr><tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Preço de mercado da ação IBM</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$130 / ação</td></tr><tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">Preço ESPP (15% de desconto)</td><td style="padding:7px 12px;border:1px solid #dde1e7;color:#0062ff;font-weight:600;">$110,50 / ação</td></tr><tr style="background:#edf5ff;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">Retorno imediato</td><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">17,6%</td></tr></table><div class="note" style="margin-top:12px;"><strong>Nota:</strong> Este exemplo é ilustrativo. Os preços reais das ações e os retornos variarão.</div>` },
      { section:"overview", icon:"icon-purple", sym:"&#128196;", title:"Detalhes do plano", body:`<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:10px;"><thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Característica do plano</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Detalhes</th></tr></thead><tbody><tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Desconto</td><td style="padding:8px 12px;border:1px solid #dde1e7;">15% abaixo do preço de mercado em cada data de compra na folha de pagamento</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Faixa de contribuição</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1% – 10% da remuneração elegível</td></tr><tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Limite anual</td><td style="padding:8px 12px;border:1px solid #dde1e7;">US$ 25.000 em ações por ano civil</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Períodos de oferta</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1º jan – 30 jun &nbsp;|&nbsp; 1º jul – 31 dez</td></tr></tbody></table>` },
      { section:"overview", icon:"icon-orange", sym:"&#36;&#36;", title:"Taxas padrão (Computershare)", body:`<p style="font-size:13.5px;color:#21272a;margin-top:8px;margin-bottom:12px;">Antes de se inscrever, esteja ciente das taxas padrão do ESPP cobradas pelo fornecedor global da IBM, a Computershare.</p><table style="width:100%;border-collapse:collapse;font-size:13px;"><thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Transação</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">Taxa (USD)</th></tr></thead><tbody><tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Venda de ações</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$19,95</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">Transferência de ações para uma instituição financeira</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Sem taxa</td></tr><tr><td style="padding:8px 12px;border:1px solid #dde1e7;">Taxa de transferência bancária (EUA e exterior)</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$35</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">Cheque em USD por dividendos ou ações vendidas</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">Sem taxa</td></tr></tbody></table><div class="info-box" style="margin-top:12px;">Consulte também o <strong><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-prospectus" target="_blank" rel="noopener" style="color:#0043ce;">Prospecto</a></strong> e o <strong><a href="https://ibm.mystockoptions.com/global-tax-guide/?ibmtoken=SUJNVE9LRU4yNA==" target="_blank" rel="noopener" style="color:#0043ce;">Guia Fiscal Global</a></strong> antes de se inscrever para verificar as implicações fiscais por país. Consulte um profissional fiscal para orientações específicas à sua situação.</div>` },
      {section:"new",icon:"icon-blue",sym:"&#43;",title:"Inscrever-se no ESPP",body:`<div class="info-box"><strong>Apenas nas janelas de inscrição.</strong> A inscrição é possível durante as duas janelas anuais (junho e dezembro). É necessária assinatura eletrônica.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acesse o <strong>portlet de Benefícios do SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Clique em <strong>«Ir para Visão geral de benefícios»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Em <strong>«Inscrições abertas»</strong>, selecione <strong>ESPP – Dedução de salário base IBM</strong> ou <strong>ESPP – Outra remuneração IBM</strong> e clique em <strong>«Inscrever-se»</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">A <strong>data de vigência</strong> é preenchida automaticamente com base no calendário de folha de pagamento do seu país.</div></div><div class="step"><div class="step-num">5</div><div class="step-text">Insira o <strong>percentual de contribuição do funcionário (1–10%)</strong>.</div></div><div class="step"><div class="step-num">6</div><div class="step-text">Selecione <strong>«Sim»</strong> em <em>Aceito</em> e clique em <strong>«Salvar»</strong>.</div></div></div><div class="note"><strong>Ambos os planos?</strong> Clique em «Inscrever-se» em cada plano separadamente. «Outra remuneração» abrange pagamentos que não são salário base nem verbas rescisórias.</div>`},
      {section:"new",icon:"icon-green",sym:"&#10003;",title:"O que esperar após a inscrição",body:`<div class="timeline"><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Janela de dezembro</div>As primeiras deduções começam em <strong>janeiro</strong>.</div></div><div class="tl-item"><div class="tl-dot purple"></div><div class="tl-content"><div class="tl-label purple">Janela de junho</div>As primeiras deduções começam em <strong>julho</strong>.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Verificar deduções</div>Consulte seus <strong>contracheques no SAP SuccessFactors</strong>.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">Credenciais EquatePlus</div>Criadas após o crédito da sua <strong>primeira compra</strong>. Ver tabela abaixo.</div></div></div><table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:12px;"><thead><tr style="background:#f2f4f8;"><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Período de oferta</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Folha</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">Entrega estimada</th></tr></thead><tbody><tr><td style="padding:7px 10px;border:1px solid #dde1e7;">Janeiro</td><td style="padding:7px 10px;border:1px solid #dde1e7;">EUA</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Até 1 semana após o contracheque de 15 de janeiro</td></tr><tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">Janeiro</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Fora dos EUA</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Até 2 semanas após o contracheque de janeiro</td></tr><tr><td style="padding:7px 10px;border:1px solid #dde1e7;">Julho</td><td style="padding:7px 10px;border:1px solid #dde1e7;">EUA</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Até 1 semana após o contracheque de 15 de julho</td></tr><tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">Julho</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Fora dos EUA</td><td style="padding:7px 10px;border:1px solid #dde1e7;">Até 2 semanas após o contracheque de julho</td></tr></tbody></table>`},
      {section:"existing",icon:"icon-orange",sym:"&#8595;",title:"Reduzir contribuição / Cancelar inscrição",body:`<div class="info-box"><strong>Disponível a qualquer momento.</strong> Você pode reduzir ou cancelar a inscrição a qualquer momento do ano.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acesse o <strong>portlet de Benefícios do SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Clique em <strong>«Visão geral de benefícios»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>Para reduzir:</strong> Aba <strong>ESPP/Previdência</strong>, clique no <strong>ícone de lápis</strong>, atualize e salve.</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>Para cancelar:</strong> Clique em <strong>«Cancelar inscrição»</strong>.</div></div></div>`},
      {section:"existing",icon:"icon-blue",sym:"&#8593;",title:"Aumentar contribuição",body:`<div class="info-box"><strong>Apenas nas janelas de inscrição.</strong> O aumento só é possível durante as janelas de junho ou dezembro.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acesse o <strong>portlet de Benefícios do SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Clique em <strong>«Visão geral de benefícios»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Navegue até a aba <strong>«Inscrição»</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Defina a <strong>data de vigência</strong> e o <strong>percentual desejado</strong>.</div></div><div class="step"><div class="step-num">5</div><div class="step-text">Selecione <strong>«Sim»</strong> e clique em <strong>«Salvar»</strong>.</div></div></div>`},
      {section:"check",icon:"icon-blue",sym:"&#128196;",title:"Opção 1 — Portlet de Benefícios",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acesse o <strong>portlet de Benefícios do SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Clique em <strong>«Visão geral de benefícios»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Selecione <strong>ESPP/Previdência</strong>.</div></div></div>`},
      {section:"check",icon:"icon-purple",sym:"&#128203;",title:"Opção 2 — Extrato de confirmação de benefícios",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acesse o <strong>portlet de Benefícios do SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Clique em <strong>«Ver extrato de benefícios»</strong>.</div></div></div><div class="note"><strong>Inscrição recente?</strong> Defina a <strong>«Data em»</strong>: <strong>1º de julho</strong> (janela de junho) ou <strong>1º de janeiro</strong> do ano seguinte (janela de dezembro).</div>`},
      {section:"check",icon:"icon-green",sym:"&#9733;",title:"Opção 3 — Aba Remuneração total",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text">Acesse seu <strong>perfil no SAP SuccessFactors</strong>.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Selecione a aba <strong>«Remuneração total»</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Suas escolhas ESPP aparecem em <strong>«Dedução recorrente»</strong>.</div></div></div>`},
      {section:"special",icon:"icon-red",sym:"&#9873;",title:"Países CEE — Anexo obrigatório",cee:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Funcionários dos países abaixo devem anexar um formulário preenchido:</p>{{CEE_TAGS}}<div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Baixe o formulário na janela de inscrição do SuccessFactors.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Preencha garantindo que os dados <strong>coincidam com sua inscrição</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Anexe novamente no SuccessFactors.</div></div></div><div class="note"><strong>Não consegue baixar?</strong> Problema conhecido. Abra um <strong>ticket no AskHR</strong>.</div>`},
      {section:"special",icon:"icon-blue",sym:"&#127470;&#127481;",title:"Itália — Conta WeBank obrigatória",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Os funcionários na Itália devem cumprir um requisito adicional antes de se inscrever no ESPP.</p><div class="info-box" style="margin-top:10px;">É obrigatório ter tanto uma <strong>conta corrente WeBank</strong> quanto uma <strong>conta de investimentos</strong> para participar do ESPP.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Consulte as instruções detalhadas para funcionários na Itália: <a href="https://w3.ibm.com/hr/policy/it-compensation-espp" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/hr/policy/it-compensation-espp</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Abra sua <strong>conta corrente WeBank</strong> e sua <strong>conta de investimentos</strong>.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Complete seu <strong>perfil bancário no WeBank</strong>.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Após abrir as contas e concluir o perfil bancário, prossiga com as etapas padrão de inscrição no ESPP.</div></div></div>`},
      {section:"special",icon:"icon-green",sym:"&#127463;&#127479;",title:"Brasil — Validação da Intercam obrigatória",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">As aprovações de ESPP para o Brasil são baseadas exclusivamente na lista de confirmação oficial da <strong>Intercam</strong>. Todas as solicitações devem ser validadas pela Intercam.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">Entre em contato diretamente com a Intercam para solicitar o formulário ESPP:<br><a href="mailto:janvion@intercam.com.br" style="color:#0062ff;">janvion@intercam.com.br</a> &nbsp;|&nbsp; <a href="mailto:mcrippa@intercam.com.br" style="color:#0062ff;">mcrippa@intercam.com.br</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Preencha o formulário ESPP da Intercam para que eles possam validar sua solicitação e adicionar seu nome à lista oficial.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Após a confirmação da Intercam, o <strong>parceiro ESPP aprovará a transação no SuccessFactors</strong>.</div></div></div>`},
      {section:"special",icon:"icon-purple",sym:"&#127479;&#127476;",title:"Romênia — Assinatura eletrônica IBM Adobe",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">O formulário ESPP para a Romênia requer uma <strong>assinatura eletrônica IBM Adobe</strong>.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">Acesse a assinatura eletrônica IBM: <a href="https://ibm.eu1.adobesign.com/account/homeJS" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ibm.eu1.adobesign.com</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Sem acesso? Solicite em: <a href="https://w3.ibm.com/w3publisher/adobe-sign/how-to-get-access" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/w3publisher/adobe-sign/how-to-get-access</a></div></div></div>`},
      {section:"special",icon:"icon-orange",sym:"&#9997;",title:"Croácia, Lituânia, Polônia e Sérvia — Assinatura física",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">O formulário ESPP para os seguintes países requer uma <strong>assinatura física (tinta)</strong>:</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croácia</span><span class="tag">Lituânia</span><span class="tag">Polônia</span><span class="tag">Sérvia</span></div><div class="info-box">Certifique-se de que o formulário esteja fisicamente assinado antes de submetê-lo como parte da sua inscrição no SuccessFactors.</div>`},
      {section:"special",icon:"icon-red",sym:"&#128683;",title:"Croácia, Lituânia, Polônia e Sérvia — Cancelar inscrição no ESPP",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Os funcionários dos seguintes países devem concluir uma etapa adicional ao cancelar a inscrição no ESPP:</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">Croácia</span><span class="tag">Lituânia</span><span class="tag">Polônia</span><span class="tag">Sérvia</span></div><div class="info-box" style="margin-top:12px;">Após concluir a transação de <strong>cancelamento de inscrição</strong> no SuccessFactors, você receberá um e-mail com o formulário ESPP. Preencha o formulário e faça o upload para o <strong>OpenText</strong>.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">Conclua a transação de <strong>cancelamento de inscrição</strong> no SuccessFactors.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">Verifique seu e-mail para o formulário ESPP enviado após a confirmação.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Preencha o formulário de forma completa e precisa.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">Faça o upload do formulário preenchido no OpenText. Consulte o guia: <a href="https://ibm.box.com/s/9ev95b9x1eypipm0n7hc53uc0q4rotmf" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">Como fazer upload de documentos ESPP no OpenText</a></div></div></div>`},


      {section:"special",icon:"icon-orange",sym:"&#9203;",title:"Países que exigem aprovação adicional",approval:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">Nesses países, sua escolha ESPP <strong>não ficará visível</strong> até a conclusão da aprovação:</p>{{APPROVAL_TAGS}}<div class="info-box" style="margin-top:14px;">Isso é normal. Contate o <strong>AskHR</strong> se a escolha permanecer invisível após o fechamento da janela.</div>`},
      { section:"faq", icon:"icon-blue", sym:"&#128101;", title:"1. Participação", body:`<div class="faq-q">Quem é elegível para participar do ESPP?</div><div class="faq-a">Todos os funcionários IBM regulares, incluindo trabalhadores em tempo parcial e a maioria dos funcionários suplementares, desde que residam em um país onde a participação seja permitida — regiões das Américas, Ásia-Pacífico e EMEA. Consulte a lista completa de países elegíveis na página ESPP do w3.</div><div class="faq-q">Se já estou inscrito, preciso me reinscrever?</div><div class="faq-a">Em geral, não. É necessário se reinscrever se: retornando de licença; previamente suspenso; ou atingindo os limites anuais de US$ 25.000 / 1.000 ações. Folhas de pagamento dos EUA são reinscritas automaticamente; folhas fora dos EUA devem se reinscrever manualmente.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#36;", title:"2. Remuneração elegível e deduções de folha", body:`<div class="faq-q">Quanto posso contribuir?</div><div class="faq-a">De <strong>1% a 10%</strong> do seu salário. Máximo: <strong>US$ 25.000 em ações por ano civil</strong> e não mais de <strong>1.000 ações</strong> por período de oferta.</div><div class="faq-q">Posso alterar as contribuições após o fechamento da janela de inscrição?</div><div class="faq-a">Você pode <strong>reduzir</strong> a qualquer momento; só pode <strong>aumentar</strong> durante uma janela de inscrição.</div><div class="faq-q">O que conta como remuneração elegível?</div><div class="faq-a">Inclui salário base, comissões e bônus pagos via folha de pagamento. Não inclui verbas rescisórias, reembolsos de despesas ou pagamentos de separação.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#8801;", title:"3. Plataforma EquatePlus", body:`<div class="faq-q">Não consigo acessar minha conta EquatePlus. O que devo fazer?</div><div class="faq-a">Selecione o link <strong>Ajuda</strong> na página de login do EquatePlus.</div><div class="faq-q">Quanto tempo após as deduções as ações aparecerão no EquatePlus?</div><div class="faq-a">1–10 dias (ex.: EUA, França, Alemanha); 10–20 dias (ex.: Brasil, Índia, Filipinas); 20+ dias (ex.: Austrália, Japão, China).</div><div class="faq-q">Como visualizo o histórico de compras no EquatePlus?</div><div class="faq-a">Acesse <strong>Detalhes do plano</strong> no EquatePlus e selecione <strong>Compras arquivadas</strong>.</div>` },
      { section:"faq", icon:"icon-orange", sym:"&#9401;", title:"4. Suspensão e saída da IBM", body:`<div class="faq-q">O que acontece com minhas ações se eu sair, me aposentar ou deixar a IBM?</div><div class="faq-a">As ações permanecem na sua conta Computershare. Ao sair da IBM, atualize seu e-mail no Computershare para um endereço não corporativo.</div><div class="faq-q">A reintegração após suspensão é automática?</div><div class="faq-a"><strong>Folha dos EUA:</strong> Automática. <strong>Folha fora dos EUA:</strong> É necessário se reinscrever manualmente na próxima janela de inscrição.</div><div class="faq-q">O que causa a suspensão do ESPP?</div><div class="faq-a">Licença não remunerada, afastamento por doença, saída temporária ou atingir o limite anual de US$ 25.000 / 1.000 ações.</div>` },
      { section:"faq", icon:"icon-blue", sym:"&#128200;", title:"6. Consulta, venda e transferência de ações", body:`<div class="faq-q">Como vendo minhas ações?</div><div class="faq-a">Envie solicitações de venda pelo <strong>EquatePlus</strong> ou <strong>EquateMobile</strong> 24 horas por dia, 7 dias por semana. Taxa de transação: ~US$ 19,95 por venda.</div><div class="faq-q">Como transfiro ações para uma instituição financeira?</div><div class="faq-a">Adicione sua corretora em <strong>Preferências Financeiras</strong> no EquatePlus e clique em <strong>Transacionar</strong>. Sem taxas da Computershare ou da IBM.</div><div class="faq-q">Há taxa de transferência bancária para receber os recursos da venda?</div><div class="faq-a">Sim, US$ 35 para transferências via wire (EUA e exterior).</div>` },
      { section:"faq", icon:"icon-green", sym:"&#127987;", title:"7. Dividendos", body:`<div class="faq-q">Como meus dividendos são pagos?</div><div class="faq-a"><strong>(1) Reinvestimento automático</strong> (padrão desde 1º de jan de 2023); <strong>(2) Transferência eletrônica</strong>; <strong>(3) Cheque em USD</strong>.</div><div class="faq-q">Como altero minha preferência de dividendos?</div><div class="faq-a">Acesse <strong>Perfil</strong> no EquatePlus, selecione <strong>Preferências Financeiras</strong> e atualize a opção de dividendos.</div>` },
      { section:"faq", icon:"icon-red", sym:"&#128203;", title:"8. Tributação", body:`<div class="faq-q">Pago imposto quando as ações são compradas em meu nome?</div><div class="faq-a">Em muitos países, sim — sobre o desconto recebido. Certifique-se por meio do <strong>W-9BEN</strong> (EUA) ou <strong>W-8BEN</strong> (fora dos EUA) no EquatePlus.</div><div class="faq-q">Pago imposto ao vender minhas ações?</div><div class="faq-a">Podem existir consequências fiscais dependendo do período de manutenção e das leis tributárias locais. Consulte um profissional de impostos.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#9997;", title:"9. Outros", body:`<div class="faq-q">Como obtenho um histórico de todas as minhas contribuições ao ESPP?</div><div class="faq-a">Acesse <strong>Detalhes do plano</strong> no EquatePlus e selecione <strong>Compras arquivadas</strong>.</div><div class="faq-q">Onde encontro a política do ESPP e o guia de inscrição?</div><div class="faq-a">Na intranet da IBM: <strong>w3.ibm.com → Programas de Compensação Global → ESPP → Perguntas frequentes do ESPP</strong>.</div>` },
      {section:"resources",icon:"icon-purple",sym:"&#128279;",title:"Links úteis e suporte",body:`<ul class="resource-list"><li><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs" target="_blank" rel="noopener"><strong>Página ESPP w3</strong></a> — Detalhes do programa na intranet da IBM</li><li><a href="https://w3.ibm.com/hr/askhr/home" target="_blank" rel="noopener"><strong>AskHR</strong></a> — Abrir ticket para dúvidas de inscrição</li><li><strong>SAP SuccessFactors – Portlet de Benefícios</strong> — Inscrever-se, atualizar, consultar</li><li><a href="https://www.na.equateplus.com/EquatePlusParticipant2/?login" target="_blank" rel="noopener"><strong>Plataforma EquatePlus</strong></a> — Gerenciar ações após a compra</li></ul>`}
    ]
  },
  ko: {
    badge:"IBM 복리후생", title:"종업원 주식 구매 제도 (ESPP)", subtitle:"참여자 가이드 — 등록, 기여금 관리, 특별 사례 및 자주 묻는 질문",
    search:"주제, 키워드, 국가 검색…", noResults:"결과를 찾을 수 없습니다. 다른 키워드를 시도해 보세요.",
    tabs:["전체","프로그램 개요","신규 참여자","기존 참여자","등록 확인","특별 사례","자주 묻는 질문","참고 자료"],
    sections:{overview:"프로그램 개요",new:"신규 참여자",existing:"기존 참여자",check:"등록 및 기여금 확인",special:"특별 사례",faq:"자주 묻는 질문(FAQ)",resources:"추가 참고 자료"},
    ceeCountries:["크로아티아","에스토니아","라트비아","폴란드","루마니아","리투아니아","세르비아","베네수엘라"],
    approvalCountries:["브라질","이탈리아","크로아티아","에스토니아","라트비아","폴란드","루마니아","리투아니아","세르비아"],
    cards:[
      { section:"overview", icon:"icon-blue", sym:"&#9733;", title:"ESPP란 무엇인가요?", body:`<p style="font-size:14px;color:#21272a;line-height:1.75;margin-top:8px;"><strong>종업원 주식 구매 제도(ESPP)</strong>는 IBM 직원이 시장 가격 대비 <strong>15% 할인된 가격</strong>으로 IBM 주식을 구매할 수 있는 제도입니다. 기여금은 급여 공제를 통해 자동으로 납부되므로 별도의 거래가 필요하지 않습니다.</p><div class="info-box" style="margin-top:14px;"><strong>운영 방식:</strong> 각 급여 기간마다 적격 보상의 1%~10%를 기여합니다. IBM은 구매일 기준 15% 할인된 가격으로 귀하를 대신하여 주식을 매입합니다. 주식은 귀하의 EquatePlus 계정에 입금됩니다.</div><div class="steps" style="margin-top:16px;"><div class="step"><div class="step-num">1</div><div class="step-text">등록 기간(6월 1~14일 또는 12월 1~14일) 중에 등록하세요.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">급여 공제는 다음 부여 기간(7월 1일 또는 1월 1일)부터 시작됩니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">IBM은 각 급여 지급일에 15% 할인된 가격으로 주식을 매입합니다.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">주식은 국가에 따라 며칠에서 몇 주 내에 귀하의 EquatePlus 계정에 표시됩니다.</div></div></div>` },
      { section:"overview", icon:"icon-green", sym:"&#36;", title:"혜택 및 예시", body:`<div class="section-heading" style="margin-top:10px;">왜 등록해야 하나요?</div><ul style="margin:0 0 14px 18px;font-size:13.5px;color:#21272a;line-height:1.8;"><li>시장 가격 대비 <strong>15% 할인된 가격</strong>으로 IBM 주식 구매</li><li>급여 공제를 통한 자동적이고 간편한 투자</li><li>구매 할인을 통한 즉각적인 투자 이점</li><li>IBM 주가 상승 시 추가 수익 가능성</li><li>IBM 주식 보유 기간 동안 <strong>배당금</strong> 수령 자격</li><li>IBM 주주가 될 수 있는 기회</li></ul><div class="section-heading">실제 예시</div><table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:6px;"><tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;width:55%;">월 급여</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$4,000</td></tr><tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">기여금 (10%)</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$400</td></tr><tr style="background:#f2f4f8;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">IBM 주식 시장 가격</td><td style="padding:7px 12px;border:1px solid #dde1e7;">$130 / 주</td></tr><tr><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:600;">ESPP 구매 가격 (15% 할인)</td><td style="padding:7px 12px;border:1px solid #dde1e7;color:#0062ff;font-weight:600;">$110.50 / 주</td></tr><tr style="background:#edf5ff;"><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">즉각적인 수익률</td><td style="padding:7px 12px;border:1px solid #dde1e7;font-weight:700;color:#0062ff;">17.6%</td></tr></table><div class="note" style="margin-top:12px;"><strong>참고:</strong> 이 예시는 설명을 위한 것입니다. 실제 주가와 수익률은 다를 수 있습니다.</div>` },
      { section:"overview", icon:"icon-purple", sym:"&#128196;", title:"플랜 세부 정보", body:`<table style="width:100%;border-collapse:collapse;font-size:13px;margin-top:10px;"><thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">플랜 특징</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">세부 내용</th></tr></thead><tbody><tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">할인율</td><td style="padding:8px 12px;border:1px solid #dde1e7;">각 급여 구매일의 시장 가격 대비 15% 할인</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">기여율 범위</td><td style="padding:8px 12px;border:1px solid #dde1e7;">적격 보상의 1% – 10%</td></tr><tr><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">연간 한도</td><td style="padding:8px 12px;border:1px solid #dde1e7;">연간 USD $25,000 상당의 주식</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">부여 기간</td><td style="padding:8px 12px;border:1px solid #dde1e7;">1월 1일 – 6월 30일 &nbsp;|&nbsp; 7월 1일 – 12월 31일</td></tr></tbody></table>` },
      { section:"overview", icon:"icon-orange", sym:"&#36;&#36;", title:"표준 수수료 (Computershare)", body:`<p style="font-size:13.5px;color:#21272a;margin-top:8px;margin-bottom:12px;">등록 전에 IBM의 글로벌 벤더인 Computershare를 통한 ESPP의 표준 수수료를 확인하세요.</p><table style="width:100%;border-collapse:collapse;font-size:13px;"><thead><tr style="background:#f2f4f8;"><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">거래 유형</th><th style="padding:8px 12px;border:1px solid #dde1e7;text-align:left;color:#697077;">수수료 (USD)</th></tr></thead><tbody><tr><td style="padding:8px 12px;border:1px solid #dde1e7;">주식 매각</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$19.95</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">금융 기관으로 주식 이체</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">무료</td></tr><tr><td style="padding:8px 12px;border:1px solid #dde1e7;">전신환 수수료 (미국 및 비미국) — 매각 대금 은행 송금</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">$35</td></tr><tr style="background:#f2f4f8;"><td style="padding:8px 12px;border:1px solid #dde1e7;">배당금 또는 매각 주식 USD 수표</td><td style="padding:8px 12px;border:1px solid #dde1e7;font-weight:600;">무료</td></tr></tbody></table><div class="info-box" style="margin-top:12px;">등록 전에 <strong><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-prospectus" target="_blank" rel="noopener" style="color:#0043ce;">투자설명서</a></strong>와 <strong><a href="https://ibm.mystockoptions.com/global-tax-guide/?ibmtoken=SUJNVE9LRU4yNA==" target="_blank" rel="noopener" style="color:#0043ce;">글로벌 세금 가이드</a></strong>도 검토하여 국가별 세금 관련 사항을 확인하세요. 개인 상황에 대한 조언은 세금 전문가에게 문의하세요.</div>` },
      {section:"new",icon:"icon-blue",sym:"&#43;",title:"ESPP 등록 방법",body:`<div class="info-box"><strong>등록 기간에만 가능합니다.</strong> 연 2회 등록 기간(6월, 12월) 중에만 가입할 수 있습니다. 전자 서명이 필요합니다.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors 복리후생 포틀릿</strong>으로 이동합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「복리후생 개요로 이동」</strong>을 클릭합니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>「오픈 등록」</strong>에서 <strong>ESPP – IBM 기본급 공제</strong> 또는 <strong>ESPP – IBM 기타 보상</strong>을 선택하고 <strong>「등록」</strong>을 클릭합니다.</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>「발효일」</strong>은 해당 국가의 급여 달력에 따라 자동 설정됩니다.</div></div><div class="step"><div class="step-num">5</div><div class="step-text"><strong>직원 기여율(1~10%)</strong>을 입력합니다.</div></div><div class="step"><div class="step-num">6</div><div class="step-text"><em>동의함</em> 아래에서 <strong>「예」</strong>를 선택하고 <strong>「저장」</strong>을 클릭합니다.</div></div></div><div class="note"><strong>두 플랜 모두?</strong> 각 플랜에서 「등록」을 개별적으로 클릭하세요. 「기타 보상」은 일반적으로 기본급 및 퇴직금이 아닌 지급액을 의미합니다(국가별로 다를 수 있음).</div>`},
      {section:"new",icon:"icon-green",sym:"&#10003;",title:"등록 후 진행 과정",body:`<div class="timeline"><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">12월 등록 기간</div>첫 공제는 <strong>1월</strong>부터 시작됩니다.</div></div><div class="tl-item"><div class="tl-dot purple"></div><div class="tl-content"><div class="tl-label purple">6월 등록 기간</div>첫 공제는 <strong>7월</strong>부터 시작됩니다.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">공제 확인</div>SAP SuccessFactors에서 <strong>급여 명세서</strong>를 확인하세요.</div></div><div class="tl-item"><div class="tl-dot"></div><div class="tl-content"><div class="tl-label">EquatePlus 자격증명</div>첫 번째 매입 입금 후 생성됩니다. 아래 표를 참조하세요.</div></div></div><table style="width:100%;border-collapse:collapse;font-size:12.5px;margin-top:12px;"><thead><tr style="background:#f2f4f8;"><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">부여 기간</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">급여</th><th style="padding:7px 10px;border:1px solid #dde1e7;text-align:left;color:#697077;">예상 자격증명 수령 시기</th></tr></thead><tbody><tr><td style="padding:7px 10px;border:1px solid #dde1e7;">1월</td><td style="padding:7px 10px;border:1px solid #dde1e7;">미국</td><td style="padding:7px 10px;border:1px solid #dde1e7;">1월 15일 급여 명세서 발행 후 1주일 이내</td></tr><tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">1월</td><td style="padding:7px 10px;border:1px solid #dde1e7;">비미국</td><td style="padding:7px 10px;border:1px solid #dde1e7;">1월 급여 명세서 발행 후 2주일 이내</td></tr><tr><td style="padding:7px 10px;border:1px solid #dde1e7;">7월</td><td style="padding:7px 10px;border:1px solid #dde1e7;">미국</td><td style="padding:7px 10px;border:1px solid #dde1e7;">7월 15일 급여 명세서 발행 후 1주일 이내</td></tr><tr style="background:#f2f4f8;"><td style="padding:7px 10px;border:1px solid #dde1e7;">7월</td><td style="padding:7px 10px;border:1px solid #dde1e7;">비미국</td><td style="padding:7px 10px;border:1px solid #dde1e7;">7월 급여 명세서 발행 후 2주일 이내</td></tr></tbody></table>`},
      {section:"existing",icon:"icon-orange",sym:"&#8595;",title:"기여금 감액 / 탈퇴",body:`<div class="info-box"><strong>언제든지 가능합니다.</strong> 연중 언제든지 기여금을 줄이거나 탈퇴할 수 있습니다.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors 복리후생 포틀릿</strong>으로 이동합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「복리후생 개요로 이동」</strong>을 클릭합니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>감액의 경우:</strong> <strong>ESPP/연금</strong> 탭에서 <strong>연필 아이콘</strong>을 클릭하고 변경 후 저장합니다.</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>탈퇴의 경우:</strong> <strong>「탈퇴」</strong>를 클릭합니다.</div></div></div>`},
      {section:"existing",icon:"icon-blue",sym:"&#8593;",title:"기여금 증액",body:`<div class="info-box"><strong>등록 기간에만 가능합니다.</strong> 6월 또는 12월 등록 기간 중에만 기여율을 높일 수 있습니다.</div><div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors 복리후생 포틀릿</strong>으로 이동합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「복리후생 개요로 이동」</strong>을 클릭합니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>「등록」</strong> 탭으로 이동합니다.</div></div><div class="step"><div class="step-num">4</div><div class="step-text"><strong>발효일</strong>과 원하는 <strong>기여율</strong>을 설정합니다.</div></div><div class="step"><div class="step-num">5</div><div class="step-text"><strong>「예」</strong>를 선택하고 <strong>「저장」</strong>을 클릭합니다.</div></div></div>`},
      {section:"check",icon:"icon-blue",sym:"&#128196;",title:"방법 1 — 복리후생 포틀릿",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors 복리후생 포틀릿</strong>으로 이동합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「복리후생 개요로 이동」</strong>을 클릭합니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>ESPP/연금</strong>을 선택하면 등록 내용이 표시됩니다.</div></div></div>`},
      {section:"check",icon:"icon-purple",sym:"&#128203;",title:"방법 2 — 복리후생 확인서",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SuccessFactors 복리후생 포틀릿</strong>으로 이동합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「복리후생 명세서 보기」</strong>를 클릭합니다.</div></div></div><div class="note"><strong>최근 등록하셨나요?</strong> <strong>「기준일」</strong>을 등록 발효일로 설정하세요: 6월 기간 → <strong>7월 1일</strong>, 12월 기간 → 다음 해 <strong>1월 1일</strong>.</div>`},
      {section:"check",icon:"icon-green",sym:"&#9733;",title:"방법 3 — 총 보상 탭",body:`<div class="steps"><div class="step"><div class="step-num">1</div><div class="step-text"><strong>SAP SuccessFactors 프로필</strong>로 이동합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>「총 보상」</strong> 탭을 선택합니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text"><strong>「정기 공제」</strong> 섹션에서 ESPP 선택 내용을 확인합니다.</div></div></div>`},
      {section:"special",icon:"icon-red",sym:"&#9873;",title:"CEE 국가 — 첨부 서류 필요",cee:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">다음 국가의 직원은 등록 시 완성된 양식을 제출해야 합니다:</p>{{CEE_TAGS}}<div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">SuccessFactors 등록 창에서 양식을 다운로드합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">양식 내용이 <strong>등록 신청 내용과 일치</strong>하도록 작성합니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">작성된 양식을 SuccessFactors에 다시 첨부합니다.</div></div></div><div class="note"><strong>다운로드가 안 되나요?</strong> 알려진 문제입니다. <strong>AskHR 티켓</strong>을 제출하세요.</div>`},
      {section:"special",icon:"icon-orange",sym:"&#9203;",title:"추가 승인이 필요한 국가",approval:true,body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">다음 국가에서는 승인 프로세스가 완료될 때까지 ESPP 선택 내용이 <strong>표시되지 않습니다</strong>:</p>{{APPROVAL_TAGS}}<div class="info-box" style="margin-top:14px;">정상적인 동작입니다. 등록 기간 종료 후 장기간 표시되지 않으면 <strong>AskHR</strong>에 문의하세요.</div>`},
      {section:"special",icon:"icon-blue",sym:"&#127470;&#127481;",title:"이탈리아 — WeBank 계좌 필수",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">이탈리아 직원은 ESPP에 등록하기 전에 추가 요건을 충족해야 합니다.</p><div class="info-box" style="margin-top:10px;">ESPP 참여를 위해서는 <strong>WeBank 당좌 계좌</strong>와 <strong>투자 계좌</strong>가 모두 필요합니다.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">이탈리아 직원을 위한 상세 안내를 확인하세요: <a href="https://w3.ibm.com/hr/policy/it-compensation-espp" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/hr/policy/it-compensation-espp</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text"><strong>WeBank 당좌 계좌</strong>와 <strong>투자 계좌</strong>를 개설하세요.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">WeBank에서 <strong>은행 프로필</strong>을 완성하세요.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">계좌 개설 및 은행 프로필 완성 후 ESPP 표준 등록 절차를 진행하세요.</div></div></div>`},
      {section:"special",icon:"icon-green",sym:"&#127463;&#127479;",title:"브라질 — Intercam 검증 필수",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">브라질 직원의 ESPP 승인은 <strong>Intercam</strong>이 제공하는 공식 확인 명단에 엄격히 근거합니다. 모든 신청은 Intercam의 검증이 필요합니다.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">Intercam에 직접 연락하여 ESPP 양식을 요청하세요:<br><a href="mailto:janvion@intercam.com.br" style="color:#0062ff;">janvion@intercam.com.br</a> &nbsp;|&nbsp; <a href="mailto:mcrippa@intercam.com.br" style="color:#0062ff;">mcrippa@intercam.com.br</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">Intercam ESPP 양식을 작성하여 검증 후 공식 확인 명단에 등록되도록 하세요.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">Intercam 확인 후 <strong>ESPP 파트너가 SuccessFactors에서 거래를 승인</strong>합니다.</div></div></div>`},
      {section:"special",icon:"icon-purple",sym:"&#127479;&#127476;",title:"루마니아 — IBM Adobe 전자 서명",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">루마니아의 ESPP 양식에는 <strong>IBM Adobe 전자 서명</strong>이 필요합니다.</p><div class="steps" style="margin-top:10px;"><div class="step"><div class="step-num">1</div><div class="step-text">IBM 전자 서명 접속: <a href="https://ibm.eu1.adobesign.com/account/homeJS" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ibm.eu1.adobesign.com</a></div></div><div class="step"><div class="step-num">2</div><div class="step-text">접속 권한이 없으신가요? 여기서 신청하세요: <a href="https://w3.ibm.com/w3publisher/adobe-sign/how-to-get-access" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">w3.ibm.com/w3publisher/adobe-sign/how-to-get-access</a></div></div></div>`},
      {section:"special",icon:"icon-orange",sym:"&#9997;",title:"크로아티아, 리투아니아, 폴란드 및 세르비아 — 자필 서명",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">다음 국가의 ESPP 양식에는 <strong>자필(물리적) 서명</strong>이 필요합니다:</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">크로아티아</span><span class="tag">리투아니아</span><span class="tag">폴란드</span><span class="tag">세르비아</span></div><div class="info-box">SuccessFactors에서 등록 서류로 제출하기 전에 양식에 자필 서명이 완료되었는지 확인하세요.</div>`},
      {section:"special",icon:"icon-red",sym:"&#128683;",title:"크로아티아, 리투아니아, 폴란드 및 세르비아 — ESPP 탈퇴",body:`<p style="font-size:13.5px;color:#57606a;margin-top:8px;">다음 국가의 직원은 ESPP 탈퇴 시 추가 단계를 완료해야 합니다:</p><div class="tag-list" style="margin-top:10px;margin-bottom:12px;"><span class="tag">크로아티아</span><span class="tag">리투아니아</span><span class="tag">폴란드</span><span class="tag">세르비아</span></div><div class="info-box" style="margin-top:12px;">SuccessFactors에서 <strong>탈퇴</strong> 거래를 성공적으로 완료하면 ESPP 양식이 포함된 이메일을 받게 됩니다. 양식을 작성하고 <strong>OpenText</strong>에 업로드하세요.</div><div class="steps" style="margin-top:14px;"><div class="step"><div class="step-num">1</div><div class="step-text">SuccessFactors에서 <strong>탈퇴</strong> 거래를 완료합니다.</div></div><div class="step"><div class="step-num">2</div><div class="step-text">탈퇴 확인 후 전송된 ESPP 양식 이메일을 확인합니다.</div></div><div class="step"><div class="step-num">3</div><div class="step-text">양식을 완전하고 정확하게 작성합니다.</div></div><div class="step"><div class="step-num">4</div><div class="step-text">작성된 양식을 OpenText에 업로드합니다. 가이드 참고: <a href="https://ibm.box.com/s/9ev95b9x1eypipm0n7hc53uc0q4rotmf" target="_blank" rel="noopener" style="color:#0062ff;font-weight:600;">ESPP 문서를 OpenText에 업로드하는 방법</a></div></div></div>`},


      { section:"faq", icon:"icon-blue", sym:"&#128101;", title:"1. 참여 자격", body:`<div class="faq-q">ESPP 참여 자격은 누구에게 있나요?</div><div class="faq-a">파트타이머를 포함한 모든 정규 IBM 직원과 대부분의 보충 직원이 참여 자격이 있으며, 단 참여가 허용된 국가에 거주해야 합니다 — 아메리카, 아시아 태평양(한국 포함), EMEA 지역. 전체 적격 국가 목록은 ESPP w3 페이지에서 확인하세요.</div><div class="faq-q">현재 등록되어 있다면 재등록이 필요한가요?</div><div class="faq-a">일반적으로 필요하지 않습니다. 재등록이 필요한 경우: 휴직 복귀 시; 이전에 중단된 경우; 연간 $25,000 / 1,000주 한도에 도달한 경우. 미국 급여는 자동 재등록되며, 비미국 급여(한국 포함)는 수동으로 재등록해야 합니다.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#36;", title:"2. 적격 보상 및 급여 공제", body:`<div class="faq-q">얼마나 기여할 수 있나요?</div><div class="faq-a">급여의 <strong>1%에서 10%</strong>까지. 최대 한도: <strong>연간 $25,000 상당의 주식</strong> 및 부여 기간당 <strong>1,000주</strong> 이하.</div><div class="faq-q">등록 기간 종료 후 기여금을 변경할 수 있나요?</div><div class="faq-a"><strong>감액</strong>은 언제든지 가능하며, <strong>증액</strong>은 등록 기간 중에만 가능합니다.</div><div class="faq-q">적격 보상에는 무엇이 포함되나요?</div><div class="faq-a">기본급, 커미션, 급여를 통해 지급되는 보너스가 포함됩니다. 퇴직금, 경비 환급 또는 퇴직 위로금은 포함되지 않습니다.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#8801;", title:"3. EquatePlus 플랫폼", body:`<div class="faq-q">EquatePlus 계정에 접속할 수 없습니다. 어떻게 해야 하나요?</div><div class="faq-a">EquatePlus 로그인 페이지에서 <strong>도움말</strong> 링크를 선택하세요.</div><div class="faq-q">공제 후 얼마나 지나면 주식이 EquatePlus에 표시되나요?</div><div class="faq-a">1–10일 (예: 미국, 한국); 10–20일 (예: 인도, 태국); 20일 이상 (예: 일본, 중국).</div><div class="faq-q">EquatePlus에서 구매 내역은 어디서 확인하나요?</div><div class="faq-a">EquatePlus에서 <strong>플랜 세부 정보</strong>로 이동하여 <strong>구매 기록</strong>을 선택하세요.</div>` },
      { section:"faq", icon:"icon-orange", sym:"&#9401;", title:"4. 중단 및 IBM 퇴직", body:`<div class="faq-q">탈퇴, 퇴직 또는 IBM을 떠날 경우 주식은 어떻게 되나요?</div><div class="faq-a">주식은 Computershare 계정에 그대로 남아 있습니다. IBM을 떠나면 Computershare에 IBM 외부 이메일 주소를 업데이트하세요.</div><div class="faq-q">중단 후 복직 시 재등록이 자동으로 이루어지나요?</div><div class="faq-a"><strong>미국 급여:</strong> 자동. <strong>비미국 급여:</strong> 다음 등록 기간에 수동으로 재등록해야 합니다.</div><div class="faq-q">ESPP가 중단되는 원인은 무엇인가요?</div><div class="faq-a">무급 휴가, 병가, 일시적 퇴직 또는 연간 $25,000 / 1,000주 한도 도달.</div>` },
      { section:"faq", icon:"icon-blue", sym:"&#128200;", title:"6. 주식 조회, 매각 및 이전", body:`<div class="faq-q">주식을 어떻게 매각하나요?</div><div class="faq-a"><strong>EquatePlus</strong> 또는 <strong>EquateMobile</strong>을 통해 24시간 언제든지 매각 요청을 제출하세요. 거래 수수료: 매각당 약 $19.95.</div><div class="faq-q">주식을 금융 기관으로 이전하려면 어떻게 하나요?</div><div class="faq-a">EquatePlus의 <strong>금융 기본 설정</strong>에서 증권사를 추가하고 <strong>거래</strong>를 클릭하세요. Computershare 및 IBM의 수수료는 없습니다.</div><div class="faq-q">매각 대금 수령 시 전신환 수수료가 있나요?</div><div class="faq-a">예, 전신환 이체(미국 및 비미국)의 경우 $35가 부과됩니다.</div>` },
      { section:"faq", icon:"icon-green", sym:"&#127987;", title:"7. 배당금", body:`<div class="faq-q">배당금은 어떻게 지급되나요?</div><div class="faq-a"><strong>(1) 자동 재투자</strong> (2023년 1월 1일부터 기본값); <strong>(2) 전자 이체</strong>; <strong>(3) USD 수표</strong>.</div><div class="faq-q">배당금 지급 방식을 변경하려면 어떻게 하나요?</div><div class="faq-a">EquatePlus에서 <strong>프로필</strong>로 이동하고 <strong>금융 기본 설정</strong>을 선택한 후 배당금 옵션을 업데이트하세요.</div>` },
      { section:"faq", icon:"icon-red", sym:"&#128203;", title:"8. 세금", body:`<div class="faq-q">주식이 제 명의로 구매될 때 세금을 납부해야 하나요?</div><div class="faq-a">많은 국가에서 그렇습니다 — 받은 할인에 대해 세금이 부과됩니다. EquatePlus를 통해 <strong>W-9BEN</strong> (미국) 또는 <strong>W-8BEN</strong> (비미국)으로 인증하세요.</div><div class="faq-q">주식을 매각할 때 세금을 납부해야 하나요?</div><div class="faq-a">보유 기간 및 현지 세법에 따라 세금이 발생할 수 있습니다. 세금 전문가에게 문의하세요.</div>` },
      { section:"faq", icon:"icon-purple", sym:"&#9997;", title:"9. 기타", body:`<div class="faq-q">ESPP 기여 내역 전체를 어떻게 확인하나요?</div><div class="faq-a">EquatePlus에서 <strong>플랜 세부 정보</strong>로 이동하여 <strong>구매 기록</strong>을 선택하세요.</div><div class="faq-q">ESPP 정책 및 등록 안내는 어디서 찾을 수 있나요?</div><div class="faq-a">IBM 인트라넷에서: <strong>w3.ibm.com → 글로벌 보상 프로그램 → ESPP → ESPP FAQ</strong>.</div>` },
      {section:"resources",icon:"icon-purple",sym:"&#128279;",title:"유용한 링크 및 지원",body:`<ul class="resource-list"><li><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs" target="_blank" rel="noopener"><strong>ESPP w3 페이지</strong></a> — IBM 인트라넷의 전체 프로그램 세부 정보</li><li><a href="https://w3.ibm.com/hr/askhr/home" target="_blank" rel="noopener"><strong>AskHR</strong></a> — 등록 문제 또는 국가별 질문에 대한 티켓 접수</li><li><strong>SAP SuccessFactors – 복리후생 포틀릿</strong> — 등록, 업데이트, 조회</li><li><a href="https://www.na.equateplus.com/EquatePlusParticipant2/?login" target="_blank" rel="noopener"><strong>EquatePlus 플랫폼</strong></a> — 구매 후 주식 관리</li></ul>`}
    ]
  }
};

// ─── RENDER ENGINE ───────────────────────────────────────────────────────────
let currentLang = 'en';
let currentSection = 'all';

function makeTags(arr) {
  return '<div class="tag-list">' + arr.map(c => `<span class="tag">${c}</span>`).join('') + '</div>';
}

function renderPage(lang) {
  const t = T[lang];
  document.documentElement.lang = lang;
  document.title = t.title;
  document.getElementById('t-badge').textContent = t.badge;
  document.getElementById('t-title').textContent = t.title;
  document.getElementById('t-subtitle').textContent = t.subtitle;
  document.getElementById('searchInput').placeholder = t.search;
  document.getElementById('no-results').textContent = t.noResults;
  document.getElementById('no-results').style.display = 'none';
  document.getElementById('searchInput').value = '';

  const sectionKeys = ['all','overview','new','existing','check','special','faq','resources'];

  // Top nav links (exclude "All")
  const w3NavEl = document.getElementById('w3NavLinks');
  w3NavEl.innerHTML = sectionKeys.slice(1).map((s, i) =>
    `<li><a href="#" class="w3-navlink${currentSection === s ? ' active' : ''}" onclick="showSectionW3('${s}',this);return false;">${t.tabs[i+1]}</a></li>`
  ).join('');

  // Content
  const sectionOrder = ['overview','new','existing','check','special','faq','resources'];
  let html = '';
  sectionOrder.forEach(sec => {
    const cards = t.cards.filter(c => c.section === sec);
    if (!cards.length) return;
    html += `<div class="section-heading" id="label-${sec}" style="${currentSection !== 'all' && currentSection !== sec ? 'display:none' : ''}">${t.sections[sec]}</div>`;
    cards.forEach(card => {
      let body = card.body;
      if (card.cee) body = body.replace('{{CEE_TAGS}}', makeTags(t.ceeCountries));
      if (card.approval) body = body.replace('{{APPROVAL_TAGS}}', makeTags(t.approvalCountries));
      const display = (currentSection === 'all' || currentSection === sec) ? '' : 'display:none';
      html += `<div class="card" data-section="${sec}" style="${display}">
  <div class="card-header" onclick="toggleCard(this)">
    <div class="card-title"><span class="card-icon ${card.icon}">${card.sym}</span>${card.title}</div>
    <span class="chevron">&#9660;</span>
  </div>
  <div class="card-body">${body}</div>
</div>`;
    });
  });
  document.getElementById('content').innerHTML = html;
}

function setLang(lang) {
  document.getElementById('langSelect').value = lang;
  currentLang = lang;
  currentSection = 'all';
  renderPage(lang);
}

function _applySection(section) {
  currentSection = section;
  document.querySelectorAll('.card').forEach(card => {
    card.style.display = (section === 'all' || card.dataset.section === section) ? '' : 'none';
  });
  document.querySelectorAll('.section-heading').forEach(label => {
    const id = label.id.replace('label-', '');
    label.style.display = (section === 'all' || section === id) ? '' : 'none';
  });
  document.getElementById('searchInput').value = '';
  document.getElementById('no-results').style.display = 'none';
}

function showSectionW3(section, btn) {
  document.querySelectorAll('.w3-navlink').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  _applySection(section);
}

function toggleCard(header) {
  header.parentElement.classList.toggle('open');
}

function filterCards() {
  const query = document.getElementById('searchInput').value.toLowerCase().trim();
  document.querySelectorAll('.w3-navlink').forEach(b => b.classList.remove('active'));
  currentSection = 'all';
  if (!query) {
    document.querySelectorAll('.card').forEach(c => { c.style.display = ''; });
    document.querySelectorAll('.section-heading').forEach(l => { l.style.display = ''; });
    document.getElementById('no-results').style.display = 'none';
    return;
  }
  let anyVisible = false;
  const visibleSections = new Set();
  document.querySelectorAll('.card').forEach(card => {
    const match = card.textContent.toLowerCase().includes(query);
    card.style.display = match ? '' : 'none';
    if (match) { anyVisible = true; visibleSections.add(card.dataset.section); }
  });
  document.querySelectorAll('.section-heading').forEach(label => {
    label.style.display = visibleSections.has(label.id.replace('label-', '')) ? '' : 'none';
  });
  document.getElementById('no-results').style.display = anyVisible ? 'none' : 'block';
}

// Init
renderPage('en');
</script>
</body>
</html>
