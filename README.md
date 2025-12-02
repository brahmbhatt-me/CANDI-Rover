# CANDI Rover – Compact Autonomous Navigating Delivery Intelligence

This repository contains the complete ROS2 simulation, robot description, and navigation stack for the C.A.N.D.I Rover. The project implements a fully virtual autonomous rover developed for the EECE 5554 Robot Sensing and Navigation course at Northeastern University.

The rover is modeled in Fusion 360, converted to URDF, simulated in Gazebo, mapped using SLAM, and navigated using the ROS2 Navigation2 stack. The primary goal is to autonomously deliver a payload from the home position to a target location while avoiding obstacles.

---

## 1. Project Overview

CANDI is a four-wheeled simulated rover equipped with a 2D LiDAR and a forward-facing camera. The system includes:

- CAD-to-URDF pipeline
- Gazebo simulation environment
- SLAM for mapping
- Autonomous navigation using Nav2
- Sensor fusion and real-time visualization in RViz
- Custom desk-like simulation world

The project demonstrates end-to-end robot development: modeling, simulation, mapping, planning, and execution.

---

## 2. Repository Structure
```
CANDI-Rover/
│
├── src/
│   └── final_project_description/
│       ├── config/
│       ├── launch/
│       ├── meshes/
│       ├── resource/
│       ├── test/
│       ├── urdf/
│       ├── package.xml
│       ├── setup.py
│       └── setup.cfg
│
├── DOCS/
│
├── IMG_VID/
│
└── README.md
```

---

## 3. Main Components

### Robot Description (URDF/Xacro)
Located in `src/final_project_description/urdf/`:

- Base link and wheel joints
- LiDAR sensor plugin
- Camera plugin
- Transformation frames
- Gazebo physics and dynamics configuration

### Gazebo Simulation
Includes:

- Desk-style simulation world
- Sensor models
- Robot spawn configuration
- Physics tuning files

### SLAM
Implements:

- 2D occupancy grid mapping
- LiDAR-based real-time scan matching
- Map publishing and TF broadcasting

### Navigation (Nav2)
Includes:

- Global planner configuration
- Local planner (DWA) tuning
- Costmap parameters (static, obstacle, inflation layers)
- Goal execution and obstacle avoidance

---

## 4. Launch Files

The package contains launch files for:

- Robot description
- Gazebo world and robot spawning
- SLAM
- Navigation2
- RViz visualization

Examples (inside `launch/`):

- `display.launch.py`  
- `slam.launch.py`  
- `nav2.launch.py`  
- `gazebo.launch.py`

---

## 5. How to Run

Build the workspace:
```bash
colcon build
source install/setup.bash
```

Launch Gazebo with the rover:
```bash
ros2 launch final_project_description gazebo.launch.py
```

Launch SLAM:
```bash
ros2 launch final_project_description slam.launch.py
```

Launch Navigation:
```bash
ros2 launch final_project_description nav2.launch.py
```

Launch RViz:
```bash
ros2 launch final_project_description display.launch.py
```

---

## 6. Results

The system successfully performs:

- Real-time mapping using SLAM Toolbox
- Autonomous navigation from start to target
- Obstacle avoidance using local planning
- Consistent sensor visualization in RViz
- Smooth motion from tuned parameters

Supporting images, videos, and simulation captures are provided in the `IMG_VID/` folder.

---

## 7. Next Steps

- Improve environmental realism in Gazebo
- Add PID tuning for smoother motion
- Fix camera pose and plugin issues
- Implement improved perception modules
- Add basic object detection or ArUco-based goal recognition

---

## 8. Documents

The DOCS folder includes:

- Final project presentation (PDF)
- Supporting reference materials
- Work cited list

---

## 9. Team

Meet Brahmbhatt  
Dawei Wang  
Michael Nunes  
Shourya Vuddemarri

---

## 10. License

This project is released under the MIT License unless otherwise stated.
