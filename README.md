# TIRT-Gazebo-Simple-ROS2

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
![ROS](https://img.shields.io/badge/ROS-Dashing_|_Foxy_|_Humble-blue)
[![Robot](https://img.shields.io/badge/Robot-TurtleBot3-brightgreen)](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#gazebo-simulation)

<kbd> <br> English <br> </kbd>
<kbd> <br> [简体中文][zh-CN] <br> </kbd>
<kbd> <br> [繁體中文][zh-TW] <br> </kbd>

[zh-CN]: README_zh-CN.md
[zh-TW]: README_zh-TW.md

The "tirt_gazebo_ros2" ROS2 package is crafted with the objective of facilitating uncomplicated simulation validation for the TIRT Intelligent Service Competition - Food Runner Robots.

## Install and Build

1. Navigating to the "src" directory within your workspace :
   ```
   cd ~/dev_ws/src
   ```
2. Clone tirt_gazebo_ros2 package for github :
   ```
   sudo apt install git
   ```
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple-ROS2.git tirt_gazebo_ros2
   ```
3. Build tirt_gazebo_ros2 package :
   ```
   sudo apt install python3-colcon-common-extensions
   ```
   ```
   cd ~/dev_ws && colcon build --symlink-install
   ```
4. Package environment setup :
   ```
   source ./install/setup.bash
   ```

## How to Use

1. Add permanent workspace environment variables :

   - Turtlebot3 Model

      - Burger
        ```
        echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
        ```
      - Waffle
        ```
        echo "export TURTLEBOT3_MODEL=waffle" >> ~/.bashrc
        ```
      - Waffle Pi
        ```
        echo "export TURTLEBOT3_MODEL=waffle_pi" >> ~/.bashrc
        ```
   - Reload the .bashrc file
     ```
     source ~/.bashrc
     ```
2. Launch Simulation World :
   ```
   ros2 launch tirt_gazebo_ros2 turtlebot3_tirt.launch.py
   ```