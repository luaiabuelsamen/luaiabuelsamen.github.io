---
permalink: /
title: "Luai Abuelsamen"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! I'm a Master's student in Robotics at UC Berkeley working on embodied AI systems that bridge foundation models with real-world control. My research spans from multimodal perception for robot manipulation to large-scale autonomous systems simulation.

Currently, I work as a Graduate Student Researcher at [PATH](https://path.berkeley.edu), building traffic simulation tools to evaluate infrastructure impacts on autonomous vehicle behavior. I also collaborate with the [Autonomy, Robotics, and Controls (ARC)](https://sites.google.com/berkeley.edu/prof-roberto-horowitz/people) Lab on manipulation research combining learning-based control with multimodal perception.

Previously, I studied Mechanical Engineering at McGill University and interned at Tesla, Beta Technologies, and Vention, where I worked on embedded systems, mechatronic design, and simulation tooling for robotic platforms.

**Research Interests:**
- Foundation models for robotics and embodied AI
- Multimodal perception and imitation learning  
- Model-based and learning-based control
- Sim-to-real transfer and real-time planning
- Multi-agent systems and intelligent infrastructure

---

<div class="project-grid">

  <div class="project-card">
    <img src="/images/voxels.png" alt="Multimodal Imitation Learning" />
    <div class="project-content">
      <h3><strong>Multimodal Perception in Imitation Learning</strong></h3>
      <p>Research collaboration analyzing how RGB-D, proprioceptive, and language inputs affect sample complexity and optimization landscapes in robot manipulation tasks, with theoretical insights and empirical validation.</p>
      <p>
        <a href="https://arxiv.org/abs/2508.05077">📄 Paper</a> · 
        <a href="https://github.com/luaiabuelsamen/pick_and_place">🔗 Code</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/gpu.png" alt="Industrial Robot Motion Planning" />
    <div class="project-content">
      <h3><strong>Industrial Robot Motion Planning with GPUs</strong></h3>
      <p>Integrated NVIDIA cuRobo into modular automation systems for real-time, collision-free trajectory planning in multi-axis robotic platforms, achieving significant speedups for industrial applications.</p>
      <p>
        <a href="https://github.com/luaiabuelsamen/VentionMotionPlanner">🔗 Code</a> · 
        <a href="https://arxiv.org/abs/2508.04146">📄 Paper</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/traffic.gif" alt="PATH Simulation" />
    <div class="project-content">
      <h3><strong>Autonomous Vehicle Infrastructure Impact Study</strong></h3>
      <p>Funded research position developing microsimulation models using Aimsun Next to assess freeway auxiliary lane removal impacts on mainline and arterial flows in mixed autonomy scenarios.</p>
      <p>
        <a href="https://drive.google.com/file/d/1Uvhiqlq9BkToVlS6ZZTnwhuWWCBXudWC/view?usp=sharing">📄 Paper (submitted to TRB)</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/CoverageControl.png" alt="Coverage Control" />
    <div class="project-content">
      <h3><strong>Coverage Control for Hybrid Aerial / Ground Robot Teams</strong></h3>
      <p>Developed a two-layer Voronoi-based approach for multi-agent coverage in heterogeneous robot teams, improving emergency response coordination and resilience to sensor loss.</p>
      <p>
        <a href="https://github.com/dHutchings/ME292B/tree/master/final_project">🔗 Code</a> · 
        <a href="https://drive.google.com/file/d/1XoUTgT1_qR2gOTL1xUAzfZ57Qem-vZP6/view">📄 Paper</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/rocket_trajectory.gif" alt="Rocket Landing Optimization" />
    <div class="project-content">
      <h3><strong>Rocket Landing Trajectory Optimization</strong></h3>
      <p>Implemented SOCP-based convex optimization in Python for soft landing guidance, accounting for vehicle dynamics, control limits, and environmental constraints with real-time performance.</p>
      <p>
        <a href="https://github.com/luaiabuelsamen/SoftLandingMPC">🔗 Code</a> · 
        <a href="https://docs.google.com/document/d/11QCTM3BNVeIW7PA9SoeAVAMo6YDuA-Zh4ko_VKOMwwU/edit?usp=sharing">📄 Report</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/drone.png" alt="LLM Drone Control" />
    <div class="project-content">
      <h3><strong>LLM-Based Natural Language Drone Control</strong></h3>
      <p>Rapid prototyping project integrating vision-language models, SLAM, and zero-shot action chunking for voice-controlled quadrotor navigation in real environments. Built for Eric Schmidt AI hackathon.</p>
      <p>
        <a href="https://github.com/einjun03/drone_follower">🔗 Code</a> · 
        <a href="https://drive.google.com/file/d/1fDzkQsQkkZZLiuYc3AgknRpwYNpTFnID/view?usp=drive_link">🎥 Video</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/pihatrobot.gif" alt="Motor Controller Pi-Hat" />
    <div class="project-content">
      <h3><strong>PCB Design: Raspberry Pi Motor Controller Hat</strong></h3>
      <p>Custom PCB enabling high-current servo control and force sensing for autonomous robots, with integrated power regulation and I²C multiplexing for research platform development.</p>
      <p><a href="https://sites.google.com/berkeley.edu/ape-sp25-project-showcase/ape-robot-pi-hat?authuser=0">🔗 Project Page</a></p>
    </div>
  </div>

</div>

<style>
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 1.5rem;
  margin-top: 1rem;
  align-items: stretch;
}
.project-card {
  border-radius: 10px;
  padding: 1rem;
  background: #fafafa;
  border: 1px solid #e1e1e1;
  box-shadow: 0 3px 8px rgba(0,0,0,0.06);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  display: flex;
  flex-direction: column;
  height: 100%;
}
.project-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 14px rgba(0,0,0,0.1);
}
.project-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 6px;
  margin-bottom: 0.75rem;
}
.project-content {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.project-content h3 {
  margin: 0 0 0.4rem;
  font-size: 1.1rem;
  color: #222;
}
.project-content p {
  margin: 0.25rem 0;
  font-size: 0.9rem;
  line-height: 1.4;
  color: #555;
}
.project-content a {
  text-decoration: none;
  color: #0066cc;
}
.project-content a:hover {
  text-decoration: underline;
}

/* Dark mode support - only when explicitly set by theme */
[data-theme="dark"] .project-card,
.dark .project-card {
  background: #1a1a1a;
  border-color: #333;
}
[data-theme="dark"] .project-content h3,
.dark .project-content h3 {
  color: #ffffff;
}
[data-theme="dark"] .project-content p,
.dark .project-content p {
  color: #cccccc;
}
[data-theme="dark"] .project-content a,
.dark .project-content a {
  color: #66b3ff;
}

/* Fallback for system dark mode preference, but only if theme supports it */
@media (prefers-color-scheme: dark) {
  body.dark-mode .project-card,
  html.dark .project-card {
    background: #1a1a1a;
    border-color: #333;
  }
  body.dark-mode .project-content h3,
  html.dark .project-content h3 {
    color: #ffffff;
  }
  body.dark-mode .project-content p,
  html.dark .project-content p {
    color: #cccccc;
  }
  body.dark-mode .project-content a,
  html.dark .project-content a {
    color: #66b3ff;
  }
}
</style>
