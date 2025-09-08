# Final-year-Project
# Deep Reinforcement Learning for Autonomous Mobile Robot Navigation in V-REP Simulator

This repository contains our final-year B.Tech project at NIT Arunachal Pradesh.  
It extends the baseline DDPG implementation with advanced DRL algorithms (TD3, SAC, PPO), domain randomization, sensor fusion and curriculum learning.
Current version is a little bit modified and much improved. The project is using modified algorithm Deterministic Policy Gradient ([Lillicrap et al.arXiv:1509.02971](https://arxiv.org/pdf/1509.02971.pdf)) (written in Tensorflow) to control mobile robot. The main idea was to learn mobile robot navigate to goal and also avoid obstacles. For obstacles avoidance, robot is using 5 ultrasonic sensors. For navigation task, required information (like absolute pose) are taken from simulation engine. That's a little hack. However, more realistic (like odometry) pose estimation can be found in [gym-vrep](https://github.com/Souphis/gym-vrep).

## Authors
Jaji Vagdhevi Chinta · Rakesh Kumar Swain · Sachin Pathak · Piyush Randeep  
Supervisor: Dr. Biri Arun, Dept. of CSE, NIT Arunachal Pradesh

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
