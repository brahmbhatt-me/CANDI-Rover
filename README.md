# CANDI Rover - Compact Autonomous Navigating Delivery Intelligence


An autonomous desktop delivery rover designed to deliver candy from a home state to boost productivity within workspace environments. Built with ROS2, Gazebo simulation, SLAM mapping, and Nav2 autonomous navigation.

## Project Overview

CANDI Rover (Compact Autonomous Navigating Delivery Intelligence) is an autonomous desktop delivery system developed as the final project for EECE5554 - Sensing and Navigation at Northeastern University. The rover autonomously navigates desktop environments to deliver candy, demonstrating key robotics concepts including SLAM, path planning, and obstacle avoidance.


### Key Capabilities
- **Autonomous Navigation**: Navigate complex desktop environments using Nav2 stack
- **Real-time Mapping**: Generate 2D occupancy maps using SLAM with LiDAR data
- **Obstacle Avoidance**: Dynamic Window Approach (DWA) for real-time collision avoidance
- **Sensor Fusion**: Integration of LiDAR scans and camera data for environmental awareness

## Features

- ✅ Custom URDF model converted from Fusion360 CAD design
- ✅ Full Gazebo simulation environment
- ✅ SLAM-based mapping with LiDAR
- ✅ Autonomous navigation with global and local planning
- ✅ Multi-layer costmap generation (static, obstacle, inflation)
- ✅ Teleoperation support for manual control
- 🔄 Camera integration (in progress)
- 🔄 Enhanced PID tuning for smoother motion

## Prerequisites

```bash
# Ubuntu 22.04 LTS
# ROS2 Humble
# Gazebo 11
# Python 3.8+
```

## Repository Structure

```
CANDI-Rover/
├── final_project_description/  # Main ROS2 package
│   ├── config/                 # Configuration files
│   ├── launch/                 # ROS2 launch files
│   ├── meshes/                 # 3D CAD models (STL/DAE)
│   ├── resource/               # Package resources
│   ├── urdf/                   # Robot description files
│   ├── package.xml             # ROS2 package dependencies
│   ├── setup.py                # Python package setup
│   └── setup.cfg               # Setup configuration
├── docs/                       # Documentation
│   └── CANDI_Final_Project_Presentation.pdf
├── videos/                     # Demo videos
│   ├── simulation_demo.mp4
│   └── navigation_demo.mp4
├── images/                     # Screenshots and diagrams
├── .gitignore
├── LICENSE
└── README.md
```

## Technical Details

### URDF Files
- `.xacro`: Macros and variables for rover description
- `.trans`: Coordinate frame transformations
- `.gazebo`: Simulation elements (physics, dynamics, sensors)

### Navigation Stack
- **Global Planner**: Long-range path planning using global map
- **Local Planner**: Dynamic Window Approach for obstacle avoidance
- **Costmap Layers**:
  - Static Layer: From SLAM-generated map
  - Obstacle Layer: Real-time LiDAR detection
  - Inflation Layer: Safety radius around obstacles


## Resources & References

- [Automatic Addison - ROS2 Navigation Tuning Guide](https://automaticaddison.com/ros-2-navigation-tuning-guide-nav2/)
- [Yahboom ROS Master Repository](https://github.com/automaticaddison/yahboom_rosmaster/tree/main)
- [Fusion360 to URDF Converter](https://github.com/runtimerobotics/fusion360-urdf-ros2)
- [ROS2 Documentation](https://docs.ros.org/en/humble/)
- [Nav2 Documentation](https://navigation.ros.org/)


## Course Information

**Course**: EECE 5554 - Sensing and Navigation  
**Institution**: Northeastern University  
**Program**: Master's in Robotics  
**Semester**: Fall 2024

## Contact

**Meet Brahmbhatt**
- Email: brahmbhatt.me@northeastern.edu
