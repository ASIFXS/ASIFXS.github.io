---
layout: default
title: Asif Ali — Research Engineer
permalink: /
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=JetBrains+Mono:wght@300;400;500&family=IBM+Plex+Sans:wght@300;400;500&display=swap');

:root {
  --bg:        #0a0a0c;
  --bg2:       #111116;
  --bg3:       #18181f;
  --border:    rgba(255,255,255,0.07);
  --accent:    #ff5a28;
  --accent2:   #3ecfcf;
  --text:      #e8e6e0;
  --muted:     rgba(232,230,224,0.45);
  --mono:      'JetBrains Mono', monospace;
  --sans:      'IBM Plex Sans', sans-serif;
  --display:   'Syne', sans-serif;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: var(--sans);
  line-height: 1.6;
  overflow-x: hidden;
}

/* ── NOISE OVERLAY ── */
body::before {
  content: '';
  position: fixed;
  inset: 0;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
  pointer-events: none;
  z-index: 0;
  opacity: 0.5;
}

/* ── NAV ── */
.nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 56px;
  background: rgba(10,10,12,0.85);
  backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: var(--mono);
  font-size: 13px;
  font-weight: 500;
  color: var(--accent);
  letter-spacing: 0.04em;
  text-decoration: none;
}
.nav-links {
  display: flex;
  gap: 36px;
  list-style: none;
}
.nav-links a {
  font-family: var(--mono);
  font-size: 11px;
  font-weight: 400;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--muted);
  text-decoration: none;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--text); }

/* ── WRAPPER ── */
.site {
  position: relative;
  z-index: 1;
  max-width: 1100px;
  margin: 0 auto;
  padding: 0 40px;
}

/* ── HERO ── */
.hero {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding-top: 100px;
  padding-bottom: 80px;
  position: relative;
}
.hero::after {
  content: '';
  position: absolute;
  top: 20%; right: -10%;
  width: 600px; height: 600px;
  background: radial-gradient(circle, rgba(255,90,40,0.07) 0%, transparent 65%);
  pointer-events: none;
}
.hero-eyebrow {
  font-family: var(--mono);
  font-size: 11px;
  font-weight: 400;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 28px;
  display: flex;
  align-items: center;
  gap: 12px;
}
.hero-eyebrow::before {
  content: '';
  display: inline-block;
  width: 32px; height: 1px;
  background: var(--accent);
}
.hero-name {
  font-family: var(--display);
  font-size: clamp(52px, 8vw, 96px);
  font-weight: 800;
  line-height: 0.95;
  letter-spacing: -0.04em;
  margin-bottom: 32px;
}
.hero-name span { color: var(--accent); }
.hero-role {
  font-family: var(--mono);
  font-size: 13px;
  color: var(--accent2);
  letter-spacing: 0.1em;
  margin-bottom: 28px;
}
.hero-bio {
  font-size: 16px;
  font-weight: 300;
  line-height: 1.85;
  color: var(--muted);
  max-width: 580px;
  margin-bottom: 48px;
}
.hero-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-bottom: 52px;
}
.hero-tag {
  font-family: var(--mono);
  font-size: 10px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--muted);
  border: 1px solid var(--border);
  padding: 6px 14px;
  border-radius: 4px;
  background: var(--bg2);
}
.hero-cta {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}
.btn {
  font-family: var(--mono);
  font-size: 11px;
  font-weight: 500;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  text-decoration: none;
  padding: 14px 28px;
  border-radius: 6px;
  transition: all 0.25s ease;
  display: inline-flex;
  align-items: center;
  gap: 8px;
}
.btn-primary {
  background: var(--accent);
  color: #fff;
  border: 1px solid var(--accent);
}
.btn-primary:hover {
  background: transparent;
  color: var(--accent);
}
.btn-ghost {
  background: transparent;
  color: var(--muted);
  border: 1px solid var(--border);
}
.btn-ghost:hover {
  border-color: rgba(255,255,255,0.2);
  color: var(--text);
}

/* ── SECTION ── */
.section {
  padding: 100px 0;
  border-top: 1px solid var(--border);
}
.section-label {
  font-family: var(--mono);
  font-size: 10px;
  font-weight: 500;
  letter-spacing: 0.24em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 16px;
  display: flex;
  align-items: center;
  gap: 12px;
}
.section-label::before {
  content: '';
  display: inline-block;
  width: 24px; height: 1px;
  background: var(--accent);
}
.section-title {
  font-family: var(--display);
  font-size: clamp(28px, 4vw, 44px);
  font-weight: 800;
  letter-spacing: -0.03em;
  line-height: 1.1;
  margin-bottom: 56px;
}

/* ── ABOUT GRID ── */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: start;
}
.about-text p {
  font-size: 15px;
  font-weight: 300;
  line-height: 1.9;
  color: var(--muted);
  margin-bottom: 20px;
}
.about-text p:last-child { margin-bottom: 0; }
.about-stats {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2px;
}
.stat-box {
  background: var(--bg2);
  border: 1px solid var(--border);
  padding: 28px 24px;
  border-radius: 2px;
}
.stat-box:first-child { border-radius: 12px 2px 2px 2px; }
.stat-box:nth-child(2) { border-radius: 2px 12px 2px 2px; }
.stat-box:nth-child(3) { border-radius: 2px 2px 2px 12px; }
.stat-box:last-child { border-radius: 2px 2px 12px 2px; }
.stat-num {
  font-family: var(--display);
  font-size: 36px;
  font-weight: 800;
  color: var(--accent);
  letter-spacing: -0.03em;
  line-height: 1;
  margin-bottom: 6px;
}
.stat-label {
  font-family: var(--mono);
  font-size: 10px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--muted);
}

/* ── RESEARCH CARDS ── */
.research-grid {
  display: grid;
  gap: 2px;
}
.r-card {
  background: var(--bg2);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 36px 40px;
  display: grid;
  grid-template-columns: 80px 1fr auto;
  align-items: center;
  gap: 32px;
  text-decoration: none;
  color: inherit;
  transition: background 0.25s, border-color 0.25s;
  position: relative;
  overflow: hidden;
}
.r-card::before {
  content: '';
  position: absolute;
  left: 0; top: 0; bottom: 0;
  width: 3px;
  background: var(--accent);
  transform: scaleY(0);
  transform-origin: bottom;
  transition: transform 0.3s ease;
}
.r-card:hover { background: var(--bg3); border-color: rgba(255,255,255,0.12); }
.r-card:hover::before { transform: scaleY(1); }
.r-num {
  font-family: var(--display);
  font-size: 48px;
  font-weight: 800;
  color: rgba(255,255,255,0.05);
  line-height: 1;
  letter-spacing: -0.04em;
  transition: color 0.3s;
}
.r-card:hover .r-num { color: rgba(255,90,40,0.15); }
.r-body {}
.r-tags {
  display: flex;
  gap: 8px;
  flex-wrap: wrap;
  margin-bottom: 10px;
}
.r-tag {
  font-family: var(--mono);
  font-size: 9px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--accent2);
  border: 1px solid rgba(62,207,207,0.2);
  padding: 3px 9px;
  border-radius: 3px;
}
.r-title {
  font-family: var(--display);
  font-size: 17px;
  font-weight: 700;
  letter-spacing: -0.01em;
  color: var(--text);
  margin-bottom: 8px;
  line-height: 1.3;
}
.r-desc {
  font-size: 13px;
  font-weight: 300;
  color: var(--muted);
  line-height: 1.7;
}
.r-arrow {
  font-size: 20px;
  color: var(--muted);
  transition: color 0.2s, transform 0.2s;
}
.r-card:hover .r-arrow { color: var(--accent); transform: translateX(4px); }

/* ── CONTACT ── */
.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  align-items: start;
}
.contact-text {
  font-size: 15px;
  font-weight: 300;
  line-height: 1.9;
  color: var(--muted);
}
.contact-links {
  display: flex;
  flex-direction: column;
  gap: 2px;
}
.contact-link {
  display: flex;
  align-items: center;
  gap: 20px;
  padding: 20px 24px;
  background: var(--bg2);
  border: 1px solid var(--border);
  border-radius: 4px;
  text-decoration: none;
  color: var(--muted);
  font-size: 13px;
  transition: all 0.2s;
}
.contact-link:hover {
  background: var(--bg3);
  border-color: rgba(255,255,255,0.12);
  color: var(--text);
}
.contact-link-icon {
  width: 36px; height: 36px;
  background: var(--bg3);
  border: 1px solid var(--border);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
  font-size: 16px;
}
.contact-link-label {
  font-family: var(--mono);
  font-size: 10px;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--accent);
  display: block;
  margin-bottom: 2px;
}
.contact-link-val {
  font-size: 13px;
  color: var(--muted);
}

/* ── FOOTER ── */
.footer {
  border-top: 1px solid var(--border);
  padding: 36px 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.footer-left {
  font-family: var(--mono);
  font-size: 11px;
  color: var(--muted);
  letter-spacing: 0.06em;
}
.footer-right {
  font-family: var(--mono);
  font-size: 11px;
  color: var(--muted);
}
.footer-right span { color: var(--accent); }

/* ── FADE-IN ── */
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(24px); }
  to   { opacity: 1; transform: translateY(0); }
}
.hero-eyebrow { animation: fadeUp 0.6s ease both; animation-delay: 0.1s; }
.hero-name    { animation: fadeUp 0.6s ease both; animation-delay: 0.2s; }
.hero-role    { animation: fadeUp 0.6s ease both; animation-delay: 0.3s; }
.hero-bio     { animation: fadeUp 0.6s ease both; animation-delay: 0.4s; }
.hero-tags    { animation: fadeUp 0.6s ease both; animation-delay: 0.5s; }
.hero-cta     { animation: fadeUp 0.6s ease both; animation-delay: 0.6s; }

/* ── RESPONSIVE ── */
@media (max-width: 768px) {
  .nav { padding: 16px 24px; }
  .nav-links { gap: 20px; }
  .site { padding: 0 20px; }
  .about-grid, .contact-grid { grid-template-columns: 1fr; }
  .r-card { grid-template-columns: 1fr; gap: 16px; }
  .r-num { font-size: 32px; }
  .r-arrow { display: none; }
  .footer { flex-direction: column; gap: 12px; text-align: center; }
}
</style>

<!-- NAV -->
<nav class="nav">
  <a class="nav-logo" href="/">&lt;asif.ali /&gt;</a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#research">Research</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<div class="site">

  <!-- ── HERO ── -->
  <section class="hero">
    <div class="hero-eyebrow">Research Engineer · IIT Madras</div>
    <h1 class="hero-name">Asif<br><span>Ali</span></h1>
    <div class="hero-role">// Autonomous Systems Lab</div>
    <p class="hero-bio">
      I am a Research Engineer at the Autonomous Systems Lab, IIT Madras, working at the intersection of robotics, computer vision, and AI. My work focuses on enabling robots to perceive, reason, and act intelligently in unstructured real-world environments — from language-guided grasping to safe human-robot collaboration.
    </p>
    <div class="hero-tags">
      <span class="hero-tag">Robotics &amp; Manipulation</span>
      <span class="hero-tag">Computer Vision</span>
      <span class="hero-tag">Large Language Models</span>
      <span class="hero-tag">Human-Robot Collaboration</span>
    </div>
    <div class="hero-cta">
      <a class="btn btn-primary" href="#research">View Research →</a>
      <a class="btn btn-ghost" href="#contact">Get in Touch</a>
    </div>
  </section>

  <!-- ── ABOUT ── -->
  <section class="section" id="about">
    <div class="section-label">About Me</div>
    <h2 class="section-title">Building intelligent<br>robotic systems</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>
          I work as a Research Engineer at the Autonomous Systems Lab, IIT Madras, where I develop perception and planning frameworks for robotic manipulation. My research bridges classical robotics with modern AI — combining sensor fusion, motion planning, and large language models to push the boundaries of what autonomous systems can do.
        </p>
        <p>
          I am particularly interested in open-vocabulary manipulation, where robots can act on natural language instructions without being limited to predefined object categories. I also work on real-time human-aware motion planning to enable safe and seamless collaboration between robots and people in shared workspaces.
        </p>
        <p>
          My tools of choice include ROS, Python, PyTorch, and a range of depth sensors and robotic manipulators including the UR5e and Robotiq grippers.
        </p>
      </div>
      <div class="about-stats">
        <div class="stat-box">
          <div class="stat-num">3+</div>
          <div class="stat-label">Research Projects</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">IIT</div>
          <div class="stat-label">Madras · ASL</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">ROS</div>
          <div class="stat-label">Primary Stack</div>
        </div>
        <div class="stat-box">
          <div class="stat-num">AI</div>
          <div class="stat-label">Focus Area</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ── RESEARCH ── -->
  <section class="section" id="research">
    <div class="section-label">Research</div>
    <h2 class="section-title">Selected projects</h2>
    <div class="research-grid">

      <a class="r-card" href="/intelligent_grasping/">
        <div class="r-num">01</div>
        <div class="r-body">
          <div class="r-tags">
            <span class="r-tag">LLM</span>
            <span class="r-tag">Segmentation</span>
            <span class="r-tag">Grasping</span>
          </div>
          <div class="r-title">Intelligent Grasp Planning using Open Vocabulary Image Segmentation and LLM</div>
          <div class="r-desc">A framework combining open vocabulary image segmentation with LLMs to enable language-guided, semantically-aware grasp planning without predefined object categories.</div>
        </div>
        <div class="r-arrow">→</div>
      </a>

      <a class="r-card" href="/intelligent_grasping/#project02">
        <div class="r-num">02</div>
        <div class="r-body">
          <div class="r-tags">
            <span class="r-tag">HRC</span>
            <span class="r-tag">Motion Planning</span>
            <span class="r-tag">Real-time</span>
          </div>
          <div class="r-title">Real-time Perception and Motion Planning for Human-Robot Collaboration</div>
          <div class="r-desc">A real-time framework enabling a UR5e manipulator to dynamically re-plan trajectories in response to human movement, ensuring safe and efficient co-working.</div>
        </div>
        <div class="r-arrow">→</div>
      </a>

      <a class="r-card" href="/intelligent_grasping/#project03">
        <div class="r-num">03</div>
        <div class="r-body">
          <div class="r-tags">
            <span class="r-tag">Sensor Fusion</span>
            <span class="r-tag">Manipulation</span>
            <span class="r-tag">Pick &amp; Place</span>
          </div>
          <div class="r-title">Perception and Motion Planning for Autonomous Grasping</div>
          <div class="r-desc">Sensor fusion-based estimation of unknown object properties to plan stable, autonomous grasps using a three-finger Robotiq gripper and fiducial markers.</div>
        </div>
        <div class="r-arrow">→</div>
      </a>

    </div>
  </section>

  <!-- ── CONTACT ── -->
  <section class="section" id="contact">
    <div class="section-label">Contact</div>
    <h2 class="section-title">Let's connect</h2>
    <div class="contact-grid">
      <p class="contact-text">
        I'm always open to discussing research collaborations, project ideas, or opportunities in robotics and AI. Feel free to reach out via email or connect with me on LinkedIn or GitHub.
      </p>
      <div class="contact-links">
        <a class="contact-link" href="mailto:mguasifali@gmail.com">
          <div class="contact-link-icon">✉</div>
          <div>
            <span class="contact-link-label">Email</span>
            <span class="contact-link-val">mguasifali@gmail.com</span>
          </div>
        </a>
        <a class="contact-link" href="https://www.linkedin.com/in/asifalitp/" target="_blank">
          <div class="contact-link-icon">in</div>
          <div>
            <span class="contact-link-label">LinkedIn</span>
            <span class="contact-link-val">linkedin.com/in/asifalitp</span>
          </div>
        </a>
        <a class="contact-link" href="https://github.com/ASIFXS" target="_blank">
          <div class="contact-link-icon">⌥</div>
          <div>
            <span class="contact-link-label">GitHub</span>
            <span class="contact-link-val">github.com/ASIFXS</span>
          </div>
        </a>
      </div>
    </div>
  </section>

  <!-- ── FOOTER ── */-->
  <footer class="footer">
    <div class="footer-left">© 2026 Asif Ali · IIT Madras</div>
    <div class="footer-right">Built with <span>♥</span> using Jekyll</div>
  </footer>

</div>
