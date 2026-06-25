---
layout: default
title: HERMES
description: Real-Time Traffic Hazard Reasoning on Edge Devices (iOS / NVidia Jetson)
---

<style>
:root {
  --bg: #0b1117;
  --card: rgba(255, 255, 255, 0.065);
  --card-strong: rgba(255, 255, 255, 0.105);
  --text: #e8f0f2;
  --muted: #9fb1b7;
  --accent: #00e0a4;
  --accent-2: #4da3ff;
  --warning: #ffcc66;
  --danger: #ff6b6b;
  --border: rgba(255, 255, 255, 0.13);
  --shadow: 0 20px 60px rgba(0, 0, 0, 0.35);
}

body {
  background: radial-gradient(circle at top left, #103b3a 0, transparent 32%),
              radial-gradient(circle at top right, #172f5f 0, transparent 30%),
              var(--bg);
}

.main-content {
  max-width: 1180px;
}

.main-content h1,
.main-content h2,
.main-content h3 {
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

.hero {
  padding: 56px 34px 36px 34px;
  margin-top: 20px;
  border: 1px solid var(--border);
  border-radius: 28px;
  background:
    linear-gradient(135deg, rgba(0, 224, 164, 0.12), rgba(77, 163, 255, 0.10)),
    rgba(255, 255, 255, 0.045);
  box-shadow: var(--shadow);
  overflow: hidden;
}

.hero-title {
  font-size: 3.1rem;
  line-height: 1.05;
  margin: 0;
  color: var(--text);
  letter-spacing: -1.5px;
}

.hero-subtitle {
  font-size: 1.35rem;
  margin-top: 16px;
  color: #d9f7f0;
  font-weight: 600;
}

.hero-text {
  font-size: 1.05rem;
  margin-top: 20px;
  color: var(--muted);
}

.badges {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 26px;
}

.badge {
  padding: 8px 13px;
  border: 1px solid var(--border);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.08);
  color: var(--text);
  font-size: 0.88rem;
  font-weight: 700;
}

.hero-image {
  margin-top: 34px;
  border-radius: 22px;
  overflow: hidden;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
}

.hero-image img {
  width: 100%;
  display: block;
}

.section-card {
  padding: 30px;
  margin: 36px 0;
  border: 1px solid var(--border);
  border-radius: 24px;
  background: var(--card);
  box-shadow: 0 12px 38px rgba(0, 0, 0, 0.18);
}

.section-card h2 {
  margin-top: 0;
  font-size: 2rem;
  letter-spacing: -0.5px;
}

.feature-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
  margin-top: 22px;
}

.feature {
  padding: 16px 18px;
  border-radius: 18px;
  background: var(--card-strong);
  border: 1px solid var(--border);
  color: var(--text);
  font-weight: 700;
}

.demo-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 22px;
  margin-top: 26px;
}

.demo-card {
  border: 1px solid var(--border);
  border-radius: 22px;
  background: var(--card);
  overflow: hidden;
  box-shadow: 0 12px 34px rgba(0, 0, 0, 0.18);
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
  font-weight: 800;
  margin-bottom: 6px;
}

.demo-desc {
  color: var(--muted);
  font-size: 0.95rem;
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
  border-radius: 24px;
  overflow: hidden;
  border: 1px solid var(--border);
  box-shadow: var(--shadow);
  margin-top: 22px;
}

.image-card img {
  width: 100%;
  display: block;
}

.clean-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0 10px;
  margin-top: 20px;
}

.clean-table th {
  color: var(--text);
  text-align: left;
  padding: 12px 14px;
}

.clean-table td {
  padding: 14px;
  background: var(--card-strong);
  border-top: 1px solid var(--border);
  border-bottom: 1px solid var(--border);
}

.clean-table td:first-child {
  border-left: 1px solid var(--border);
  border-radius: 14px 0 0 14px;
  color: var(--text);
  font-weight: 800;
}

.clean-table td:last-child {
  border-right: 1px solid var(--border);
  border-radius: 0 14px 14px 0;
}

.method-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 18px;
  margin-top: 24px;
}

.method-card {
  padding: 20px;
  border-radius: 20px;
  border: 1px solid var(--border);
  background: var(--card-strong);
}

.method-card h3 {
  margin-top: 0;
  margin-bottom: 10px;
}

.status-list li {
  margin-bottom: 7px;
}

.contact-card {
  text-align: center;
  padding: 34px;
  border-radius: 24px;
  background: linear-gradient(135deg, rgba(0, 224, 164, 0.11), rgba(77, 163, 255, 0.10));
  border: 1px solid var(--border);
  margin-top: 36px;
}

@media (max-width: 760px) {
  .hero-title {
    font-size: 2.2rem;
  }

  .feature-grid,
  .demo-grid,
  .method-grid {
    grid-template-columns: 1fr;
  }

  .section-card {
    padding: 22px;
  }
}
</style>

<div class="hero">

<h1 class="hero-title">HERMES</h1>

<div class="hero-subtitle">
Real-Time Traffic Hazard Reasoning on Edge Devices
</div>

<div class="badges">
  <span class="badge">iOS / CoreML</span>
  <span class="badge">NVIDIA Jetson Orin Nano</span>
  <span class="badge">CUDA / TensorRT</span>
  <span class="badge">RWKV Video Model</span>
  <span class="badge">Real-Time Edge AI</span>
</div>

<p class="hero-text">
<strong>HERMES: Hierarchical Efficient RWKV with Multi-rate Event Sensing</strong>
</p>

<p class="hero-text">
HERMES is a research-to-production project for real-time, causal traffic hazard anticipation using a CUDA/CoreML-optimized RWKV video model.
</p>

<p class="hero-text">
The system performs frame-by-frame online inference directly from video streams and predicts traffic risk without using future frames. HERMES is deployed on <strong>iPhone via CoreML</strong> and on <strong>NVIDIA Jetson Orin Nano via CUDA/TensorRT</strong>, and validated in real-world motorcycle riding scenarios.
</p>

<div class="hero-image">
  <img src="assets/Hermes_app.png" alt="HERMES iOS safety interface">
</div>

</div>

<div class="section-card">

<h3> Real-World iOS Deployment </h3>

HERMES was integrated into a real-time iOS prototype for motorcycle-mounted traffic hazard anticipation.

The app processes a live camera stream directly on device and visualizes predicted traffic risk through a lightweight safety dashboard.

<div class="feature-grid">
  <div class="feature">Causal frame-by-frame inference</div>
  <div class="feature">Live traffic risk estimation</div>
  <div class="feature">SAFE / WARNING / DANGER state prediction</div>
  <div class="feature">Frame-level hazard probability</div>
  <div class="feature">Current riding speed</div>
  <div class="feature">Visual hazard localization cues</div>
  <div class="feature">Sound and vibration warning options</div>
  <div class="feature">Runtime controls for camera, resolution, inference frequency, focus, and exposure</div>
</div>

The system was tested in real-world urban riding scenarios, including rainy roads, nighttime traffic, dense scooter flows, intersections, and mixed vehicle environments.

</div>

<div class="section-card">

## Demo Gallery

The following demos show HERMES running in real time on iPhone during motorcycle-mounted riding in real-world urban traffic.

<div class="note">
GIFs may take several seconds to load depending on network speed. Each demo is sampled from real riding footage.
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

<h3>iOS App Interface</h3>

<div class="image-card">
  <img src="assets/Hermes_app.png" alt="Annotated HERMES iOS interface">
</div>

The HERMES iOS interface is designed for real-time riding feedback while keeping the road view unobstructed.

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
    <td>Processes the iPhone camera stream directly on device using causal frame-by-frame inference.</td>
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

<div class="section-card">

<h3> System Pipeline </h3>

<div class="image-card">
  <img src="assets/diagram.png" alt="HERMES iOS safety diagram">
</div>

</div>

<div class="section-card">

<h3> Highlights </h3>

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

<h3> Method Overview </h3>

HERMES uses a <b>Hierarchical Spatio-Temporal RWKV** backbone for efficient causal video understanding.

<div class="method-grid">

<div class="method-card">

<h4> HST-RWKV Backbone </h4>

The backbone combines hierarchical spatial encoding with recurrent temporal modeling, enabling online video understanding without requiring access to the full video sequence.

</div>

<div class="method-card">

<h4> Multi-rate Event Sensing </h4>

Stride-controlled recurrent updates capture both fast motion cues and longer-range temporal context within a single recurrent architecture.

</div>

<div class="method-card"> 

<h4> Causal Future Distillation </h4>

Causal Future Distillation transfers future-aware representation targets during training while preserving strictly causal inference at test time.

</div>

<div class="method-card">

<h4> Unified Multi-task Objective </h4>

HERMES jointly predicts traffic anomaly occurrence, hazard localization, and anomaly category from the same causal video representation.

</div>

</div>

</div>

<div class="section-card">

<h3> Deployment </h3>

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

<h3> Status </h3>

Current status:

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

<h3> Contact </h3>

<p><b>Patrik Patera, Ph.D.</b></p>
<p><i>Computer Vision & Deep Learning Research Egnineer</i></p>
<p>Taiwan</p>
<p>pat.patera@gmail.com</p>

</div>
