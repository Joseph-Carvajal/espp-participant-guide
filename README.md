<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ESPP Participant Guide</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: -apple-system, "Segoe UI", system-ui, sans-serif;
    font-size: 14px;
    line-height: 1.6;
    color: #1f2328;
    background: #f7f8fa;
    padding: 24px 16px 48px;
  }

  .container {
    max-width: 760px;
    margin: 0 auto;
  }

  /* Header */
  .header {
    background: #fff;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    padding: 28px 28px 20px;
    margin-bottom: 20px;
  }
  .header-badge {
    display: inline-block;
    background: #3b82d4;
    color: #fff;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    padding: 3px 10px;
    border-radius: 4px;
    margin-bottom: 10px;
  }
  .header h1 {
    font-size: 22px;
    font-weight: 700;
    color: #1f2328;
    margin-bottom: 6px;
  }
  .header p {
    color: #57606a;
    font-size: 13.5px;
  }

  /* Search */
  .search-wrap {
    position: relative;
    margin-bottom: 20px;
  }
  .search-wrap input {
    width: 100%;
    padding: 10px 14px 10px 38px;
    border: 1px solid #e5e7eb;
    border-radius: 6px;
    font-size: 14px;
    background: #fff;
    color: #1f2328;
    outline: none;
  }
  .search-wrap input:focus { border-color: #3b82d4; }
  .search-icon {
    position: absolute;
    left: 12px;
    top: 50%;
    transform: translateY(-50%);
    color: #57606a;
    font-size: 15px;
  }

  /* Nav tabs */
  .nav-tabs {
    display: flex;
    gap: 6px;
    flex-wrap: wrap;
    margin-bottom: 20px;
  }
  .tab-btn {
    padding: 7px 14px;
    border: 1px solid #e5e7eb;
    border-radius: 20px;
    background: #fff;
    color: #57606a;
    font-size: 13px;
    cursor: pointer;
    transition: background 0.15s, color 0.15s, border-color 0.15s;
  }
  .tab-btn:hover { background: #f0f4ff; border-color: #3b82d4; color: #3b82d4; }
  .tab-btn.active { background: #3b82d4; border-color: #3b82d4; color: #fff; font-weight: 600; }

  /* Cards */
  .card {
    background: #fff;
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    margin-bottom: 12px;
    overflow: hidden;
  }
  .card-header {
    padding: 14px 18px;
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: center;
    user-select: none;
  }
  .card-header:hover { background: #f7f8fa; }
  .card-title {
    font-weight: 600;
    font-size: 14px;
    color: #1f2328;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .card-icon {
    width: 26px;
    height: 26px;
    border-radius: 6px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 13px;
    flex-shrink: 0;
  }
  .icon-blue   { background: #dbeafe; color: #3b82d4; }
  .icon-purple { background: #ede9fe; color: #7c5cd8; }
  .icon-green  { background: #dcfce7; color: #16a34a; }
  .icon-orange { background: #fff7ed; color: #ea580c; }
  .icon-red    { background: #fee2e2; color: #dc2626; }

  .chevron { color: #57606a; font-size: 11px; transition: transform 0.2s; }
  .card.open .chevron { transform: rotate(180deg); }
  .card-body {
    display: none;
    padding: 0 18px 16px;
    border-top: 1px solid #e5e7eb;
  }
  .card.open .card-body { display: block; }

  /* Steps */
  .steps { margin-top: 12px; }
  .step { display: flex; gap: 12px; margin-bottom: 10px; align-items: flex-start; }
  .step-num {
    width: 22px; height: 22px; border-radius: 50%;
    background: #3b82d4; color: #fff;
    font-size: 11px; font-weight: 700;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0; margin-top: 1px;
  }
  .step-text { color: #1f2328; font-size: 13.5px; line-height: 1.55; }

  /* Alert boxes */
  .note {
    background: #fff7ed; border-left: 3px solid #ea580c;
    border-radius: 0 6px 6px 0; padding: 10px 14px;
    margin-top: 12px; font-size: 13px; color: #7c2d12;
  }
  .note strong { color: #9a3412; }
  .info-box {
    background: #f0f4ff; border-left: 3px solid #3b82d4;
    border-radius: 0 6px 6px 0; padding: 10px 14px;
    margin-top: 12px; font-size: 13px; color: #1e3a5f;
  }
  .info-box strong { color: #1d4ed8; }

  /* Country tags */
  .tag-list { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 8px; }
  .tag { background: #ede9fe; color: #5b21b6; font-size: 11.5px; font-weight: 600; padding: 2px 9px; border-radius: 12px; }

  /* FAQ */
  .faq-q {
    font-weight: 600; color: #1f2328; margin-top: 14px;
    font-size: 13.5px; display: flex; gap: 8px;
  }
  .faq-q::before {
    content: "Q"; background: #3b82d4; color: #fff;
    border-radius: 4px; padding: 0 5px; font-size: 11px;
    display: flex; align-items: center; flex-shrink: 0; height: 18px; margin-top: 2px;
  }
  .faq-a { color: #57606a; font-size: 13.5px; margin-top: 4px; padding-left: 26px; }

  /* Section headings */
  .section-heading {
    font-size: 13px; font-weight: 700; text-transform: uppercase;
    letter-spacing: 0.05em; color: #57606a; margin-bottom: 10px; margin-top: 4px;
  }

  /* Timeline */
  .timeline { margin-top: 12px; }
  .tl-item { display: flex; gap: 14px; margin-bottom: 14px; align-items: flex-start; }
  .tl-dot { width: 12px; height: 12px; border-radius: 50%; background: #3b82d4; flex-shrink: 0; margin-top: 4px; }
  .tl-dot.purple { background: #7c5cd8; }
  .tl-content { font-size: 13.5px; color: #1f2328; }
  .tl-label { font-weight: 600; color: #3b82d4; font-size: 12px; text-transform: uppercase; letter-spacing: 0.05em; margin-bottom: 2px; }
  .tl-label.purple { color: #7c5cd8; }

  /* Resources */
  .resource-list { list-style: none; margin-top: 10px; }
  .resource-list li { padding: 8px 0; border-bottom: 1px solid #e5e7eb; display: flex; align-items: center; gap: 10px; font-size: 13.5px; }
  .resource-list li:last-child { border-bottom: none; }
  .resource-list li::before { content: "↗"; color: #3b82d4; font-weight: 700; }

  /* No results */
  .no-results { text-align: center; color: #57606a; padding: 32px 0; font-size: 14px; display: none; }

  /* Footer */
  .footer { margin-top: 36px; padding-top: 14px; border-top: 1px solid #e5e7eb; text-align: center; font-size: 12px; color: #57606a; }
</style>
</head>
<body>
<div class="container">

  <!-- Header -->
  <div class="header">
    <div class="header-badge">IBM Benefits</div>
    <h1>Employee Stock Purchase Plan</h1>
    <p>Participant Guide — enrollment, contribution management, special cases &amp; FAQs</p>
  </div>

  <!-- Search -->
  <div class="search-wrap">
    <span class="search-icon">&#128269;</span>
    <input type="text" id="searchInput" placeholder="Search topics, keywords, countries…" oninput="filterCards()">
  </div>

  <!-- Nav tabs -->
  <div class="nav-tabs">
    <button class="tab-btn active" onclick="showSection('all', this)">All Topics</button>
    <button class="tab-btn" onclick="showSection('new', this)">New Participants</button>
    <button class="tab-btn" onclick="showSection('existing', this)">Existing Participants</button>
    <button class="tab-btn" onclick="showSection('check', this)">Check Enrollment</button>
    <button class="tab-btn" onclick="showSection('special', this)">Special Cases</button>
    <button class="tab-btn" onclick="showSection('faq', this)">FAQs</button>
    <button class="tab-btn" onclick="showSection('resources', this)">Resources</button>
  </div>

  <div id="no-results" class="no-results">No matching topics found. Try a different keyword.</div>

  <!-- NEW PARTICIPANTS -->
  <div class="section-heading" id="label-new">New Participants</div>

  <div class="card" data-section="new" data-keywords="enroll enrollment new participant espp base salary other compensation successfactors">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-blue">&#43;</span>Enrolling in ESPP</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="info-box"><strong>Enrollment windows only.</strong> You can enroll during one of the two annual enrollment windows (June &amp; December). Your electronic signature is required.</div>
      <div class="steps">
        <div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
        <div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
        <div class="step"><div class="step-num">3</div><div class="step-text">Under <strong>Open Enrollments</strong>, select <strong>ESPP – IBM Base Salary Deduction</strong> or <strong>ESPP – IBM Other Compensation</strong> by clicking <strong>Enroll</strong>.</div></div>
        <div class="step"><div class="step-num">4</div><div class="step-text">The <strong>Effective From Date</strong> defaults to the Enrollment Effective Date based on your country payroll calendar.</div></div>
        <div class="step"><div class="step-num">5</div><div class="step-text">Enter the <strong>Employee Contribution Percentage</strong> between <strong>1–10%</strong>.</div></div>
        <div class="step"><div class="step-num">6</div><div class="step-text">Select <strong>"Yes"</strong> under <em>I Accept</em>, then click <strong>Save</strong>.</div></div>
      </div>
      <div class="note"><strong>Both plans?</strong> If you want both Base Salary Deduction and Other Compensation, click Enroll in each plan separately. "Other Compensation" generally covers payments that are not base salary nor separation payments (may vary by country).</div>
    </div>
  </div>

  <div class="card" data-section="new" data-keywords="after enrollment deductions january july payslip equateplus login">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-green">&#10003;</span>What to Expect After Enrollment</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="timeline">
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-content"><div class="tl-label">December Window</div>First ESPP payroll deductions begin in <strong>January</strong>.</div>
        </div>
        <div class="tl-item">
          <div class="tl-dot purple"></div>
          <div class="tl-content"><div class="tl-label purple">June Window</div>First ESPP payroll deductions begin in <strong>July</strong>.</div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-content"><div class="tl-label">Verify Deductions</div>Check your <strong>payslips in SAP SuccessFactors</strong> to confirm deductions were made.</div>
        </div>
        <div class="tl-item">
          <div class="tl-dot"></div>
          <div class="tl-content"><div class="tl-label">EquatePlus Access</div><strong>2–3 weeks</strong> after the first deduction, expect login credentials for the ESPP platform, <strong>EquatePlus</strong>.</div>
        </div>
      </div>
    </div>
  </div>

  <!-- EXISTING PARTICIPANTS -->
  <div class="section-heading" id="label-existing">Existing Participants</div>

  <div class="card" data-section="existing" data-keywords="decrease contribution opt out withdraw anytime pencil icon">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-orange">&#8595;</span>Decreasing Contribution / Opting Out</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="info-box"><strong>Available anytime.</strong> You can decrease your contribution or opt out at any point throughout the year.</div>
      <div class="steps">
        <div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
        <div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
        <div class="step"><div class="step-num">3</div><div class="step-text"><strong>To decrease:</strong> Go to the <strong>ESPP/Pensions tab</strong>, click the <strong>Pencil Icon</strong> to update your percentage, and save.</div></div>
        <div class="step"><div class="step-num">4</div><div class="step-text"><strong>To opt out:</strong> Click <strong>Opt Out</strong>.</div></div>
      </div>
    </div>
  </div>

  <div class="card" data-section="existing" data-keywords="increase contribution enrollment window june december">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-blue">&#8593;</span>Increasing Contribution Amount</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="info-box"><strong>Enrollment windows only.</strong> You can only increase your contribution during the June or December enrollment windows.</div>
      <div class="steps">
        <div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
        <div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
        <div class="step"><div class="step-num">3</div><div class="step-text">Navigate to the <strong>Enrollment tab</strong>.</div></div>
        <div class="step"><div class="step-num">4</div><div class="step-text">Set the <strong>Effective Date</strong> and desired <strong>Employee Contribution Percentage</strong>.</div></div>
        <div class="step"><div class="step-num">5</div><div class="step-text">Select <strong>"Yes"</strong> under <em>I Accept</em>, then click <strong>Save</strong>.</div></div>
      </div>
    </div>
  </div>

  <!-- CHECK ENROLLMENT -->
  <div class="section-heading" id="label-check">Checking Enrollment &amp; Contribution</div>

  <div class="card" data-section="check" data-keywords="check enrollment benefits portlet option 1">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-blue">&#128196;</span>Option 1 — Benefits Portlet</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="steps">
        <div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
        <div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>Go to Benefits Overview</strong>.</div></div>
        <div class="step"><div class="step-num">3</div><div class="step-text">Select <strong>ESPP/Pensions</strong>. Your completed elections should populate here.</div></div>
      </div>
    </div>
  </div>

  <div class="card" data-section="check" data-keywords="benefits confirmation statement as of date july january option 2">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-purple">&#128203;</span>Option 2 — Benefits Confirmation Statement</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="steps">
        <div class="step"><div class="step-num">1</div><div class="step-text">Go to the <strong>SuccessFactors Benefit Portlet</strong>.</div></div>
        <div class="step"><div class="step-num">2</div><div class="step-text">Click <strong>View Benefits Statement</strong>.</div></div>
      </div>
      <div class="note">
        <strong>Recently enrolled or changed contributions?</strong> Set the <strong>"As of Date"</strong> to the Enrollment Effective Date:
        <ul style="margin-top:6px; padding-left:16px;">
          <li><strong>June window</strong> → use <strong>July 1</strong></li>
          <li><strong>December window</strong> → use <strong>January 1</strong> of the next year</li>
        </ul>
      </div>
    </div>
  </div>

  <div class="card" data-section="check" data-keywords="total rewards tab recurring deduction profile option 3">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-green">&#9733;</span>Option 3 — Total Rewards Tab</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="steps">
        <div class="step"><div class="step-num">1</div><div class="step-text">Navigate to your <strong>SAP SuccessFactors Profile</strong>.</div></div>
        <div class="step"><div class="step-num">2</div><div class="step-text">Select the <strong>Total Rewards</strong> tab.</div></div>
        <div class="step"><div class="step-num">3</div><div class="step-text">Your ESPP elections appear under the <strong>Recurring Deduction</strong> section.</div></div>
      </div>
    </div>
  </div>

  <!-- SPECIAL CASES -->
  <div class="section-heading" id="label-special">Special Cases</div>

  <div class="card" data-section="special" data-keywords="CEE countries attachment form croatia estonia latvia poland romania lithuania serbia venezuela">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-red">&#9873;</span>CEE Countries — Attachment Required</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <p style="font-size:13.5px; color:#57606a; margin-top:8px;">Employees in the following countries must submit a completed form with their enrollment:</p>
      <div class="tag-list">
        <span class="tag">Croatia</span><span class="tag">Estonia</span><span class="tag">Latvia</span>
        <span class="tag">Poland</span><span class="tag">Romania</span><span class="tag">Lithuania</span>
        <span class="tag">Serbia</span><span class="tag">Venezuela</span>
      </div>
      <div class="steps" style="margin-top:14px;">
        <div class="step"><div class="step-num">1</div><div class="step-text">Download the required form from within the enrollment window in SuccessFactors.</div></div>
        <div class="step"><div class="step-num">2</div><div class="step-text">Complete the form, ensuring all details <strong>match your enrollment submission</strong> exactly.</div></div>
        <div class="step"><div class="step-num">3</div><div class="step-text">Re-attach the completed form in SuccessFactors.</div></div>
      </div>
      <div class="note"><strong>Can't download the form?</strong> This is a known issue being resolved. Please raise an <strong>AskHR ticket</strong> if you are unable to download it.</div>
    </div>
  </div>

  <div class="card" data-section="special" data-keywords="approval pending brazil italy croatia estonia latvia poland romania lithuania serbia election not showing">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-orange">&#9203;</span>Countries Requiring Additional Approval</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <p style="font-size:13.5px; color:#57606a; margin-top:8px;">In these countries, your ESPP election will <strong>not be visible</strong> until the approval process is fully completed:</p>
      <div class="tag-list">
        <span class="tag">Brazil</span><span class="tag">Italy</span><span class="tag">Croatia</span>
        <span class="tag">Estonia</span><span class="tag">Latvia</span><span class="tag">Poland</span>
        <span class="tag">Romania</span><span class="tag">Lithuania</span><span class="tag">Serbia</span>
      </div>
      <div class="info-box" style="margin-top:14px;">This is expected behavior — no action needed while approval is pending. Contact <strong>AskHR</strong> if your election remains invisible for an extended period after the enrollment window closes.</div>
    </div>
  </div>

  <!-- FAQs -->
  <div class="section-heading" id="label-faq">Frequently Asked Questions</div>

  <div class="card" data-section="faq" data-keywords="faq questions when enroll increase decrease anytime contribution">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-blue">?</span>Enrollment &amp; Contribution FAQs</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="faq-q">When can I enroll in ESPP?</div>
      <div class="faq-a">Only during the two annual enrollment windows — <strong>June</strong> and <strong>December</strong>. You cannot enroll outside these windows.</div>
      <div class="faq-q">Can I change my contribution percentage at any time?</div>
      <div class="faq-a"><strong>Decrease / Opt Out:</strong> Yes, any time during the year.<br><strong>Increase:</strong> Only during June or December enrollment windows.</div>
      <div class="faq-q">What is the contribution range?</div>
      <div class="faq-a">Between <strong>1% and 10%</strong> of eligible compensation.</div>
      <div class="faq-q">Do I need to enroll in both Base Salary and Other Compensation plans separately?</div>
      <div class="faq-a">Yes. If you want both, you must click <strong>Enroll</strong> in each plan independently in SuccessFactors.</div>
      <div class="faq-q">What counts as "Other Compensation"?</div>
      <div class="faq-a">Generally, any payments that are <strong>not base salary nor separation payments</strong>. This may vary by country.</div>
    </div>
  </div>

  <div class="card" data-section="faq" data-keywords="faq equateplus deductions payslip when start">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-green">?</span>Deductions &amp; Platform FAQs</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <div class="faq-q">When do payroll deductions begin?</div>
      <div class="faq-a"><strong>January</strong> for December window enrollees, and <strong>July</strong> for June window enrollees. Exact dates vary by country — check your payslip in SuccessFactors.</div>
      <div class="faq-q">When will I receive access to EquatePlus?</div>
      <div class="faq-a">Approximately <strong>2–3 weeks</strong> after your first payroll deduction.</div>
      <div class="faq-q">How do I verify my deductions were made?</div>
      <div class="faq-a">Check your <strong>payslips in SAP SuccessFactors</strong> after the expected deduction date.</div>
      <div class="faq-q">My election is not visible after enrollment — is something wrong?</div>
      <div class="faq-a">If you are in a country requiring additional approval (Brazil, Italy, Croatia, Estonia, Latvia, Poland, Romania, Lithuania, Serbia), your election will not appear until approval is complete. This is expected.</div>
    </div>
  </div>

  <!-- RESOURCES -->
  <div class="section-heading" id="label-resources">Additional Resources</div>

  <div class="card" data-section="resources" data-keywords="resources w3 askhr espp page help support">
    <div class="card-header" onclick="toggleCard(this)">
      <div class="card-title"><span class="card-icon icon-purple">&#128279;</span>Helpful Links &amp; Support</div>
      <span class="chevron">&#9660;</span>
    </div>
    <div class="card-body">
      <ul class="resource-list">
        <li><strong>ESPP w3 Page</strong> — Full program details and announcements on IBM's intranet</li>
        <li><strong>AskHR</strong> — Raise a ticket for enrollment issues, missing forms, or country-specific questions</li>
        <li><strong>SAP SuccessFactors – Benefit Portlet</strong> — Enroll, update, and view your ESPP elections</li>
        <li><strong>EquatePlus Platform</strong> — Manage your ESPP shares after purchase (access provided after first deduction)</li>
      </ul>
    </div>
  </div>

</div><!-- /container -->

<div class="footer" style="max-width:760px; margin:0 auto;">
  Made with IBM Bob
</div>

<script>
  function toggleCard(header) {
    header.parentElement.classList.toggle('open');
  }

  function showSection(section, btn) {
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
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

  function filterCards() {
    const query = document.getElementById('searchInput').value.toLowerCase().trim();
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    document.querySelector('.tab-btn').classList.add('active');
    if (!query) {
      document.querySelectorAll('.card').forEach(c => { c.style.display = ''; });
      document.querySelectorAll('.section-heading').forEach(l => { l.style.display = ''; });
      document.getElementById('no-results').style.display = 'none';
      return;
    }
    let anyVisible = false;
    const visibleSections = new Set();
    document.querySelectorAll('.card').forEach(card => {
      const text = (card.dataset.keywords + ' ' + card.textContent).toLowerCase();
      const match = text.includes(query);
      card.style.display = match ? '' : 'none';
      if (match) { anyVisible = true; visibleSections.add(card.dataset.section); }
    });
    document.querySelectorAll('.section-heading').forEach(label => {
      label.style.display = visibleSections.has(label.id.replace('label-', '')) ? '' : 'none';
    });
    document.getElementById('no-results').style.display = anyVisible ? 'none' : 'block';
  }
</script>
</body>
</html>
