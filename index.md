---
layout: default
title: HERMES
description: Real-Time Traffic Hazard Reasoning on Edge Devices
---

<style>
:root {
  --bg: #05080d;
  --bg-soft: #0b111a;
  --card: rgba(255, 255, 255, 0.065);
  --card-strong: rgba(255, 255, 255, 0.105);
  --glass: rgba(255, 255, 255, 0.075);
  --text: #eef7f8;
  --muted: #9db0b8;
  --muted-2: #73848c;
  --accent: #00f0b5;
  --accent-2: #54a7ff;
  --accent-3: #b26cff;
  --warning: #ffcc66;
  --danger: #ff5f72;
  --border: rgba(255, 255, 255, 0.13);
  --shadow: 0 24px 80px rgba(0, 0, 0, 0.42);
}

body {
  background:
    radial-gradient(circle at 10% 0%, rgba(0, 240, 181, 0.18), transparent 32%),
    radial-gradient(circle at 90% 5%, rgba(84, 167, 255, 0.18), transparent 34%),
    radial-gradient(circle at 50% 95%, rgba(178, 108, 255, 0.10), transparent 30%),
    var(--bg);
  color: var(--text);
}

.main-content {
  max-width: 900px;
  padding-left: 24px;
  padding-right: 24px;
}

.main-content h1,
.main-content h2,
.main-content h3,
.main-content h4 {
  color: var(--text);
}

.main-content p,
.main-content li,
.main-content td {
  color: var(--muted);
}

.main-content strong {
  color: var(--text);
}

.main-content a {
  color: var(--accent-2);
}

.page-header {
  display: none;
}

.hero {
  position: relative;
  padding: 68px 38px 38px 38px;
  margin-top: 24px;
  border: 1px solid var(--border);
  border-radius: 34px;
  background:
    linear-gradient(145deg, rgba(255, 255, 255, 0.095), rgba(255, 255, 255, 0.035)),
    rgba(255, 255, 255, 0.045);
  box-shadow: var(--shadow);
  overflow: hidden;
}

.hero::before {
  content: "";
  position: absolute;
  inset: -1px;
  background:
    linear-gradient(120deg, rgba(0, 240, 181, 0.25), transparent 25%),
    linear-gradient(260deg, rgba(84, 167, 255, 0.20), transparent 32%);
  pointer-events: none;
}

.hero-inner {
  position: relative;
  z-index: 2;
}

.kicker {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 8px 13px;
  border-radius: 999px;
  background: rgba(0, 240, 181, 0.10);
  border: 1px solid rgba(0, 240, 181, 0.30);
  color: #bfffee;
  font-weight: 800;
  font-size: 0.84rem;
  letter-spacing: 0.3px;
  text-transform: uppercase;
}

.hero-title {
  max-width: 900px;
  margin: 22px 0 0 0;
  font-size: clamp(2.5rem, 7vw, 5.4rem);
  line-height: 0.95;
  letter-spacing: -3px;
  color: var(--text);
}

.hero-title span {
  background: linear-gradient(90deg, var(--accent), var(--accent-2));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-subtitle {
  max-width: 870px;
  margin-top: 22px;
  font-size: 1.28rem;
  line-height: 1.65;
  color: #c8d8dd;
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  margin-top: 30px;
}

.btn {
  display: inline-block;
  padding: 13px 18px;
  border-radius: 14px;
  font-weight: 850;
  text-decoration: none;
  border: 1px solid var(--border);
}

.btn-primary {
  color: #04110d !important;
  background: linear-gradient(90deg, var(--accent), #7af7ff);
  border-color: transparent;
}

.btn-secondary {
  color: var(--text) !important;
  background: rgba(255, 255, 255, 0.075);
}

.badges {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 28px;
}

.badge {
  padding: 8px 13px;
  border: 1px solid var(--border);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.075);
  color: var(--text);
  font-size: 0.88rem;
  font-weight: 800;
}

.hero-image {
  position: relative;
  z-index: 2;
  margin-top: 38px;
  border-radius: 26px;
  overflow: hidden;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  background: #000;
}

.hero-image img {
  width: 100%;
  display: block;
}

.metrics-strip {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
  margin: 28px 0 36px 0;
}

.metric {
  padding: 20px;
  border-radius: 22px;
  background: var(--glass);
  border: 1px solid var(--border);
  box-shadow: 0 14px 44px rgba(0, 0, 0, 0.20);
}

.metric-value {
  color: var(--text);
  font-size: 1.45rem;
  font-weight: 950;
}

.metric-label {
  margin-top: 5px;
  color: var(--muted);
  font-size: 0.92rem;
}

.section-card {
  padding: 34px;
  margin: 36px 0;
  border: 1px solid var(--border);
  border-radius: 28px;
  background:
    linear-gradient(180deg, rgba(255, 255, 255, 0.075), rgba(255, 255, 255, 0.045));
  box-shadow: 0 18px 54px rgba(0, 0, 0, 0.22);
}

.section-label {
  color: var(--accent);
  font-weight: 900;
  font-size: 0.82rem;
  letter-spacing: 0.8px;
  text-transform: uppercase;
  margin-bottom: 8px;
}

.section-card h2,
.section-card h3 {
  margin-top: 0;
  font-size: 2.15rem;
  letter-spacing: -0.9px;
}

.section-card > p {
  font-size: 1.02rem;
  line-height: 1.75;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
  margin-top: 24px;
}

.feature {
  position: relative;
  padding: 17px 18px 17px 46px;
  border-radius: 18px;
  background: var(--card-strong);
  border: 1px solid var(--border);
  color: var(--text);
  font-weight: 800;
}

.feature::before {
  content: "◆";
  position: absolute;
  left: 18px;
  top: 17px;
  color: var(--accent);
  font-size: 0.85rem;
}

.demo-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 22px;
  margin-top: 26px;
}

.demo-card {
  border: 1px solid var(--border);
  border-radius: 24px;
  background: var(--card);
  overflow: hidden;
  box-shadow: 0 14px 38px rgba(0, 0, 0, 0.22);
  transition: transform 0.18s ease, border-color 0.18s ease;
}

.demo-card:hover {
  transform: translateY(-3px);
  border-color: rgba(0, 240, 181, 0.42);
}

.demo-card img {
  width: 100%;
  display: block;
}

.demo-body {
  padding: 18px 18px 20px 18px;
}

.demo-title {
  color: var(--text);
  font-size: 1.05rem;
  font-weight: 900;
  margin-bottom: 6px;
}

.demo-desc {
  color: var(--muted);
  font-size: 0.95rem;
  line-height: 1.55;
}

.note {
  padding: 14px 18px;
  border-left: 4px solid var(--warning);
  border-radius: 14px;
  background: rgba(255, 204, 102, 0.10);
  color: #f6dfaa;
  margin-top: 18px;
}

.image-card {
  border-radius: 26px;
  overflow: hidden;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  margin-top: 24px;
  background: #000;
}

.image-card img {
  width: 100%;
  display: block;
}

.clean-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0 10px;
  margin-top: 24px;
}

.clean-table th {
  color: var(--text);
  text-align: left;
  padding: 12px 14px;
  font-size: 0.92rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.clean-table td {
  padding: 15px 14px;
  background: var(--card-strong);
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
}

.clean-table td:first-child {
  border-left: 1px solid var(--border);
  border-radius: 15px 0 0 15px;
  color: var(--text);
  font-weight: 900;
}

.clean-table td:last-child {
  border-right: 1px solid var(--border);
  border-radius: 0 15px 15px 0;
}

.method-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 18px;
  margin-top: 24px;
}

.method-card {
  padding: 22px;
  color: var(--text);
  border-radius: 22px;
  border: 1px solid var(--border);
  background: var(--card-strong);
}

.method-card h4 {
  margin-top: 0;
  margin-bottom: 10px;
  font-size: 1.12rem;
}

.method-card p {
  color: var(--muted);
  line-height: 1.65;
}

.status-list li {
  margin-bottom: 8px;
}

.contact-card {
  text-align: center;
  padding: 38px;
  border-radius: 28px;
  background:
    linear-gradient(135deg, rgba(0, 240, 181, 0.12), rgba(84, 167, 255, 0.12));
  border: 1px solid var(--border);
  margin: 36px 0 10px 0;
  box-shadow: var(--shadow);
}

.contact-card h3 {
  margin-top: 0;
}

@media (max-width: 860px) {
  .hero {
    padding: 46px 24px 28px 24px;
  }

  .hero-title {
    letter-spacing: -1.7px;
  }

  .metrics-strip,
  .feature-grid,
  .demo-grid,
  .method-grid {
    grid-template-columns: 1fr;
  }

  .section-card {
    padding: 24px;
  }
}
</style>

<div class="hero">
  <div class="hero-inner">

    <div class="kicker">Real-Time Edge AI for Road Safety</div>

    <h1 class="hero-title">
      HERMES<br>
      <span>Traffic Hazard Reasoning</span>
    </h1>

    <p class="hero-subtitle">
      HERMES is a research-to-production system for real-time, causal traffic hazard anticipation using a CUDA/CoreML-optimized RWKV video model on iPhone and NVIDIA Jetson edge devices.
    </p>

    <p class="hero-subtitle">
      During driving, HERMES performs <strong>real-time online inference</strong> directly from the live camera stream, enabling risk estimation and visual hazard localization without offline processing or noticeable delay.
    </p>

    <div class="hero-actions">
      <a class="btn btn-primary" href="#demo-gallery">View Real-World Demos</a>
      <a class="btn btn-secondary" href="#system-pipeline">See System Pipeline</a>
    </div>

    <div class="badges">
      <span class="badge">iOS / CoreML</span>
      <span class="badge">NVIDIA Jetson Orin Nano</span>
      <span class="badge">CUDA / TensorRT</span>
      <span class="badge">RWKV Video Model</span>
      <span class="badge">Real-Time Edge AI</span>
    </div>

  </div>

  <div class="hero-image">
    <img src="assets/Hermes_app.png" alt="HERMES iOS safety interface">
  </div>
</div>

<div class="metrics-strip">
  <div class="metric">
    <div class="metric-value">Real-time</div>
    <div class="metric-label">Live camera inference</div>
  </div>
  <div class="metric">
    <div class="metric-value">Causal</div>
    <div class="metric-label">No future frames used</div>
  </div>
  <div class="metric">
    <div class="metric-value">31M</div>
    <div class="metric-label">Edge-oriented parameters</div>
  </div>
  <div class="metric">
    <div class="metric-value">iOS + Jetson</div>
    <div class="metric-label">CoreML / TensorRT deployment</div>
  </div>
</div>

<div class="section-card">

<div class="section-label">Deployment</div>
<h3>Real-World iOS Safety Dashboard</h3>

<p>
HERMES was integrated into a real-time iOS prototype for motorcycle-mounted traffic hazard anticipation.
The app processes a live camera stream directly on device and visualizes predicted traffic risk through a lightweight safety dashboard.
</p>

<div class="feature-grid">
  <div class="feature">Real-time causal frame-by-frame inference</div>
  <div class="feature">Live traffic risk estimation</div>
  <div class="feature">SAFE / WARNING / DANGER state prediction</div>
  <div class="feature">Frame-level hazard probability</div>
  <div class="feature">Current riding speed</div>
  <div class="feature">Visual hazard localization cues</div>
  <div class="feature">Sound and vibration warning options</div>
  <div class="feature">Runtime controls for camera, resolution, inference frequency, focus, and exposure</div>
</div>

<p>
The system was tested in real-world urban riding scenarios, including rainy roads, nighttime traffic, dense scooter flows, intersections, and mixed vehicle environments.
</p>

</div>

<div class="section-card" id="demo-gallery">

<div class="section-label">Real-World Riding Footage</div>
<h3>Demo Gallery</h3>

<p>
The following demos show HERMES running in real time on iPhone during motorcycle-mounted riding in real-world urban traffic in Taipei City.
</p>

<div class="note">
GIFs may take several seconds to load depending on network speed.
</div>

<div class="demo-grid">

<div class="demo-card">
  <img src="assets/demo_1.gif" alt="Demo 1">
  <div class="demo-body">
    <div class="demo-title">Demo 1 — Dense Urban Warning</div>
    <div class="demo-desc">Real-time WARNING prediction in dense scooter traffic.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_2.gif" alt="Demo 2">
  <div class="demo-body">
    <div class="demo-title">Demo 2 — Nighttime Following</div>
    <div class="demo-desc">Stable SAFE prediction during low-light riding.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_3.gif" alt="Demo 3">
  <div class="demo-body">
    <div class="demo-title">Demo 3 — Nighttime Intersection Zone</div>
    <div class="demo-desc">Risk estimation near complex intersection markings.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_4.gif" alt="Demo 4">
  <div class="demo-body">
    <div class="demo-title">Demo 4 — Multi-Lane Night Traffic</div>
    <div class="demo-desc">Online inference during normal nighttime traffic.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_5.gif" alt="Demo 5">
  <div class="demo-body">
    <div class="demo-title">Demo 5 — Rainy Scooter Traffic</div>
    <div class="demo-desc">Robust prediction under wet-road reflections.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_6.gif" alt="Demo 6">
  <div class="demo-body">
    <div class="demo-title">Demo 6 — Rainy Urban Corridor</div>
    <div class="demo-desc">Real-world rainy traffic with storefront clutter.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_7.gif" alt="Demo 7">
  <div class="demo-body">
    <div class="demo-title">Demo 7 — Close-Range Scooter Interaction</div>
    <div class="demo-desc">Localization of nearby traffic participants.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_8.gif" alt="Demo 8">
  <div class="demo-body">
    <div class="demo-title">Demo 8 — Rainy Intersection Approach</div>
    <div class="demo-desc">Risk estimation while approaching an intersection.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_9.gif" alt="Demo 9">
  <div class="demo-body">
    <div class="demo-title">Demo 9 — Crowded Scooter Queue</div>
    <div class="demo-desc">Stable prediction in dense slow-moving traffic.</div>
  </div>
</div>

<div class="demo-card">
  <img src="assets/demo_10.gif" alt="Demo 10">
  <div class="demo-body">
    <div class="demo-title">Demo 10 — Higher-Speed Urban Road</div>
    <div class="demo-desc">Safety monitoring with surrounding vehicles at speed.</div>
  </div>
</div>

</div>
</div>

<div class="section-card">

<div class="section-label">Application Interface</div>
<h3>iOS App Interface</h3>

<div class="image-card">
  <img src="assets/Hermes_app.png" alt="Annotated HERMES iOS interface">
</div>

<p>
The HERMES iOS interface is designed for real-time riding feedback while keeping the road view unobstructed.
</p>

<table class="clean-table">
  <tr>
    <th>Component</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>Safety Status Panel</td>
    <td>Shows the current prediction state, real-time hazard probability, and riding speed.</td>
  </tr>
  <tr>
    <td>Live Camera Inference</td>
    <td>Processes the iPhone camera stream directly on device using real-time causal frame-by-frame inference.</td>
  </tr>
  <tr>
    <td>Hazard Localization Cues</td>
    <td>Visualizes image regions that contribute to the predicted traffic risk.</td>
  </tr>
  <tr>
    <td>Runtime Control Panel</td>
    <td>Controls camera lens, resolution, inference frequency, warning alerts, focus, and exposure.</td>
  </tr>
  <tr>
    <td>Compact Peripheral Indicator</td>
    <td>Provides quick visual safety feedback without covering the central road view.</td>
  </tr>
  <tr>
    <td>Adaptive Inference Settings</td>
    <td>Allows balancing responsiveness, accuracy, thermal behavior, and battery consumption.</td>
  </tr>
  <tr>
    <td>Settings Toggle</td>
    <td>Opens the overlay control panel while keeping the live camera feed visible.</td>
  </tr>
</table>

</div>

<div class="section-card" id="system-pipeline">

<div class="section-label">System Design</div>
<h3>System Pipeline</h3>

<div class="image-card">
  <img src="assets/diagram.png" alt="HERMES iOS safety diagram">
</div>

</div>

<div class="section-card">

<div class="section-label">Key Capabilities</div>
<h3>Highlights</h3>

<div class="feature-grid">
  <div class="feature">Real-time online inference under strict causal constraints</div>
  <div class="feature">No future frames used during inference</div>
  <div class="feature">CoreML-optimized deployment on iPhone</div>
  <div class="feature">CUDA/TensorRT deployment on NVIDIA Jetson Orin Nano</div>
  <div class="feature">Motorcycle-mounted real-world testing</div>
  <div class="feature">RWKV-based temporal modeling with linear complexity</div>
  <div class="feature">Multi-task prediction of traffic anomaly occurrence, localization, and category</div>
  <div class="feature">Edge-oriented model design with 31M parameters</div>
</div>

</div>

<div class="section-card">

<div class="section-label">Research Method</div>
<h3>Method Overview</h3>

<p>
HERMES uses a <b>Hierarchical Spatio-Temporal RWKV</b> backbone for efficient causal video understanding.
</p>

<div class="method-grid">

<div class="method-card">
<h4>HST-RWKV Backbone</h4>
<p>
The backbone combines hierarchical spatial encoding with recurrent temporal modeling, enabling online video understanding without requiring access to the full video sequence.
</p>
</div>

<div class="method-card">
<h4>Multi-rate Event Sensing</h4>
<p>
Stride-controlled recurrent updates capture both fast motion cues and longer-range temporal context within a single recurrent architecture.
</p>
</div>

<div class="method-card">
<h4>Causal Future Distillation</h4>
<p>
Causal Future Distillation transfers future-aware representation targets during training while preserving strictly causal inference at test time.
</p>
</div>

<div class="method-card">
<h4>Unified Multi-task Objective</h4>
<p>
HERMES jointly predicts traffic anomaly occurrence, hazard localization, and anomaly category from the same causal video representation.
</p>
</div>

</div>
</div>

<div class="section-card">

<div class="section-label">Edge Runtime</div>
<h3>Deployment</h3>

<table class="clean-table">
  <tr>
    <th>Platform</th>
    <th>Runtime</th>
    <th>Status</th>
  </tr>
  <tr>
    <td>iPhone</td>
    <td>CoreML</td>
    <td>Real-time prototype implemented</td>
  </tr>
  <tr>
    <td>NVIDIA Jetson Orin Nano</td>
    <td>CUDA / TensorRT</td>
    <td>Edge deployment tested</td>
  </tr>
</table>

</div>

<div class="section-card">

<div class="section-label">Project Status</div>
<h3>Status</h3>

<ul class="status-list">
  <li>iOS prototype implemented</li>
  <li>CoreML model deployed on iPhone</li>
  <li>Real-time motorcycle-mounted testing completed</li>
  <li>NVIDIA Jetson Orin Nano deployment tested</li>
  <li>Demo videos collected from real-world riding footage</li>
  <li>Paper currently under review</li>
</ul>

</div>

<div class="contact-card">

<h3>Contact</h3>

<p><b>Patrik Patera, Ph.D.</b></p>
<p><i>Computer Vision & Deep Learning Research Engineer</i></p>
<p>Taiwan</p>
<p>pat.patera@gmail.com</p>

</div>