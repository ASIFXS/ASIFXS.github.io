---
layout: page
title: Intelligent Grasping
permalink: /intelligent_grasping/
ribbon_display: no
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;1,300&display=swap');

  .ig-wrapper {
    font-family: 'DM Sans', sans-serif;
    color: #0f1117;
    max-width: 960px;
    margin: 0 auto;
    padding: 0 0 80px 0;
  }

  .ig-hero {
    background: #0f1117;
    color: #fff;
    border-radius: 16px;
    padding: 56px 52px 48px;
    margin-bottom: 64px;
    position: relative;
    overflow: hidden;
  }

  .ig-hero::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 320px; height: 320px;
    background: radial-gradient(circle, rgba(255,107,53,0.18) 0%, transparent 70%);
    pointer-events: none;
  }

  .ig-hero::after {
    content: '';
    position: absolute;
    bottom: -80px; left: 30%;
    width: 280px; height: 280px;
    background: radial-gradient(circle, rgba(99,190,255,0.12) 0%, transparent 70%);
    pointer-events: none;
  }

  .ig-hero-label {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #ff6b35;
    margin-bottom: 18px;
  }

  .ig-hero h1 {
    font-family: 'Syne', sans-serif;
    font-size: clamp(28px, 4vw, 42px);
    font-weight: 800;
    line-height: 1.15;
    margin: 0 0 20px 0;
    letter-spacing: -0.02em;
  }

  .ig-hero p {
    font-size: 15px;
    line-height: 1.75;
    color: rgba(255,255,255,0.65);
    max-width: 680px;
    margin: 0;
    font-weight: 300;
  }

  .ig-card {
    border: 1px solid #e8e8e8;
    border-radius: 16px;
    overflow: hidden;
    margin-bottom: 48px;
    transition: box-shadow 0.3s ease, transform 0.3s ease;
    background: #fff;
  }

  .ig-card:hover {
    box-shadow: 0 20px 60px rgba(0,0,0,0.1);
    transform: translateY(-3px);
  }

  .ig-card-header {
    padding: 32px 36px 24px;
    border-bottom: 1px solid #f0f0f0;
  }

  .ig-card-number {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: #ff6b35;
    margin-bottom: 10px;
  }

  .ig-card-title {
    font-family: 'Syne', sans-serif;
    font-size: 20px;
    font-weight: 700;
    color: #0f1117;
    margin: 0 0 14px 0;
    line-height: 1.3;
    letter-spacing: -0.01em;
  }

  .ig-card-desc {
    font-size: 14px;
    line-height: 1.8;
    color: #555;
    margin: 0;
    font-weight: 300;
  }

  .ig-card-video {
    padding: 24px 36px 28px;
    background: #fafafa;
  }

  .ig-card-video-label {
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: #aaa;
    margin-bottom: 12px;
  }

  .ig-thumb-link {
    display: block;
    position: relative;
    border-radius: 10px;
    overflow: hidden;
    max-width: 480px;
    box-shadow: 0 4px 24px rgba(0,0,0,0.12);
  }

  .ig-thumb-link img {
    display: block;
    width: 100%;
    transition: transform 0.4s ease;
  }

  .ig-thumb-link:hover img {
    transform: scale(1.03);
  }

  .ig-play-overlay {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    background: rgba(15,17,23,0.35);
    transition: background 0.3s ease;
  }

  .ig-thumb-link:hover .ig-play-overlay {
    background: rgba(15,17,23,0.2);
  }

  .ig-play-btn {
    width: 52px; height: 52px;
    background: #ff6b35;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 4px 20px rgba(255,107,53,0.5);
    transition: transform 0.3s ease;
  }

  .ig-thumb-link:hover .ig-play-btn {
    transform: scale(1.1);
  }

  .ig-play-btn svg {
    width: 20px; height: 20px;
    fill: #fff;
    margin-left: 3px;
  }
</style>

<div class="ig-wrapper">

  <div class="ig-hero">
    <div class="ig-hero-label">Research · Autonomous Systems Lab · IIT Madras</div>
    <h1>Intelligent Grasping</h1>
    <p>Exploring the intersection of perception, language, and motion planning to enable robots to grasp and manipulate objects autonomously in unstructured, real-world environments.</p>
  </div>

  <!-- CARD 1 -->
  <div class="ig-card">
    <div class="ig-card-header">
      <div class="ig-card-number">Project 01</div>
      <h2 class="ig-card-title">Intelligent Grasp Planning using Open Vocabulary Image Segmentation and LLM</h2>
      <p class="ig-card-desc">Intelligent grasp planning in unstructured environments remains an open challenge, driven by applications in manufacturing, logistics, healthcare, and assistive robotics. Planning a stable grasp becomes significantly harder when object properties such as geometry, mass distribution, and surface compliance are not known in advance. This work proposes a framework that combines open vocabulary image segmentation with large language models (LLMs) to interpret natural language instructions, identify target objects in the scene, and plan semantically-aware grasps without relying on predefined object categories.</p>
    </div>
    <div class="ig-card-video">
      <div class="ig-card-video-label">▶ Full walkthrough — problem formulation, approach &amp; results</div>
      <a class="ig-thumb-link" href="https://www.youtube.com/watch?v=FAYOKLMosNI" target="_blank">
        <img src="https://img.youtube.com/vi/FAYOKLMosNI/0.jpg" alt="Intelligent Grasp Planning using Open Vocabulary Image Segmentation and LLM">
        <div class="ig-play-overlay">
          <div class="ig-play-btn">
            <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
          </div>
        </div>
      </a>
    </div>
  </div>

  <!-- CARD 2 -->
  <div class="ig-card">
    <div class="ig-card-header">
      <div class="ig-card-number">Project 02</div>
      <h2 class="ig-card-title">Real-time Perception and Motion Planning for Human-Robot Collaboration</h2>
      <p class="ig-card-desc">Human-robot collaboration in shared workspaces introduces significant challenges for motion planning, as the robot must continuously adapt to the presence and movement of human operators. This work presents a real-time perception and motion planning framework that enables a UR5e manipulator to safely operate alongside humans without interrupting task execution. The system fuses live human tracking with occupancy grid-based path planning, allowing the robot to dynamically re-plan its trajectory in response to human motion and avoid collisions in real time.</p>
    </div>
    <div class="ig-card-video">
      <div class="ig-card-video-label">▶ Full walkthrough — methodology, system design &amp; experimental results</div>
      <a class="ig-thumb-link" href="https://www.youtube.com/watch?v=HLudJf04hnI" target="_blank">
        <img src="https://img.youtube.com/vi/HLudJf04hnI/0.jpg" alt="Real-time Perception and Motion Planning">
        <div class="ig-play-overlay">
          <div class="ig-play-btn">
            <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
          </div>
        </div>
      </a>
    </div>
  </div>

  <!-- CARD 3 -->
  <div class="ig-card">
    <div class="ig-card-header">
      <div class="ig-card-number">Project 03</div>
      <h2 class="ig-card-title">Perception and Motion Planning for Autonomous Grasping</h2>
      <p class="ig-card-desc">Autonomous grasping is an active research area primarily because of the wide range of applications including manufacturing, logistics, assistive systems, and healthcare. Grasping and manipulation of objects in real-world environments is a challenging research problem, when properties of the object such as weight, shape, dimensions, stiffness etc. are unknown. This research work aims to explore sensor fusion to help estimate the object properties and then plan a stable grasp based on the manipulation requirements.</p>
    </div>
    <div class="ig-card-video">
      <div class="ig-card-video-label">▶ Preliminary results — autonomous pick-and-place with Robotiq gripper</div>
      <a class="ig-thumb-link" href="https://www.youtube.com/watch?v=glKLp9OO6yQ" target="_blank">
        <img src="https://img.youtube.com/vi/glKLp9OO6yQ/0.jpg" alt="Autonomous Pick and Place">
        <div class="ig-play-overlay">
          <div class="ig-play-btn">
            <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"/></svg>
          </div>
        </div>
      </a>
    </div>
  </div>

</div>
