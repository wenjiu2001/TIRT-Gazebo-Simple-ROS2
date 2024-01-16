# TIRT-Gazebo-Simple-ROS2

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Ubuntu:Focal](https://img.shields.io/badge/Ubuntu-Focal-brightgreen)](https://releases.ubuntu.com/focal/)
[![ROS:Foxy](https://img.shields.io/badge/ROS-Foxy-blue)](https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html)

<kbd> <br> English <br> </kbd>
<kbd> <br> [简体中文][zh-CN] <br> </kbd>
<kbd> <br> [繁體中文][zh-TW] <br> </kbd>

[zh-CN]: README_zh-CN.md
[zh-TW]: README_zh-TW.md

The "tirt_gazebo_ros2" ROS2 package is crafted with the objective of facilitating uncomplicated simulation validation for the TIRT Intelligent Service Competition - Food Runner Robots.

## Requirements

- Gazebo
   ```
   sudo apt-get install gazebo11 && sudo apt-get install libgazebo11-dev
   ```
- Turtlebot3
   ```
   sudo apt-get install ros-foxy-turtlebot3*
   ```

## Install and Build

1. Navigating to the "src" directory within your catkin workspace :
   ```
   cd ~/dev_ws/src
   ```
2. Clone tirt_gazebo_ros2 package for github :
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple-ROS2.git tirt_gazebo_ros2
   ```
3. Build tirt_gazebo_ros2 package :
   ```
   cd ~/dev_ws && colcon build --symlink-install
   ```
4. Package environment setup :
   ```
   source ./install/setup.bash
   ```

## How to Use

Adjustments can be made by modifying the following parameters:

| Parameter name | Data Type | Detail                                                            |
| -------------- | --------- | ----------------------------------------------------------------- |
| model          | string    | Set the Turtlebot3 robot model. <br/>default: `null`              |

1. Add permanent workspace environment variables :

   Note: "{TURTLEBOT3_MODEL}" represents the name of the utilized models: "burger", "waffle", or "waffle_pi".
   ```
   echo "export TURTLEBOT3_MODEL={TURTLEBOT3_MODEL}" >> ~/.bashrc
   ```
   ```
   source ~/.bashrc
   ```
2. Launch Simulation World :
   ```
   ros2 launch tirt_gazebo_ros2 turtlebot3_tirt.launch.py
   ```
   
## References

- Install Gazebo using Ubuntu packages (https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
- TurtleBot3 Simulation (https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)
- TIRT (https://www.tirtpointsrace.org/)
