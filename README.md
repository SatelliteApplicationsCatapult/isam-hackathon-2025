# isam-hackathon-2025
IASM Hackathon 2025 template code.

Single-arm UR10e with Robotiq gripper and Gazebo simulated world.

Uses code from the following sources:

- ur_description
    - https://github.com/UniversalRobots/Universal_Robots_ROS2_Description/tree/humble
    -   Contains the robot description URDF and related files

- ur_moveit_config
    - https://github.com/UniversalRobots/Universal_Robots_ROS2_Driver/tree/humble/ur_moveit_config
    - Contains MoveIt SRDF config files

- robotiq_description
    - https://github.com/PickNikRobotics/ros2_robotiq_gripper/tree/humble/robotiq_description
    - Contains the gripper description URDF and related files

- ur_simulation_gazebo
    - https://github.com/UniversalRobots/Universal_Robots_ROS2_Gazebo_Simulation/tree/humble/ur_simulation_gazebo
    - Gazebo simulation setup for UR


## Setup Instructions

```bash
# Navigate to your ROS2 workspace

# Build:
colcon build --packages-select custom_ur_description custom_ur_moveit_config custom_robotiq_description isam_hackathon_2025_main

# Source:
source install/setup.bash
source /usr/share/gazebo/setup.bash

# Run:
ros2 launch isam_hackathon_2025_main custom_ur_sim_moveit.launch.py
```
