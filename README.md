<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>MyCalculator — Free Online Calculators</title>
  <meta name="description" content="MyCalculator: Free online calculators — Loan, BMI, Age, Tax and more. Fast, simple and accurate tools for everyday use." />
  <style>
    /* ---------- BASIC RESET ---------- */
    *{box-sizing:border-box;margin:0;padding:0}
    html,body{height:100%;font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial; color:#1f2937}
    a{color:inherit;text-decoration:none}
    button{cursor:pointer}

    /* ---------- LAYOUT ---------- */
    .container{max-width:1100px;margin:0 auto;padding:20px}
    header{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
    .logo{display:flex;align-items:center;gap:12px;font-weight:700;font-size:18px;color:#0b63a7}
    .logo svg{width:40px;height:40px}
    nav ul{display:flex;gap:18px;list-style:none;align-items:center}
    nav a{padding:8px 10px;border-radius:6px;font-weight:600;color:#374151}
    nav a:hover{background:#eef2ff;color:#0b63a7}

    .cta{background:#0b63a7;color:#fff;padding:8px 12px;border-radius:8px;font-weight:700}
    .searchbar{display:flex;align-items:center;background:#f3f4f6;border-radius:8px;padding:6px 10px;gap:8px}
    .searchbar input{border:0;background:transparent;outline:none;width:200px;font-size:14px}

    /* ---------- HERO ---------- */
    .hero{display:flex;align-items:center;gap:30px;padding:28px 0}
    .hero-left{flex:1}
    .hero h1{font-size:40px;line-height:1.02;color:#0b2540;margin-bottom:10px}
    .hero p{color:#4b5563;margin-bottom:14px}
    .hero .primary-btn{background:#0b63a7;color:#fff;padding:10px 16px;border-radius:8px;font-weight:700}

    .hero-right{width:360px;background:linear-gradient(180deg,#ffffff,#f8fafc);border-radius:12px;padding:18px;box-shadow:0 8px 30px rgba(6,78,59,0.05)}
    .card-list{display:grid;grid-template-columns:repeat(2,1fr);gap:10px}
    .calc-card{background:#fff;padding:10px;border-radius:10px;box-shadow:0 6px 18px rgba(13,42,71,0.04);display:flex;flex-direction:column;gap:8px}
    .calc-card button{margin-top:auto;padding:8px;border-radius:8px;border:0;background:#0b63a7;color:white;font-weight:700}

    /* ---------- GRID ---------- */
    .grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:26px}
    .card{background:#fff;padding:18px;border-radius:10px;box-shadow:0 8px 24px rgba(2,6,23,0.04)}
    .card h3{margin-bottom:8px;color:#0b3a66}
    .card p{color:#475569;font-size:14px;margin-bottom:12px}

    /* ---------- Calculator sections ---------- */
    .calc-section{margin-top:28px;background:#fff;padding:18px;border-radius:10px;box-shadow:0 6px 18px rgba(2,6,23,0.04)}
    .form-row{display:flex;gap:12px;margin-bottom:12px;flex-wrap:wrap}
    input[type=number], input[type=text], select{padding:10px;border:1px solid #e6e9ef;border-radius:8px;min-width:120px}
    .result{margin-top:12px;padding:12px;border-radius:8px;background:#f1f5f9;color:#0b2540;font-weight:700}

    /* ---------- FOOTER ---------- */
    footer{margin-top:40px;padding:18px 0;color:#64748b;text-align:center}

    /* ---------- RESPONSIVE ---------- */
    @media (max-width:900px){
      .grid{grid-template-columns:repeat(2,1fr)}
      .hero-right{display:none}
      .searchbar input{width:120px}
    }
    @media (max-width:600px){
      header{flex-direction:column;align-items:flex-start;gap:10px}
      .grid{grid-template-columns:1fr}
      .hero{flex-direction:column}
      .hero h1{font-size:28px}
    }
  </style>
</head>
<body>
  <div class="container">
    <!-- HEADER -->
    <header>
      <div class="logo">
        <!-- Simple inline SVG logo -->
        <svg viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <rect x="4" y="6" width="40" height="36" rx="6" fill="#e6f2ff"/>
          <rect x="10" y="12" width="28" height="6" rx="2" fill="#0b63a7"/>
          <g transform="translate(10,22)" fill="#0b63a7">
            <circle cx="4" cy="4" r="3"/>
            <circle cx="12" cy="4" r="3"/>
            <circle cx="20" cy="4" r="3"/>
            <circle cx="4" cy="12" r="3"/>
            <circle cx="12" cy="12" r="3"/>
            <circle cx="20" cy="12" r="3"/>
          </g>
        </svg>
        MyCalculator
      </div>

      <nav>
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#calculators">Calculators</a></li>
          <li><a href="#blog">Blog</a></li>
          <li><a href="#about">About</a></li>
          <li><a href="#contact">Contact</a></li>
          <li>
            <div class="searchbar" role="search">
              <svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M21 21l-4.35-4.35" stroke="#6b7280" stroke-width="2" stroke-linecap="round"/></svg>
              <input id="searchCalc" placeholder="Search calculators..." />
            </div>
          </li>
          <li><a class="cta" href="#calculators">Use Calculator</a></li>
        </ul>
      </nav>
    </header>

    <!-- HERO -->
    <section class="hero">
      <div class="hero-left">
        <h1>Free Online Calculators for Finance, Health & Everyday Use</h1>
        <p>Fast, accurate and mobile-friendly calculators — Loan, BMI, Age, Tax and many more. Use instantly without signup.</p>
        <div style="display:flex;gap:10px;margin-top:12px">
          <a class="primary-btn" href="#calculators">Browse Calculators</a>
          <a style="padding:10px;border-radius:8px;border:1px solid #e6eef8;font-weight:700" href="#bmi">Try BMI</a>
        </div>
      </div>

      <aside class="hero-right">
        <div style="font-weight:700;margin-bottom:10px">Popular tools</div>
        <div class="card-list">
          <div class="calc-card">
            <div style="font-size:15px;font-weight:700">Loan Calculator</div>
            <div style="font-size:13px;color:#6b7280">EMI & Interest estimate</div>
            <button onclick="location.href='#loan'">Open</button>
          </div>
          <div class="calc-card">
            <div style="font-size:15px;font-weight:700">BMI Calculator</div>
            <div style="font-size:13px;color:#6b7280">Health & Fitness</div>
            <button onclick="location.href='#bmi'">Open</button>
          </div>
          <div class="calc-card">
            <div style="font-size:15px;font-weight:700">Age Calculator</div>
            <div style="font-size:13px;color:#6b7280">Find age from DOB</div>
            <button onclick="alert('Coming soon')">Open</button>
          </div>
          <div class="calc-card">
            <div style="font-size:15px;font-weight:700">Unit Converter</div>
            <div style="font-size:13px;color:#6b7280">Length, Weight, Temp</div>
            <button onclick="alert('Coming soon')">Open</button>
          </div>
        </div>
      </aside>
    </section>

    <!-- CALCULATORS GRID -->
    <section id="calculators" class="grid">
      <div class="card">
        <h3>BMI Calculator</h3>
        <p>Calculate Body Mass Index quickly — enter weight and height, get BMI and category.</p>
        <a class="cta" href="#bmi" style="display:inline-block;margin-top:10px">Open BMI</a>
      </div>

      <div class="card">
        <h3>Loan Calculator</h3>
        <p>Estimate monthly EMI, total interest and total payment for loans.</p>
        <a class="cta" href="#loan" style="display:inline-block;margin-top:10px">Open Loan</a>
      </div>

      <div class="card">
        <h3>Age Calculator</h3>
        <p>Find exact age from date of birth (years, months, days).</p>
        <a class="cta" href="#age" style="display:inline-block;margin-top:10px">Open Age</a>
      </div>
    </section>

    <!-- BMI CALCULATOR -->
    <section id="bmi" class="calc-section">
      <h2>BMI Calculator</h2>
      <div class="form-row">
        <div>
          <label>Weight (kg)</label><br>
          <input id="bmiWeight" type="number" min="1" step="0.1" placeholder="e.g. 70" />
        </div>
        <div>
          <label>Height (cm)</label><br>
          <input id="bmiHeight" type="number" min="30" step="0.1" placeholder="e.g. 170" />
        </div>
        <div style="display:flex;align-items:flex-end">
          <button onclick="calculateBMI()" style="padding:10px 12px;border-radius:8px;background:#0b63a7;color:#fff;border:0;font-weight:700">Calculate</button>
        </div>
      </div>
      <div id="bmiResult" class="result" style="display:none"></div>
      <p style="margin-top:12px;color:#475569;font-size:14px">BMI (Body Mass Index) = weight (kg) / (height (m))²</p>
    </section>

    <!-- LOAN CALCULATOR -->
    <section id="loan" class="calc-section">
      <h2>Loan / EMI Calculator</h2>
      <div class="form-row">
        <div>
          <label>Loan Amount</label><br>
          <input id="loanAmount" type="number" min="1" step="0.01" placeholder="e.g. 500000" />
        </div>
        <div>
          <label>Annual Interest Rate (%)</label><br>
          <input id="loanRate" type="number" min="0" step="0.01" placeholder="e.g. 7.5" />
        </div>
        <div>
          <label>Tenure (years)</label><br>
          <input id="loanYears" type="number" min="0.1" step="0.1" placeholder="e.g. 5" />
        </div>
        <div style="display:flex;align-items:flex-end">
          <button onclick="calculateLoan()" style="padding:10px 12px;border-radius:8px;background:#0b63a7;color:#fff;border:0;font-weight:700">Calculate EMI</button>
        </div>
      </div>

      <div id="loanResult" class="result" style="display:none"></div>
      <p style="margin-top:12px;color:#475569;font-size:14px">EMI = [P × r × (1+r)^n] / [(1+r)^n – 1] where r = monthly rate, n = months</p>
    </section>

    <!-- AGE CALCULATOR (simple display) -->
    <section id="age" class="calc-section">
      <h2>Age Calculator (Quick)</h2>
      <div class="form-row">
        <div>
          <label>Date of Birth</label><br>
          <input id="dob" type="date" />
        </div>
        <div style="display:flex;align-items:flex-end">
          <button onclick="calculateAge()" style="padding:10px 12px;border-radius:8px;background:#0b63a7;color:#fff;border:0;font-weight:700">Calculate Age</button>
        </div>
      </div>
      <div id="ageResult" class="result" style="display:none"></div>
    </section>

    <footer>
      © <span id="year"></span> MyCalculator • Free online calculators • Privacy • Contact
    </footer>
  </div>

  <script>
    // set year
    document.getElementById('year').textContent = new Date().getFullYear();

    // SEARCH (basic)
    document.getElementById('searchCalc').addEventListener('keydown', function(e){
      if(e.key === 'Enter'){
        const q = this.value.trim().toLowerCase();
        if(!q) return;
        // very simple search mapping
        if(q.includes('bmi')) location.href = '#bmi';
        else if(q.includes('loan') || q.includes('emi')) location.href = '#loan';
        else if(q.includes('age')) location.href = '#age';
        else alert('No direct match found. Try keywords: bmi, loan, age');
      }
    });

    // BMI CALC
    function calculateBMI(){
      const w = parseFloat(document.getElementById('bmiWeight').value);
      const hcm = parseFloat(document.getElementById('bmiHeight').value);
      const out = document.getElementById('bmiResult');

      if(!w || !hcm){ out.style.display='block'; out.textContent = 'Please enter weight and height.'; return; }

      const h = hcm / 100;
      const bmi = w / (h*h);
      const bmiRounded = Math.round(bmi * 10) / 10;
      let cat = '';
      if(bmi < 18.5) cat = 'Underweight';
      else if(bmi < 25) cat = 'Normal weight';
      else if(bmi < 30) cat = 'Overweight';
      else cat = 'Obesity';

      out.style.display='block';
      out.innerHTML = `Your BMI is <strong>${bmiRounded}</strong> — <em>${cat}</em>`;
    }

    // LOAN CALC
    function calculateLoan(){
      const P = parseFloat(document.getElementById('loanAmount').value);
      const annualRate = parseFloat(document.getElementById('loanRate').value);
      const years = parseFloat(document.getElementById('loanYears').value);
      const out = document.getElementById('loanResult');

      if(!P || !annualRate || !years){ out.style.display='block'; out.textContent='Please enter amount, interest rate and tenure.'; return; }

      const r = (annualRate / 100) / 12; // monthly rate
      const n = Math.round(years * 12);
      const numerator = P * r * Math.pow(1 + r, n);
      const denominator = Math.pow(1 + r, n) - 1;
      const emi = numerator / denominator;
      const totalPayment = emi * n;
      const totalInterest = totalPayment - P;

      out.style.display='block';
      out.innerHTML = `
        EMI (monthly): <strong>${emi.toFixed(2)}</strong><br>
        Total Interest: <strong>${totalInterest.toFixed(2)}</strong><br>
        Total Payment: <strong>${totalPayment.toFixed(2)}</strong>
      `;
    }

    // AGE CALC
    function calculateAge(){
      const dob = document.getElementById('dob').value;
      const out = document.getElementById('ageResult');
      if(!dob){ out.style.display='block'; out.textContent='Please choose your date of birth.'; return; }

      const birth = new Date(dob);
      const now = new Date();
      if(birth > now){ out.style.display='block'; out.textContent='Date of birth cannot be in future.'; return; }

      let years = now.getFullYear() - birth.getFullYear();
      let months = now.getMonth() - birth.getMonth();
      let days = now.getDate() - birth.getDate();

      if(days < 0){
        const prevMonth = new Date(now.getFullYear(), now.getMonth(), 0);
        days += prevMonth.getDate();
        months--;
      }
      if(months < 0){
        months += 12;
        years--;
      }

      out.style.display='block';
      out.innerHTML = `Age: <strong>${years}</strong> years, <strong>${months}</strong> months, <strong>${days}</strong> days.`;
    }
  </script>
</body>
</html>
