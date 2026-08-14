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

<table>
  <!-- Simulation -->
  <tr>
    <td colspan="3" align="left">
      <h3>🎮 Simulation Demos</h3>
    </td>
  </tr>
  <tr>
    <td width="50%" align="center" valign="top" colspan="2">
      <h4>🚶‍♂️ Sideways Passing Through Corridors</h4>
      <video src="https://github.com/user-attachments/assets/e4cf1782-c612-44ec-906f-b2d3d89e4d40" controls width="100%"></video>
      <br>
      <em>Straight & curved corridors</em>
    </td>
    <td width="50%" align="center" valign="top">
      <h4>👥 Corridor Navigation with Pedestrian</h4>
      <video src="https://github.com/user-attachments/assets/7f0e76d5-9efe-4906-befb-da844962b17f" controls width="100%"></video>
      <br>
      <em>Adapts path and body orientation</em>
    </td>
  </tr>

  <!-- Real Deployment -->
  <tr>
    <td colspan="3" align="left">
      <h3>🤖 Real Robot Deployment</h3>
    </td>
  </tr>
  <tr>
    <td width="33.3%" align="center" valign="top">
      <h4> Unitree G1 Navigation</h4>
      <video src="https://github.com/user-attachments/assets/027c076f-f5c4-48d4-bcd6-ede91fb5148e" controls width="100%"></video>
      <br>
      <em>LiDAR SLAM & global planning</em>
    </td>
    <td width="33.3%" align="center" valign="top">
      <h4>🗺️ Hybrid A* Local Planning</h4>
      <video src="https://github.com/user-attachments/assets/fa13414a-9857-4758-9378-4430fc66925c" controls width="100%"></video>
    </td>
    <td width="33.3%" align="center" valign="top">
      <h4>🔄 Adaptive Local Planning</h4>
      <video src="https://github.com/user-attachments/assets/872429d7-e9e8-496e-9328-a606a1c9695a" controls width="100%"></video>
    </td>
  </tr>
</table>

---

## Platform

- **Robot:** Unitree G1 (29-DOF bipedal humanoid)  
- **Simulation:** MuJoCo  
- **Real robot:** ROS 2, FAST-LIO2, onboard LiDAR  

---
## Author

Zijian Ge

## Citation
