# Humanoid-navigation-in-crowds-and-narrow-spaces
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

| Video | Description |
|-------|-------------|
| [Simulation — social corridor]() | Humanoid navigates a corridor with a pedestrian; adapts path and body orientation |
| [Simulation — narrow passage]() | Sideways passing through a tight gap |
| https://github.com/user-attachments/assets/d21c1aa0-2a7c-412d-a6a3-364e17943717| Unitree G1 navigation with LiDAR SLAM and global planning |

*(Links will be added when videos are uploaded.)*

---

## Platform

- **Robot:** Unitree G1 (29-DOF bipedal humanoid)  
- **Simulation:** MuJoCo  
- **Real robot:** ROS 2, FAST-LIO2, onboard LiDAR  

---

## Citation
