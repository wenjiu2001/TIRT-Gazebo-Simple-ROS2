# TIRT-Gazebo-Simple-ROS2

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
![ROS](https://img.shields.io/badge/ROS-Dashing_|_Foxy_|_Humble-blue)
[![Robot](https://img.shields.io/badge/Robot-TurtleBot3-brightgreen)](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#gazebo-simulation)

<kbd> <br> [English][en] <br> </kbd>
<kbd> <br> 简体中文 <br> </kbd>
<kbd> <br> [繁體中文][zh-TW] <br> </kbd>

[en]: README.md
[zh-TW]: README_zh-TW.md

“tirt_gazebo_ros2” ROS2 软件包旨在为 TIRT 智慧服务竞赛 - 送餐机器人组提供简便的仿真验证工具。

## 安装并构建

1. 导航至您的工作空间内的「src」目录：
   ```
   cd ~/dev_ws/src
   ```
2. 从 GitHub 克隆 tirt_gazebo_ros2 包至本地端：
   ```
   sudo apt install git
   ```
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple-ROS2.git tirt_gazebo_ros2
   ```
3. 构建 tirt_gazebo_ros2 包：
   ```
   sudo apt install python3-colcon-common-extensions
   ```
   ```
   cd ~/dev_ws && colcon build --symlink-install
   ```
4. 包环境设置：
   ```
   source ./install/setup.bash
   ```

## 使用方法

1. 添加永久性工作空间环境变量：

   - Turtlebot3 模型

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
   - 重新加载.bashrc文件
     ```
     source ~/.bashrc
     ```
2. 启动仿真世界：
   ```
   ros2 launch tirt_gazebo_ros2 turtlebot3_tirt.launch.py
   ```