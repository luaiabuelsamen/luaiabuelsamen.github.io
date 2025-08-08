---
permalink: /
title: "Luai Abuelsamen"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

Hi! I'm a Master's student in Robotics at UC Berkeley, currently exploring the intersection of intelligent systems, optimization, and control. I work as a Graduate Student Researcher at [PATH](https://path.berkeley.edu), building large-scale traffic simulation tools to evaluate the impact of infrastructure changes on human and autonomous driver behavior.

Previously, I studied Mechanical Engineering at McGill University and interned at Tesla, Beta Technologies, and Vention, where I worked on embedded systems, mechatronic design, and simulation tooling for robotic platforms.

I'm broadly interested in how learning-based systems can act, adapt, and reason in the real world. My work has touched on:
- Model-based and learning-based control  
- Multi-agent systems and intelligent infrastructure  
- Simulation and optimization for embodied agents  
- Design and computation tools for robotics and autonomy

---

<div class="project-grid">

  <div class="project-card">
    <img src="/images/drone.png" alt="LLM Drone Control" />
    <div class="project-content">
      <h3><strong>LLM-Based Natural Language Drone Control</strong></h3>
      <p>Integrated vision-language models, SLAM, and zero-shot action chunking for voice-controlled quadrotor navigation in real environments.</p>
      <p>
        <a href="https://github.com/einjun03/drone_follower">🔗 Code</a> · 
        <a href="https://drive.google.com/file/d/1fDzkQsQkkZZLiuYc3AgknRpwYNpTFnID/view?usp=drive_link">🎥 Video</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/CoverageControl.png" alt="Coverage Control" />
    <div class="project-content">
      <h3><strong>Coverage Control for Hybrid Aerial / Ground Robot Teams</strong></h3>
      <p>Developed a two-layer Voronoi-based approach for multi-agent coverage in heterogeneous robot teams, improving emergency response and resilience to sensor loss.</p>
      <p>
        <a href="https://github.com/dHutchings/ME292B/tree/master/final_project">🔗 Code</a> · 
        <a href="https://drive.google.com/file/d/1XoUTgT1_qR2gOTL1xUAzfZ57Qem-vZP6/view">📄 Paper</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/gpu.png" alt="Industrial Robot Motion Planning" />
    <div class="project-content">
      <h3><strong>Industrial Robot Motion Planning with GPUs</strong></h3>
      <p>Integrated NVIDIA cuRobo into modular automation systems for real-time, collision-free trajectory planning in multi-axis robotic platforms.</p>
      <p>
        <a href="https://github.com/luaiabuelsamen/VentionMotionPlanner">🔗 Code</a>
        <a href="https://arxiv.org/abs/2508.04146">📄 Paper/a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/rocket_trajectory.gif" alt="Rocket Landing Optimization" />
    <div class="project-content">
      <h3><strong>Rocket Landing Trajectory Optimization</strong></h3>
      <p>Implemented SOCP-based convex optimization in Python for soft landing guidance, accounting for dynamics, control limits, and environmental constraints.</p>
      <p>
        <a href="https://github.com/luaiabuelsamen/SoftLandingMPC">🔗 Code</a> · 
        <a href="https://docs.google.com/document/d/11QCTM3BNVeIW7PA9SoeAVAMo6YDuA-Zh4ko_VKOMwwU/edit?usp=sharing">📄 Report</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/voxels.png" alt="Multimodal Imitation Learning" />
    <div class="project-content">
      <h3><strong>Multimodal Perception in Imitation Learning</strong></h3>
      <p>Theoretical analysis of RGB-D, proprioceptive, and language input effects on sample complexity and optimization landscapes in imitation learning.</p>
      <p>
        <a href="https://arxiv.org/abs/2508.05077">📄 Paper</a>
        <a href="https://github.com/luaiabuelsamen/pick_and_place">🔗 Code</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/traffic.gif" alt="PATH Simulation" />
    <div class="project-content">
      <h3><strong>Auxiliary Lane Removal Impact Study</strong></h3>
      <p>Microsimulation analysis of freeway auxiliary lane removal using Aimsun Next, assessing impacts on mainline and arterial flows in mixed autonomy scenarios.</p>
      <p>
        <a href="https://drive.google.com/file/d/1Uvhiqlq9BkToVlS6ZZTnwhuWWCBXudWC/view?usp=sharing">📄 Paper (submitted to TRB)</a>
      </p>
    </div>
  </div>

  <div class="project-card">
    <img src="/images/pihatrobot.gif" alt="Motor Controller Pi-Hat" />
    <div class="project-content">
      <h3><strong>PCB Design: Raspberry Pi Motor Controller Hat</strong></h3>
      <p>Custom PCB enabling high-current servo control and force sensing for autonomous robots, with integrated power regulation and I²C multiplexing.</p>
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
}
.project-card {
  border-radius: 10px;
  padding: 1rem;
  background: #fafafa;
  box-shadow: 0 3px 8px rgba(0,0,0,0.06);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
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
.project-content h3 {
  margin: 0 0 0.4rem;
  font-size: 1.1rem;
}
.project-content p {
  margin: 0.25rem 0;
  font-size: 0.9rem;
  line-height: 1.4;
}
.project-content a {
  text-decoration: none;
}
</style>
