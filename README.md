
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>IBM ESPP FAQs</title>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    font-family: -apple-system, "Segoe UI", system-ui, sans-serif;
    font-size: 15px;
    line-height: 1.7;
    color: #1f2328;
    background: #fff;
  }

  .site-header {
    background: #1f2328;
    color: #fff;
    padding: 28px 32px;
  }
  .site-header h1 { font-size: 22px; font-weight: 700; }
  .site-header p  { color: #9ca3af; font-size: 13px; margin-top: 4px; }

  .page { max-width: 860px; margin: 0 auto; padding: 32px 24px 64px; }

  /* SECTION HEADINGS */
  .faq-section { margin-bottom: 44px; }
  .faq-section h2 {
    font-size: 17px;
    font-weight: 700;
    color: #1f2328;
    padding-bottom: 10px;
    border-bottom: 2px solid #e5e7eb;
    margin-bottom: 12px;
  }

  /* ACCORDION via <details>/<summary> — pure CSS, no JS */
  details {
    border: 1px solid #e5e7eb;
    border-radius: 8px;
    margin-bottom: 8px;
    overflow: hidden;
  }
  details[open] {
    border-color: #bfdbfe;
  }

  summary {
    list-style: none;
    cursor: pointer;
    padding: 14px 16px;
    background: #f7f8fa;
    font-size: 14px;
    font-weight: 600;
    color: #1f2328;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 12px;
    user-select: none;
  }
  summary::-webkit-details-marker { display: none; }
  summary::after {
    content: "";
    flex-shrink: 0;
    width: 18px;
    height: 18px;
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 20 20' fill='%2357606a'%3E%3Cpath fill-rule='evenodd' d='M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z' clip-rule='evenodd'/%3E%3C/svg%3E");
    background-repeat: no-repeat;
    background-size: contain;
    transition: transform 0.2s;
  }
  details[open] summary {
    background: #eff6ff;
    color: #1d4ed8;
  }
  details[open] summary::after {
    transform: rotate(180deg);
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 20 20' fill='%233b82d4'%3E%3Cpath fill-rule='evenodd' d='M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z' clip-rule='evenodd'/%3E%3C/svg%3E");
  }
  summary:hover { background: #eef0f3; }
  details[open] summary:hover { background: #dbeafe; }

  .answer {
    padding: 16px 18px;
    font-size: 14px;
    color: #374151;
    border-top: 1px solid #e5e7eb;
    background: #fff;
  }
  .answer p { margin-bottom: 10px; }
  .answer p:last-child { margin-bottom: 0; }
  .answer ul { margin: 6px 0 10px 20px; }
  .answer ul li { margin-bottom: 5px; }

  .note {
    background: #fffbeb;
    border-left: 3px solid #f59e0b;
    padding: 10px 14px;
    border-radius: 0 6px 6px 0;
    font-size: 13px;
    color: #92400e;
    margin-top: 10px;
  }
  .tip {
    background: #eff6ff;
    border-left: 3px solid #3b82d4;
    padding: 10px 14px;
    border-radius: 0 6px 6px 0;
    font-size: 13px;
    color: #1e3a5f;
    margin-top: 10px;
  }

  .country-group { margin-bottom: 10px; }
  .country-group strong { display: block; font-size: 12px; color: #57606a; margin-bottom: 2px; }
  .country-group span { font-size: 13px; color: #374151; }

  table.timing { width: 100%; border-collapse: collapse; font-size: 13px; margin-top: 10px; }
  table.timing th {
    background: #f7f8fa; border: 1px solid #e5e7eb; padding: 8px 12px;
    text-align: left; font-size: 12px; color: #57606a; font-weight: 600;
  }
  table.timing td { border: 1px solid #e5e7eb; padding: 8px 12px; vertical-align: top; }
  table.timing tr:nth-child(even) td { background: #f7f8fa; }

  .contact-box {
    background: #f7f8fa; border: 1px solid #e5e7eb;
    border-radius: 6px; padding: 12px 14px; font-size: 13px; margin-top: 10px;
  }
  .contact-box p { margin-bottom: 4px; }

  footer {
    text-align: center; font-size: 12px; color: #57606a;
    border-top: 1px solid #e5e7eb; padding: 20px;
  }
</style>
</head>
<body>

<div class="site-header">
  <h1>IBM Employee Stock Purchase Plan (ESPP) — FAQs</h1>
  <p>Reference guide for IBM employees — based on the official ESPP FAQ document</p>
</div>

<div class="page">

  
  <section class="faq-section">
    <h2>1. Participation</h2>

    <details>
      <summary>Who is eligible to participate in ESPP?</summary>
      <div class="answer">
        <p>As a general rule, all regular IBMers, including part-timers, are eligible to participate in the Plan, along with most supplemental employees, provided they live in a country where participation is permitted by local law and the Plan is offered by the local IBM subsidiary.</p>
        <div class="country-group"><strong>Americas</strong><span>Argentina, Bahamas, Barbados, Brazil, Canada, Chile, Colombia, Costa Rica, Curacao, Ecuador, Jamaica, Mexico, Peru, Trinidad, Uruguay, United States, Venezuela</span></div>
        <div class="country-group"><strong>Asia Pacific (AP)</strong><span>Australia, China, Hong Kong, India, Japan, Malaysia, New Zealand, Philippines, Singapore, South Korea, Taiwan, Thailand</span></div>
        <div class="country-group"><strong>EMEA</strong><span>Austria, Belgium, Bulgaria, Cyprus, Czech Republic, Croatia, Denmark, Egypt, Estonia, Finland, France, Germany, Greece, Hungary, Ireland, Israel, Italy, Latvia, Lithuania, Luxembourg, Netherlands, Norway, Pakistan, Poland, Portugal, Qatar, Romania, Saudi Arabia, Serbia, Slovakia, Slovenia, South Africa, Spain, Sweden, Switzerland, Turkiye, United Arab Emirates, United Kingdom</span></div>
      </div>
    </details>

    <details>
      <summary>How do I enroll?</summary>
      <div class="answer">
        <p>You can enroll using the enrollment instructions during one of the two enrollment windows per year. Be sure to review the enrollment tab prior to enrolling in the program.</p>
        <div class="tip">There are two enrollment windows each year: <strong>June 1–14</strong> and <strong>December 1–14</strong>.</div>
      </div>
    </details>

    <details>
      <summary>What if I already have a pending ESPP enrollment request or change to contribution in SAP SuccessFactors?</summary>
      <div class="answer">
        <p>If you previously submitted an ESPP enrollment request or change to contribution that is still pending, you'll need to withdraw that request before submitting a new one. SAP SuccessFactors will not allow a new submission until the previous request has been cleared.</p>
        <p>In some countries, earlier requests may have been sent back to you for correction or review. If that happened, the returned request will appear in your <strong>To Do</strong> list in SAP SuccessFactors. You must withdraw the sent-back request as well before you can proceed.</p>
        <p>Once the old request is withdrawn, you'll be able to enroll without issues.</p>
      </div>
    </details>

    <details>
      <summary>I followed the enrollment instructions but cannot confirm my enrollment was successfully submitted. Why?</summary>
      <div class="answer">
        <p>To confirm successful enrollment, check your Benefit Confirmation Statement by navigating to <strong>Benefits Overview</strong> in SuccessFactors and clicking <strong>View Benefits Confirmation Statement</strong>. Set the <em>As of Date</em> to the enrollment effective date:</p>
        <ul>
          <li>June enrollment window → <strong>July 1st</strong></li>
          <li>December enrollment window → <strong>January 1st</strong></li>
        </ul>
        <div class="note">If you are in <strong>Brazil, Croatia, Estonia, Latvia, Lithuania, Poland, Romania, Serbia, or Venezuela</strong>, your enrollment requires legal approval via an additional form. If you cannot download the form, open an AskHR ticket. Allow 1–2 weeks for legal approval. You will receive an email confirmation once approved.</div>
      </div>
    </details>

    <details>
      <summary>If I'm currently enrolled, do I need to enroll again during future enrollment windows?</summary>
      <div class="answer">
        <p>Generally, no action is needed if you would like to remain enrolled at your current contribution rate. The 15% discount will automatically be applied.</p>
        <p>You will need to re-enroll if:</p>
        <ul>
          <li>You are returning from a Leave of Absence.</li>
          <li>You were previously suspended and are eligible to re-enroll for the next Offering Period.</li>
          <li>You reach the annual maximum of <strong>$25,000 USD</strong> worth of shares in any calendar year or <strong>1,000 shares</strong> in any Offering Period. US payrolls are automatically re-enrolled at the start of the next calendar year; non-US payrolls must re-enroll manually.</li>
        </ul>
      </div>
    </details>

    <details>
      <summary>I'm a recent new hire. How long do I need to wait to enroll?</summary>
      <div class="answer">
        <p>As long as you are officially onboarded and meet all eligibility criteria, you can enroll during the enrollment window. If you join IBM after the current enrollment window, you will need to wait until the next one.</p>
        <div class="tip">There are typically two enrollment windows per year: <strong>June 1–14</strong> and <strong>December 1–14</strong>.</div>
      </div>
    </details>

    <details>
      <summary>I permanently transferred from one IBM entity/country to another. How does this impact my ESPP elections?</summary>
      <div class="answer">
        <p>If you permanently transfer from one IBM entity to another, your ESPP contributions do not automatically continue. You must re-enroll during the next global enrollment window (June or December).</p>
        <div class="note">If the transfer is temporary (e.g. a Global IBMer assignment), your ESPP contributions will continue in the country where your payroll is run.</div>
      </div>
    </details>

    <details>
      <summary>Are there additional steps to complete ESPP enrollment in my country?</summary>
      <div class="answer">
        <p>In most countries, enrollment in SuccessFactors is immediate and no further action is needed after submitting your contribution percentages.</p>
        <p>In <strong>Brazil, Italy, Croatia, Estonia, Latvia, Poland, Romania, Lithuania, Serbia, or Venezuela</strong>, there are additional steps. SuccessFactors will prompt you if additional documents are required, and local approvals will happen shortly after enrollment prior to the first ESPP deduction.</p>
      </div>
    </details>

    <details>
      <summary>I missed the enrollment window. Can I still join the ESPP?</summary>
      <div class="answer">
        <p>Unfortunately, you can only enroll during the designated enrollment window before each offering period. There are two offering periods each year:</p>
        <ul>
          <li><strong>January 1 – June 30</strong> — Enrollment: December 1–14</li>
          <li><strong>July 1 – December 31</strong> — Enrollment: June 1–14</li>
        </ul>
        <p>If you've missed the current enrollment window, you'll need to wait until the next one.</p>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>2. Eligible Compensation &amp; Payroll Deduction</h2>

    <details>
      <summary>How much can I contribute?</summary>
      <div class="answer">
        <p>You may contribute from <strong>1% to 10%</strong> of your pay, up to certain plan and regulatory limits (all currency references are in USD).</p>
        <p>The Plan limits you to purchasing a maximum value of <strong>$25,000 of shares in any calendar year</strong> (based on the average market price on the first day of each Offering Period). In no event can you purchase more than <strong>1,000 shares</strong> in any single Offering Period.</p>
        <div class="note">In the U.S., the ESPP deduction is taken after most other program deductions (e.g. 401(k) Plus Plan). Partial ESPP deductions are not permitted.</div>
      </div>
    </details>

    <details>
      <summary>Can I elect different contribution percentages for different types of pay?</summary>
      <div class="answer">
        <p>Yes. When enrolling you can authorize a deduction from:</p>
        <ul>
          <li><strong>IBM Base Pay / Salary</strong> — compensation received regularly in the same amount, including recurring commission advances, vacation/holiday pay, and Short Term Disability benefits.</li>
          <li><strong>IBM Other Compensation</strong> — incentive payments, commissions, variable pay, and other compensation.</li>
        </ul>
        <p>When deductions are made from both, they may be for the same or different percentages, but neither may be less than 1% nor more than 10%.</p>
      </div>
    </details>

    <details>
      <summary>Can I make changes to my contributions after the enrollment window is closed?</summary>
      <div class="answer">
        <p>You can <strong>increase or decrease</strong> your contribution percentage during an enrollment window. After the window closes, you can still <strong>decrease</strong> your contribution during the offering period, but you cannot <strong>increase</strong> it until the next enrollment window.</p>
        <p>You can withdraw from the plan at any time.</p>
      </div>
    </details>

    <details>
      <summary>How is the IBM stock price determined when stock is purchased on each payroll date?</summary>
      <div class="answer">
        <p>The IBM stock price will be <strong>85% of the average of the high and low IBM stock prices</strong> on each payroll date — giving you a 15% discount on each purchase.</p>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>3. EquatePlus Platform</h2>

    <details>
      <summary>I cannot access my EquatePlus account / I'm having login issues. What should I do?</summary>
      <div class="answer">
        <p>Select the <strong>Help</strong> link on the main EquatePlus login page, then follow the instructions that fit your situation. That page also includes contact details for Computershare's call center.</p>
      </div>
    </details>

    <details>
      <summary>Why do I have both an EquatePlus account and an Investment Center account?</summary>
      <div class="answer">
        <p>A small number of participants have separate accounts across Computershare's Investor Center and EquatePlus platforms. The most common reason is holding paper stock certificates — an account with paper certificates cannot be merged with one holding book-entry shares until the certificates are collected.</p>
        <p>Contact <strong>infoibm@us.ibm.com</strong> so that Computershare can look into whether consolidating the accounts is possible.</p>
      </div>
    </details>

    <details>
      <summary>Why are my first and last names interchanged in my EquatePlus account?</summary>
      <div class="answer">
        <p>The name displayed in EquatePlus is fed by monthly or bi-monthly files from IBM. If you would like to change the name displayed, raise an <strong>AskHR ticket</strong> to ensure the next file sent to Computershare matches your SAP SuccessFactors profile.</p>
      </div>
    </details>

    <details>
      <summary>How can I update my address and personal details in EquatePlus?</summary>
      <div class="answer">
        <p>Active employees' address and personal details are updated via inbound files to Computershare. Terminated employees should contact Computershare directly for name and address changes.</p>
      </div>
    </details>

    <details>
      <summary>After my contributions are deducted, how many days will it take to see shares in my EquatePlus account?</summary>
      <div class="answer">
        <p>Timing differs by country. See the table below. Any delays are monitored closely by IBM and EquatePlus; updates are shared in <strong>#espp-ibmshare</strong> on Slack or emailed directly to participants.</p>
        <table class="timing">
          <thead><tr><th>Timeframe</th><th>Countries</th></tr></thead>
          <tbody>
            <tr><td><strong>1–10 days</strong></td><td>Argentina, Canada, Costa Rica, France, Germany, Latvia, Mexico, Netherlands, Pakistan, Romania, Singapore, South Korea, Spain, Sweden, Switzerland, Trinidad, United Kingdom, United States</td></tr>
            <tr><td><strong>10–20 days</strong></td><td>Austria, Barbados, Belgium, Brazil, Bulgaria, Chile, Colombia, Czechia, Ecuador, Egypt, Estonia, Finland, Hong Kong, Hungary, India, Ireland, Israel, Jamaica, Lithuania, Malaysia, New Zealand, Peru, Philippines, Poland, Portugal, Qatar, Saudi Arabia, Serbia, Slovakia, Slovenia, South Africa, Taiwan, Thailand, Turkey, UAE, Uruguay, Venezuela</td></tr>
            <tr><td><strong>20+ days</strong></td><td>Australia, China, Croatia, Cyprus, Denmark, Greece, Japan, Norway</td></tr>
          </tbody>
        </table>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>4. Discontinuing Participation</h2>

    <details>
      <summary>How can I opt out of the program?</summary>
      <div class="answer">
        <p>You can opt out at any time in <strong>SAP SuccessFactors</strong>. Go to the <em>Benefits</em> section in your profile → <em>Go To Benefits</em> → click the <strong>Opt Out</strong> button in the ESPP section.</p>
        <div class="note">This may take a full pay cycle to be applied — it will take effect within 1–2 paychecks after you opt out.</div>
      </div>
    </details>

    <details>
      <summary>What happens to my IBM stock balance if I withdraw, retire, or leave IBM?</summary>
      <div class="answer">
        <p>The shares you have accumulated will remain in your IBM participant account with Computershare until you either request the shares or authorize their sale.</p>
        <div class="tip">If you retire or leave IBM, update Computershare with a <strong>non-IBM email address</strong> so you continue to receive important communications after losing access to your IBM email.</div>
      </div>
    </details>

    <details>
      <summary>I opted out, but ESPP was still deducted from my pay. Why?</summary>
      <div class="answer">
        <p>This could be a timing issue. Check your ESPP participation status in SuccessFactors to confirm your participation was successfully terminated. If deductions continue, contact <strong>Computershare</strong> directly.</p>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>5. Suspension</h2>

    <details>
      <summary>Why did my ESPP payroll deduction stop? I see an 'ESPP refund' on my payslip.</summary>
      <div class="answer">
        <p>Suspension from ESPP may occur if:</p>
        <ul>
          <li>You go on a leave of absence.</li>
          <li>You reach the $25,000 annual limit or purchase 1,000 shares in an Offering Period.</li>
          <li>The total number of ESPP shares available for purchase during an offering period is reached.</li>
        </ul>
      </div>
    </details>

    <details>
      <summary>If my participation is suspended, is reinstatement automatic?</summary>
      <div class="answer">
        <p><strong>US payroll participants:</strong></p>
        <ul>
          <li>Suspended due to the $25,000 or 1,000-share limit: reinstatement is automatic when you become eligible again.</li>
          <li>Suspended due to an Offering Period share limit: reinstatement is automatic.</li>
          <li>Suspended due to a leave of absence: reinstatement is automatic upon return.</li>
        </ul>
        <div class="note"><strong>Non-US payroll participants:</strong> It is recommended that you re-enroll at your desired contribution rate during the next enrollment window. Administration may differ by country and not all payrolls auto-reinstate participation. It is your responsibility to ensure your payroll department is carrying out your instructions.</div>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>6. Viewing, Selling &amp; Transferring Shares</h2>

    <details>
      <summary>How do I check and manage my stocks in EquatePlus?</summary>
      <div class="answer">
        <p>Log into your EquatePlus account and refer to the <strong>Overview</strong>, <strong>Library</strong>, and <strong>Help</strong> menus to check and manage your stocks.</p>
      </div>
    </details>

    <details>
      <summary>I see my ESPP deduction on my payslip but don't see shares in EquatePlus. Why?</summary>
      <div class="answer">
        <p>The timing for purchases being posted depends on the IBM payroll system sending purchase information to Computershare. For non-US payrolls, pay dates generally fall at the end of each month, and it may take <strong>2–3 weeks</strong> for the local payroll team to send purchase instructions. Deductions made at the end of a month may not appear in EquatePlus until midway through the following month.</p>
      </div>
    </details>

    <details>
      <summary>How do I sell my stock?</summary>
      <div class="answer">
        <p>Sale or transfer requests may be submitted through <strong>EquatePlus</strong> or <strong>EquateMobile</strong> 24 hours a day, 7 days a week. You may receive payment in one of 100 different currencies via funds transfer.</p>
        <div class="contact-box">
          <p><strong>Computershare contact numbers:</strong></p>
          <p>U.S., Canada and Puerto Rico: <strong>1-888-426-6700</strong>  |  Hearing impaired: 800-490-1493</p>
          <p>Outside U.S., Canada and Puerto Rico: <strong>781-575-2727</strong>  |  Hearing impaired: 781-575-2694</p>
        </div>
        <div class="note">Computershare charges a transaction fee of approximately $19.95 per sale (on or after April 1, 2022). Proceeds are sent electronically to banking details on file. Checks are mailed the third business day after the sale if no banking details are on file.</div>
      </div>
    </details>

    <details>
      <summary>How long do I have to hold shares before I can sell?</summary>
      <div class="answer">
        <p>You can sell your shares anytime after they are credited to your EquatePlus account. However, there may be tax consequences depending on how long you have held your shares and the tax laws in your country.</p>
        <div class="note">U.S. employees enjoy special treatment under Federal income tax rules which defers tax until disposition of the shares if held for the required period. Consult your own tax advisor for guidance.</div>
      </div>
    </details>

    <details>
      <summary>How do I transfer my stock from Computershare to a financial institution?</summary>
      <div class="answer">
        <p>Depending on your country of residence, you may be able to electronically transfer shares to your book-entry account at your bank or brokerage:</p>
        <ul>
          <li>Enter your brokerage account information under <strong>Financial Preferences</strong> in EquatePlus.</li>
          <li>Submit an online broker transfer request by clicking the <strong>Transact</strong> button on the EquatePlus home page.</li>
        </ul>
        <div class="tip">Neither Computershare nor IBM charges transfer fees. Any fees are charged by the receiving broker — ask your broker before initiating a transfer. Only brokers that are members of the DTC system are included in the Computershare system.</div>
      </div>
    </details>

    <details>
      <summary>How does currency conversion work when selling shares?</summary>
      <div class="answer">
        <p>The exchange rate received depends on the trading market, transaction value, and the fee arrangement with Computershare's partner bank. Because individual ESPP transactions are small relative to interbank trades, individuals will receive a retail bank rate which can include <strong>up to a 3% fee</strong> on the proceeds.</p>
      </div>
    </details>

    <details>
      <summary>Which brokers can I transfer to? Where do transfer fees come from?</summary>
      <div class="answer">
        <p>Neither Computershare nor IBM charge transfer fees for transferring to a broker. Any transfer fees are charged by the <strong>receiving broker</strong>. Be sure to ask your broker if there are any fees associated with a transfer.</p>
        <p>Only brokers that are members of the DTC system are included in the Computershare system. Contact Computershare to check whether other brokers can be added.</p>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>7. Dividends</h2>

    <details>
      <summary>How are my dividends paid?</summary>
      <div class="answer">
        <p>You will receive dividends based on the number of shares held. You have three options:</p>
        <ul>
          <li><strong>Automatic reinvestment (default for enrollees from January 1, 2023):</strong> Dividends are reinvested in additional IBM stock at fair market value (not at the ESPP discount). The current fee is 2% or a maximum of $3 per dividend payment.</li>
          <li><strong>Electronic transfer to your bank / broker:</strong> Add your ACH or wire bank account details to EquatePlus. Fees may apply.</li>
          <li><strong>USD check:</strong> Sent only if no bank account details are on file.</li>
        </ul>
        <div class="note">Non-US employees can elect to receive dividends in their local currency by adding wire details to EquatePlus (subject to a $10 wire fee). If no wire details are on file, you will receive a USD check.</div>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>8. Taxation</h2>

    <details>
      <summary>Do I pay tax when the stock is purchased on my behalf?</summary>
      <div class="answer">
        <p>In many countries, you are taxed on the discount you receive on shares you purchase. The tax is withheld by local payroll in some countries; in others you are responsible for complying with local tax obligations.</p>
        <div class="tip">Refer to the Global Tax Guide for information covering 43 countries. For advice on specific situations, consult a local financial advisor or tax professional.</div>
        <p>You are strongly encouraged to certify through <strong>Form W-9BEN</strong> (U.S.) or <strong>Form W-8BEN</strong> (outside U.S.) via your EquatePlus account to avoid excess tax withholding.</p>
      </div>
    </details>

    <details>
      <summary>Do I pay tax when I sell my stock?</summary>
      <div class="answer">
        <p>There may be tax consequences when you sell your IBM stock, depending on how long you have held your shares and the tax laws in your country.</p>
        <div class="note">U.S. employees enjoy special treatment under federal income tax rules which defers tax until the disposition of the shares if held for the required period. Consult a financial advisor or local tax professional for advice on specific situations.</div>
      </div>
    </details>

    <details>
      <summary>What is a W-8BEN / W-9BEN and should I fill one out?</summary>
      <div class="answer">
        <p><strong>Form W-9BEN</strong> is required for all U.S. taxpayers. Failure to complete it results in <strong>24% U.S. tax withholding</strong> on sale proceeds and dividends. Submit via EquatePlus or EquateMobile. The form expires at the end of the third calendar year after completion — you must renew it before expiry.</p>
        <p><strong>Form W-8BEN</strong> is the equivalent form for non-U.S. taxpayers. The same rules apply.</p>
        <div class="tip">EquatePlus will prompt you when a new form needs to be completed.</div>
      </div>
    </details>

    <details>
      <summary>What is an ESPP Disqualifying Disposition (423b)?</summary>
      <div class="answer">
        <p>A disqualifying disposition occurs when you sell or otherwise transfer ESPP stock from a tax-qualified Section 423 plan without satisfying the ESPP holding periods of more than:</p>
        <ul>
          <li>Two years from grant (the offering commencement date)</li>
          <li>One year from purchase</li>
        </ul>
        <div class="note">Participants residing <strong>outside the United States</strong> are not subject to disqualifying disposition reporting. Non-US participants should ignore references to disqualifying disposition and 423b.</div>
      </div>
    </details>

    <details>
      <summary>I'm confused about the taxation of my ESPP shares. What do I do?</summary>
      <div class="answer">
        <p>Review the questions above and the Global Tax Guide. Computershare cannot provide tax advice. It is best to speak to a local tax professional if you have additional questions.</p>
      </div>
    </details>

    <details>
      <summary>What is my FTIN (Foreign Tax Identification Number)?</summary>
      <div class="answer">
        <p>A Foreign Tax Identification Number (FTIN) is a unique identifier assigned to individuals and entities by their country's tax authority for tax purposes. For additional information, click the <strong>?</strong> in the FTIN section of the tax form in EquatePlus.</p>
      </div>
    </details>

  </section>

  
  <section class="faq-section">
    <h2>9. Miscellaneous</h2>

    <details>
      <summary>Can I request stock certificates?</summary>
      <div class="answer">
        <p>Yes. You may request a stock certificate for some or all of the full shares of IBM stock held in your account by contacting Computershare.</p>
      </div>
    </details>

    <details>
      <summary>Do I need to designate a beneficiary for my ESPP shares?</summary>
      <div class="answer">
        <p>No. There is no "beneficiary" designation under ESPP. You may purchase shares in your name alone, or jointly with a family member with right of survivorship (joint tenancy). You can add a joint holder online through EquatePlus under <strong>Personal Preferences</strong>.</p>
        <div class="note">If you live in a jurisdiction that does not recognize joint tenancy, you may register shares as "tenant in common" or as community property. Consult a qualified legal advisor before committing to stock purchases in joint names.</div>
      </div>
    </details>

    <details>
      <summary>I need to transfer my ESPP participation due to global relocation. How do I do this?</summary>
      <div class="answer">
        <p>Contact Computershare directly.</p>
      </div>
    </details>

    <details>
      <summary>How do I get a history of all my ESPP contributions to date?</summary>
      <div class="answer">
        <p>Historical purchase information is available by navigating to the <strong>Plan Details</strong> page on EquatePlus and selecting <strong>Archive Purchases</strong>.</p>
      </div>
    </details>

    <details>
      <summary>Where can I provide feedback on my experience with Computershare's support?</summary>
      <div class="answer">
        <p>Please raise an <strong>AskHR ticket</strong> if you raised an issue with Computershare's support team and it was not resolved, or if you had a negative experience. Customer satisfaction is closely monitored.</p>
      </div>
    </details>

    <details>
      <summary>Where can I find the ESPP policy and enrollment guide?</summary>
      <div class="answer">
        <p>You can find the ESPP policy and enrollment guide on the IBM HR benefits portal:</p>
        <p><a href="https://w3.ibm.com/w3publisher/global-compensation-programs/espp/espp-faqs">w3.ibm.com → Global Compensation Programs → ESPP → ESPP FAQs</a></p>
        <p>The documents include: eligibility requirements, enrollment windows, contribution limits, purchase dates, withdrawal rules, and frequently asked questions.</p>
      </div>
    </details>

  </section>

</div>

<footer>Made with IBM Bob</footer>

</body>
</html>
