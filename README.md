# Humanoid Navigation in Crowds&Narrow Spaces
Navigation framework for bipedal humanoid robots in crowded and narrow environments, featuring adaptive body orientation and sideways passing. Includes MuJoCo demos and Unitree G1 deployment.



# Humanoid Navigation in Crowds and Narrow Spaces

> Social-aware navigation for bipedal humanoid robots in complex environments.

---

## About This Project

This project studies **navigation for bipedal humanoid robots** in **crowded and constrained environments** — scenarios where a typical wheeled robot would slow down or stop, but a humanoid can **adjust its body orientation and pass sideways** through narrow gaps while remaining aware of nearby pedestrians.

Our framework uses a **layered navigation pipeline**:

- **High level:** global path planning on a 2D map  
- **Middle level:** corridor-width-aware path evaluation and local path adjustment  
- **Low level:** velocity and body-orientation tracking (including sideways passing)  
- **Locomotion:** AMP-trained policy (ONNX) for whole-body motion on Unitree G1  

The same core idea applies to both:
- **Narrow corridors** — adapt body orientation to fit the available width  
- **Social scenes** — respond early to pedestrians and adjust passing behavior  

---

## What We Have So Far

| Component | Status |
|-----------|--------|
| Full-stack MuJoCo simulation (planning → tracking → locomotion) | ✅ Available (demo videos) |
| Real-robot SLAM & localization (FAST-LIO2 + human_loc) | ✅ Deployed |
| Real-robot global planning + corridor tracking | ✅ Tested |
| Vision-based pedestrian detection & local planning | 🔜 In progress |

> **Note:** Source code will be released after paper submission. This repository currently serves as the **project page** with demo videos and a brief overview.

---

## Demo Videos

Sideways passing through corridors (straight&curved)

https://github.com/user-attachments/assets/e4cf1782-c612-44ec-906f-b2d3d89e4d40

Humanoid navigates a corridor with a pedestrian; adapts path and body orientation

https://github.com/user-attachments/assets/7f0e76d5-9efe-4906-befb-da844962b17f

Unitree G1 navigation with LiDAR SLAM and global planning

https://github.com/user-attachments/assets/027c076f-f5c4-48d4-bcd6-ede91fb5148e

Local planning using hybrid A*

https://github.com/user-attachments/assets/fa13414a-9857-4758-9378-4430fc66925c

Adaptive Local planning 

https://github.com/user-attachments/assets/872429d7-e9e8-496e-9328-a606a1c9695a

---

## Platform

- **Robot:** Unitree G1 (29-DOF bipedal humanoid)  
- **Simulation:** MuJoCo  
- **Real robot:** ROS 2, FAST-LIO2, onboard LiDAR  

---
## Author

Zijian Ge

## Citation
