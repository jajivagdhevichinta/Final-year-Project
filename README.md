# Final-year-Project
# Deep Reinforcement Learning for Autonomous Mobile Robot Navigation in V-REP Simulator

This repository contains our final-year B.Tech project at NIT Arunachal Pradesh.  
It extends the baseline DDPG implementation of [gbartyzel/mobile_robot_rl] with advanced DRL algorithms (TD3, SAC, PPO), domain randomization, sensor fusion and curriculum learning.

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
### 1. Install dependencies
    ```bash
    pip install -r requirements.txt

### 2. Train
    python src/train.py --algo sac

### 3. Evaluate
    python src/eval.py
