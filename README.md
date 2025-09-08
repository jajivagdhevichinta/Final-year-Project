# Final-year-Project
# Deep Reinforcement Learning for Autonomous Mobile Robot Navigation in V-REP Simulator

This repository contains our final-year B.Tech project at NIT Arunachal Pradesh.  
It extends the baseline DDPG implementation with advanced DRL algorithms (TD3, SAC, PPO), domain randomization, sensor fusion and curriculum learning.
Current version is a little bit modified and much improved. The project is using modified algorithm Deterministic Policy Gradient ([Lillicrap et al.arXiv:1509.02971](https://arxiv.org/pdf/1509.02971.pdf)) (written in Tensorflow) to control mobile robot. The main idea was to learn mobile robot navigate to goal and also avoid obstacles. For obstacles avoidance, robot is using 5 ultrasonic sensors. For navigation task, required information (like absolute pose) are taken from simulation engine. That's a little hack. However, more realistic (like odometry) pose estimation can be found in [gym-vrep](https://github.com/Souphis/gym-vrep).

## Phase 1 – Baseline Study with DDPG
The initial phase, rooted in a prior Master’s thesis, implemented **DDPG** to train a simulated mobile robot in **V-REP**.  
- **Objective:** Goal-directed navigation with obstacle avoidance.  
- **Setup:** The robot used *absolute pose information* (hacked for simulation) and *five ultrasonic sensors*.  
- **Outcome:** Demonstrated DDPG’s ability to learn continuous control policies, but also revealed well-known limitations:  
  - Low sample efficiency  
  - High sensitivity to hyperparameters  
  - Limited robustness in diverse environments  

---

## Phase 2 – Research Agenda for Enhanced Learning
Building on these insights, the project proposed a **forward-looking research roadmap** designed to overcome DDPG’s limitations. The key elements include:  

### Algorithmic Upgrades
- Transition to advanced DRL algorithms such as:  
  - **Soft Actor-Critic (SAC)**  
  - **Twin Delayed DDPG (TD3)**  
  - **Proximal Policy Optimization (PPO)**  

### Training Enhancements
- **Domain Randomization:** Improve robustness and address the sim-to-real gap.  
- **Curriculum Learning:** Introduce progressive task difficulty to master complex behaviors.  
- **Sensor Fusion:** Move beyond sparse ultrasonic + absolute pose to realistic odometry, vision, or LiDAR.  
- **Hierarchical RL:** Explore layered architectures to tackle complex multi-step tasks.  

---

## Requirements & Methodology
The proposal included a detailed analysis of:  
- **Functional Requirements:** Ability to navigate reliably, avoid obstacles, and adapt to dynamic environments.  
- **Non-Functional Goals:** Higher success rates, smoother control, robustness under uncertainty, and stable training dynamics.  
- **Phased Development Roadmap:** Structured implementation and evaluation of each enhancement step-by-step.  

---

## Expected Contributions
This work is expected to contribute to both academic and practical domains:  
- Empirical benchmarks for DRL algorithms in mobile robotics.  
- A validated methodology for systematically enhancing DRL systems.  
- Practical insights into applying SAC, TD3, PPO, and training techniques in **V-REP** (or similar simulators).  
- A pathway toward control policies that are:  
  - More efficient and robust  
  - Generalizable to real-world robot deployments  
  - Scalable to more complex robotic tasks  

## Features
- V-REP/CoppeliaSim environment with gym-like API
- Baseline DDPG + upgraded SAC/TD3/PPO agents (Stable Baselines3 / RLlib)
- Domain randomization for robustness
- Sensor fusion (ultrasonic, odometry, camera/LiDAR)
- Curriculum/Hierarchical learning experiments
- Training & evaluation scripts

## Getting Started
## Simulation
Project is using robotic simulation [V-REP EDU](http://www.coppeliarobotics.com/). To setup V-REP environment follow instruction described in [gym-vrep](https://github.com/Souphis/gym-vrep) repository.
### 1. Install dependencies
    pip install -r requirements.txt

### 2. To run training just run command:
    python main.py --train

### 3. To run testing just run command:
    python main.py

### Result
![Alt text for the image](https://github.com/jajivagdhevichinta/Final-year-Project/blob/main/file_2025-05-29_06.39.45.png)
