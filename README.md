<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Ramprasath V — GitHub Profile</title>
<style>
  :root {
    --accent: #1D9E75;
    --accent-light: #E1F5EE;
    --accent-border: #9FE1CB;
    --accent-dark: #085041;
    --bg: #ffffff;
    --bg2: #f7f7f5;
    --border: 1px solid #e5e5e2;
    --text: #1a1a18;
    --muted: #6b6b68;
    --r: 12px;
    --font: 'Segoe UI', system-ui, -apple-system, sans-serif;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: var(--font);
    background: var(--bg);
    color: var(--text);
    max-width: 720px;
    margin: 0 auto;
    padding: 2rem 1.25rem 3rem;
  }

  /* ── Hero ─────────────────────────────────── */
  .hero {
    text-align: center;
    padding: 2.25rem 1.5rem;
    border: var(--border);
    border-radius: var(--r);
    background: var(--bg2);
    margin-bottom: 1.5rem;
  }
  .avatar {
    width: 76px; height: 76px; border-radius: 50%;
    background: var(--accent);
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 1rem;
    font-size: 28px; font-weight: 600; color: #fff; letter-spacing: 1px;
  }
  .hero h1 { font-size: 24px; font-weight: 600; margin-bottom: .3rem; }
  .hero .sub { font-size: 14px; color: var(--muted); line-height: 1.7; margin-bottom: .9rem; }
  .tag-row { display: flex; flex-wrap: wrap; gap: 6px; justify-content: center; margin-bottom: 1rem; }
  .tag {
    font-size: 11px; padding: 3px 11px; border-radius: 20px;
    border: var(--border); color: var(--muted); background: var(--bg);
  }
  .tag.green { background: var(--accent-light); color: var(--accent-dark); border-color: var(--accent-border); }
  .links { display: flex; gap: .75rem; justify-content: center; flex-wrap: wrap; }
  .link-btn {
    font-size: 13px; text-decoration: none; display: inline-flex; align-items: center; gap: 5px;
    padding: 5px 14px; border-radius: 20px;
    background: var(--accent-light); color: var(--accent-dark); border: 1px solid var(--accent-border);
  }
  .link-btn:hover { background: #c8f0e0; }

  /* ── Section ──────────────────────────────── */
  .section { margin-bottom: 1.5rem; }
  .sec-title {
    font-size: 11px; font-weight: 600; letter-spacing: .1em;
    color: var(--muted); text-transform: uppercase;
    display: flex; align-items: center; gap: 8px; margin-bottom: .9rem;
  }
  .sec-title::after { content: ''; flex: 1; height: 1px; background: #e5e5e2; }

  /* ── Stats ───────────────────────────────── */
  .stat-row { display: grid; grid-template-columns: repeat(3, 1fr); gap: .75rem; }
  .stat {
    text-align: center; padding: 1.1rem .5rem;
    background: var(--bg2); border: var(--border); border-radius: var(--r);
  }
  .stat .num { font-size: 26px; font-weight: 600; color: var(--accent); }
  .stat .lbl { font-size: 12px; color: var(--muted); margin-top: 4px; }

  /* ── About box ───────────────────────────── */
  .about-box {
    font-size: 14px; color: var(--muted); line-height: 1.8;
    padding: .9rem 1.1rem; background: var(--bg2);
    border: var(--border); border-radius: var(--r);
    border-left: 3px solid var(--accent);
  }

  /* ── Skill grid ──────────────────────────── */
  .skill-grid { display: grid; grid-template-columns: 1fr 1fr; gap: .75rem; }
  .skill-card {
    background: var(--bg); border: var(--border); border-radius: var(--r); padding: .9rem 1rem;
  }
  .skill-card h3 {
    font-size: 12px; font-weight: 600; color: var(--muted);
    margin-bottom: .6rem; display: flex; align-items: center; gap: 6px;
  }
  .skill-card h3 svg { flex-shrink: 0; }
  .pill-row { display: flex; flex-wrap: wrap; gap: 5px; }
  .pill {
    font-size: 11px; padding: 3px 9px; border-radius: 10px;
    background: var(--bg2); border: var(--border); color: var(--text);
  }
  .pill.hl { background: var(--accent-light); color: var(--accent-dark); border-color: var(--accent-border); }

  /* ── Projects ────────────────────────────── */
  .proj-list { display: flex; flex-direction: column; gap: .75rem; }
  .proj-card {
    background: var(--bg); border: var(--border); border-radius: var(--r);
    padding: 1rem 1.25rem; border-left: 3px solid var(--accent);
  }
  .proj-header {
    display: flex; align-items: flex-start; justify-content: space-between;
    gap: 8px; margin-bottom: .4rem;
  }
  .proj-title { font-size: 15px; font-weight: 600; color: var(--text); }
  .proj-link {
    font-size: 12px; color: var(--accent); text-decoration: none;
    white-space: nowrap; flex-shrink: 0; padding-top: 2px;
  }
  .proj-link:hover { text-decoration: underline; }
  .proj-desc { font-size: 13px; color: var(--muted); line-height: 1.65; margin-bottom: .65rem; }
  .badge-row { display: flex; flex-wrap: wrap; gap: 5px; }
  .badge {
    font-size: 11px; padding: 2px 8px; border-radius: 8px;
    background: var(--bg2); border: var(--border); color: var(--muted);
  }

  /* ── Table ───────────────────────────────── */
  .data-table { width: 100%; border-collapse: collapse; font-size: 13px; }
  .data-table th {
    font-size: 11px; font-weight: 600; color: var(--muted); text-align: left;
    padding: 5px 8px; border-bottom: var(--border);
  }
  .data-table td { padding: 9px 8px; color: var(--text); border-bottom: var(--border); }
  .data-table td:last-child { color: var(--muted); white-space: nowrap; }
  .data-table tr:last-child td { border-bottom: none; }

  /* ── Certs ───────────────────────────────── */
  .cert-row {
    display: flex; align-items: flex-start; gap: 10px;
    padding: .6rem 0; border-bottom: var(--border);
  }
  .cert-row:last-child { border-bottom: none; }
  .cert-icon {
    width: 30px; height: 30px; border-radius: 8px; flex-shrink: 0;
    background: var(--accent-light); display: flex; align-items: center; justify-content: center;
  }
  .cert-icon svg { color: var(--accent-dark); }
  .cert-name { font-size: 13px; color: var(--text); }
  .cert-org { font-size: 11px; color: var(--muted); margin-top: 2px; }

  /* ── IEEE badge ──────────────────────────── */
  .ieee-badge {
    display: inline-flex; align-items: center; gap: 10px;
    padding: .7rem 1.1rem;
    background: var(--accent-light); border: 1px solid var(--accent-border);
    border-radius: var(--r); font-size: 13px; font-weight: 500; color: var(--accent-dark);
  }

  /* ── SVG icons (inline, no font dep) ─────── */
  svg.ico { width: 15px; height: 15px; stroke: currentColor; fill: none;
            stroke-width: 1.75; stroke-linecap: round; stroke-linejoin: round; }

  @media (max-width: 520px) {
    .skill-grid { grid-template-columns: 1fr; }
    .stat-row { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<!-- ─── Hero ─────────────────────────────────────── -->
<div class="hero">
  <div class="avatar">RV</div>
  <h1>Ramprasath V</h1>
  <p class="sub">
    Electronics &amp; Communication Engineering &nbsp;·&nbsp; Batch 2027 &nbsp;·&nbsp; KPRIET, Coimbatore<br>
    Embedded Systems &nbsp;·&nbsp; IoT &nbsp;·&nbsp; VLSI &nbsp;·&nbsp; Machine Learning
  </p>
  <div class="tag-row">
    <span class="tag green">CGPA 8.46</span>
    <span class="tag">Industry 4.0</span>
    <span class="tag">IEEE CAS PRO</span>
    <span class="tag">250+ LeetCode</span>
    <span class="tag">Open to opportunities</span>
  </div>
  <div class="links">
    <a class="link-btn" href="mailto:veluramprasath777@gmail.com">
      <svg class="ico" viewBox="0 0 24 24"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m2 7 10 7 10-7"/></svg>
      veluramprasath777@gmail.com
    </a>
    <a class="link-btn" href="https://linkedin.com/in/ramprasath-v">
      <svg class="ico" viewBox="0 0 24 24"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
      LinkedIn
    </a>
    <a class="link-btn" href="https://github.com/ramprasathvelu">
      <svg class="ico" viewBox="0 0 24 24"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
      GitHub
    </a>
  </div>
</div>

<!-- ─── About ──────────────────────────────────────── -->
<div class="section">
  <div class="sec-title">About</div>
  <p class="about-box">
Final-year Electronics and Communication Engineering student with strong skills in embedded systems, industrial IoT,
and AI-based real-time systems. Experienced in sensor integration, microcontrollers, MQTT communication, and
computer vision for automation and anomaly detection. Focused on building efficient, intelligent solutions for real-world
industrial challenges. Aiming to contribute to smarter, sustainable systems aligned with Industry 4.0.
  </p>
</div>

<!-- ─── Stats ──────────────────────────────────────── -->
<div class="section">
  <div class="sec-title">At a glance</div>
  <div class="stat-row">
    <div class="stat"><div class="num">8.46</div><div class="lbl">CGPA</div></div>
    <div class="stat"><div class="num">250+</div><div class="lbl">LeetCode problems</div></div>
    <div class="stat"><div class="num">3</div><div class="lbl">Internships</div></div>
  </div>
</div>

<!-- ─── Skills ────────────────────────────────────── -->
<div class="section">
  <div class="sec-title">Skills</div>
  <div class="skill-grid">

    <div class="skill-card">
      <h3>
        <svg class="ico" viewBox="0 0 24 24"><rect x="4" y="4" width="16" height="16" rx="2"/><rect x="9" y="9" width="6" height="6"/><line x1="9" y1="2" x2="9" y2="4"/><line x1="15" y1="2" x2="15" y2="4"/><line x1="9" y1="20" x2="9" y2="22"/><line x1="15" y1="20" x2="15" y2="22"/><line x1="2" y1="9" x2="4" y2="9"/><line x1="2" y1="15" x2="4" y2="15"/><line x1="20" y1="9" x2="22" y2="9"/><line x1="20" y1="15" x2="22" y2="15"/></svg>
        Hardware &amp; embedded
      </h3>
      <div class="pill-row">
        <span class="pill hl">ESP32</span>
        <span class="pill hl">Arduino</span>
        <span class="pill hl">BRD2605A (SiWx917)</span>
        <span class="pill">UART / SPI / I2C</span>
        <span class="pill">GPIO &amp; Relay</span>
        <span class="pill">PCB Design</span>
        <span class="pill">Sensor Integration</span>
        <span class="pill">MicroPython</span>
      </div>
    </div>

    <div class="skill-card">
      <h3>
        <svg class="ico" viewBox="0 0 24 24"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>
        VLSI &amp; digital design
      </h3>
      <div class="pill-row">
        <span class="pill hl">Verilog HDL</span>
        <span class="pill hl">RTL Design</span>
        <span class="pill">Icarus Verilog</span>
        <span class="pill">YOSYS</span>
        <span class="pill">Magic VLSI</span>
        <span class="pill">OpenSTA</span>
        <span class="pill">CMOS Fundamentals</span>
        <span class="pill">CTS / Floorplan</span>
      </div>
    </div>

    <div class="skill-card">
      <h3>
        <svg class="ico" viewBox="0 0 24 24"><path d="M9.5 2A2.5 2.5 0 0 1 12 4.5v15a2.5 2.5 0 0 1-4.96.44 2.5 2.5 0 0 1-2.96-3.08 3 3 0 0 1-.34-5.58 2.5 2.5 0 0 1 1.32-4.84A2.5 2.5 0 0 1 9.5 2"/><path d="M14.5 2A2.5 2.5 0 0 0 12 4.5v15a2.5 2.5 0 0 0 4.96.44 2.5 2.5 0 0 0 2.96-3.08 3 3 0 0 0 .34-5.58 2.5 2.5 0 0 0-1.32-4.84A2.5 2.5 0 0 0 14.5 2"/></svg>
        ML &amp; data science
      </h3>
      <div class="pill-row">
        <span class="pill hl">Python</span>
        <span class="pill hl">YOLOv8</span>
        <span class="pill hl">Scikit-learn</span>
        <span class="pill">XGBoost</span>
        <span class="pill">OpenCV</span>
        <span class="pill">MediaPipe</span>
        <span class="pill">Pandas / NumPy</span>
        <span class="pill">Matplotlib</span>
      </div>
    </div>

    <div class="skill-card">
      <h3>
        <svg class="ico" viewBox="0 0 24 24"><path d="M4 3h16a2 2 0 0 1 2 2v6a10 10 0 0 1-10 9A10 10 0 0 1 2 11V5a2 2 0 0 1 2-2z"/></svg>
        Software &amp; cloud
      </h3>
      <div class="pill-row">
        <span class="pill hl">AWS EC2 / S3</span>
        <span class="pill hl">Java</span>
        <span class="pill hl">C</span>
        <span class="pill">MQTT / EMQX</span>
        <span class="pill">MySQL / MongoDB</span>
        <span class="pill">Git / GitHub</span>
        <span class="pill">Linux</span>
        <span class="pill">HTML / CSS / JS</span>
      </div>
    </div>

  </div>
</div>

<!-- ─── Projects ──────────────────────────────────── -->
<div class="section">
  <div class="sec-title">Projects</div>
  <div class="proj-list">

    <div class="proj-card">
      <div class="proj-header">
        <div class="proj-title">🔍 AnomalyDetection — Vision-based restricted area security</div>
        <a class="proj-link" href="https://github.com/ramprasathvelu/AnomalyDetection">↗ repo</a>
      </div>
      <p class="proj-desc">
        Real-time safety monitoring using YOLOv8 + MediaPipe pose estimation. Reduced intrusion response time by ~70% via
        dual-channel alerting (Twilio SMS + SMTP). NLP-based log verification cuts false positives by ~35%.
        Presented at an international conference; IEEE paper in progress.
      </p>
      <div class="badge-row">
        <span class="badge">YOLOv8</span><span class="badge">MediaPipe</span><span class="badge">OpenCV</span>
        <span class="badge">NLP</span><span class="badge">Twilio</span><span class="badge">AWS EC2</span>
        <span class="badge">Conference paper</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-header">
        <div class="proj-title">🗺️ BLU-PATH — Embedded web-based indoor navigation</div>
        <a class="proj-link" href="https://github.com/ramprasathvelu/BLU-PATH-Embedded-Web-Based-Indoor-Navigation-System">↗ repo</a>
      </div>
      <p class="proj-desc">
        BRD2605A (SiWx917) acts as a standalone Wi-Fi access point and embedded web server. Visitors scan a QR code,
        connect, and get interactive campus navigation instantly — zero internet, zero app install.
        Scalable to hospitals, corporates, and industrial campuses.
      </p>
      <div class="badge-row">
        <span class="badge">Silicon Labs BRD2605A</span><span class="badge">C</span>
        <span class="badge">WiseConnect SDK</span><span class="badge">Simplicity Studio</span>
        <span class="badge">HTML / CSS / JS</span><span class="badge">Embedded HTTP</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-header">
        <div class="proj-title">🌾 CropGuard — Crop disease severity classifier</div>
        <a class="proj-link" href="https://github.com/ramprasathvelu/CropGuard">↗ repo</a>
      </div>
      <p class="proj-desc">
        Ensemble ML model (Random Forest + XGBoost) for multi-class crop disease severity prediction.
        Deployed on AWS EC2 with a Streamlit interface accessible via public URL. SDG-2 aligned — precision agriculture
        for smallholder farmers.
      </p>
      <div class="badge-row">
        <span class="badge">Random Forest</span><span class="badge">XGBoost</span>
        <span class="badge">Scikit-learn</span><span class="badge">Streamlit</span>
        <span class="badge">AWS EC2</span><span class="badge">SDG 2</span>
      </div>
    </div>

    <div class="proj-card">
      <div class="proj-header">
        <div class="proj-title">🎙️ AI Voice Thinker — Offline voice home automation</div>
        <a class="proj-link" href="https://github.com/ramprasathvelu/AI-Voice-Thinker">↗ repo</a>
      </div>
      <p class="proj-desc">
        Cloud-independent embedded voice automation using AI-Thinker VC-02 (US516P6) + ESP32 over UART.
        Wake-word detection controls appliances via relay modules. Sub-100ms latency, 98%+ recognition accuracy.
      </p>
      <div class="badge-row">
        <span class="badge">AI-Thinker VC-02</span><span class="badge">ESP32</span>
        <span class="badge">UART</span><span class="badge">C</span><span class="badge">Arduino IDE</span>
      </div>
    </div>

  </div>
</div>

<!-- ─── Internships ───────────────────────────────── -->
<div class="section">
  <div class="sec-title">Internships</div>
  <table class="data-table">
    <thead>
      <tr><th>Role</th><th>Organization</th><th>Period</th></tr>
    </thead>
    <tbody>
      <tr>
        <td>VLSI Design Intern</td>
        <td>NIELIT (Remote)</td>
        <td>Dec 2025 – Feb 2026</td>
      </tr>
      <tr>
        <td>Telecom Training Intern</td>
        <td>BSNL, Kallakurichi</td>
        <td>Jun 2025 – Jul 2025</td>
      </tr>
      <tr>
        <td>Industrial Trainee — IoT &amp; PCB</td>
        <td>KPRIET, Coimbatore</td>
        <td>Nov 2025 – Dec 2025</td>
      </tr>
    </tbody>
  </table>
</div>

<!-- ─── Education ─────────────────────────────────── -->
<div class="section">
  <div class="sec-title">Education</div>
  <table class="data-table">
    <thead>
      <tr><th>Degree</th><th>Institution</th><th>Year</th><th>Score</th></tr>
    </thead>
    <tbody>
      <tr>
        <td>B.E. Electronics &amp; Communication</td>
        <td>KPRIET, Coimbatore</td>
        <td>2023 – 2027</td>
        <td>CGPA 8.46</td>
      </tr>
      <tr>
        <td>HSC</td>
        <td>Bharathi Matric Hr. Sec. School, Kallakurichi</td>
        <td>2023</td>
        <td>88.89%</td>
      </tr>
    </tbody>
  </table>
</div>

<!-- ─── Certifications ────────────────────────────── -->
<div class="section">
  <div class="sec-title">Certifications</div>
  <div>
    <div class="cert-row">
      <div class="cert-icon">
        <svg class="ico" viewBox="0 0 24 24" style="color:#085041"><path d="M22 10v6M2 10l10-5 10 5-10 5z"/><path d="M6 12v5c3 3 9 3 12 0v-5"/></svg>
      </div>
      <div>
        <div class="cert-name">Supervised Machine Learning: Regression and Classification</div>
        <div class="cert-org">DeepLearning.AI / Stanford Online · Coursera</div>
      </div>
    </div>
    <div class="cert-row">
      <div class="cert-icon">
        <svg class="ico" viewBox="0 0 24 24" style="color:#085041"><rect x="2" y="3" width="20" height="14" rx="2"/><path d="M8 21h8M12 17v4"/></svg>
      </div>
      <div>
        <div class="cert-name">Data Science Fundamentals · NLP · Artificial Intelligence</div>
        <div class="cert-org">Infosys Springboard — Virtual Internship 7.0</div>
      </div>
    </div>
    <div class="cert-row">
      <div class="cert-icon">
        <svg class="ico" viewBox="0 0 24 24" style="color:#085041"><circle cx="12" cy="12" r="10"/><path d="M12 8v4l3 3"/></svg>
      </div>
      <div>
        <div class="cert-name">Introduction to Industry 4.0 &amp; IIoT · Microelectronics · Microsensors</div>
        <div class="cert-org">NPTEL</div>
      </div>
    </div>
    <div class="cert-row">
      <div class="cert-icon">
        <svg class="ico" viewBox="0 0 24 24" style="color:#085041"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
      </div>
      <div>
        <div class="cert-name">Problem Solving · Java</div>
        <div class="cert-org">HackerRank &nbsp;|&nbsp; LeetCode — 250+ problems solved</div>
      </div>
    </div>
  </div>
</div>

<!-- ─── Activity ──────────────────────────────────── -->
<div class="section">
  <div class="sec-title">Activity</div>
  <div class="ieee-badge">
    <svg class="ico" viewBox="0 0 24 24" style="width:18px;height:18px"><path d="M5 12.55a11 11 0 0 1 14.08 0"/><path d="M1.42 9a16 16 0 0 1 21.16 0"/><path d="M8.53 16.11a6 6 0 0 1 6.95 0"/><circle cx="12" cy="20" r="1"/></svg>
    Public Relations Officer — IEEE Circuits and Systems Society (CAS), KPRIET
  </div>
</div>

</body>
</html>
