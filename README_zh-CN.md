# TIRT-Gazebo-Simple-ROS2

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Ubuntu:Focal](https://img.shields.io/badge/Ubuntu-Focal-brightgreen)](https://releases.ubuntu.com/focal/)
[![ROS:Foxy](https://img.shields.io/badge/ROS-Foxy-blue)](https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html)

<kbd> <br> [English][en] <br> </kbd>
<kbd> <br> 简体中文 <br> </kbd>
<kbd> <br> [繁體中文][zh-TW] <br> </kbd>

[en]: README.md
[zh-TW]: README_zh-TW.md

“tirt_gazebo_ros2” ROS2 软件包旨在为 TIRT 智慧服务竞赛 - 送餐机器人组提供简便的仿真验证工具。

## 软件依赖

- Gazebo
   ```
   sudo apt-get install gazebo11 && sudo apt-get install libgazebo11-dev
   ```
- Turtlebot3
   ```
   sudo apt-get install ros-foxy-turtlebot3*
   ```

## 安装并构建

1. 导航至您的 catkin 工作空间内的「src」目录：
   ```
   cd ~/dev_ws/src
   ```
2. 从 GitHub 克隆 tirt_gazebo_ros2 包至本地端：
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple-ROS2.git tirt_gazebo_ros2
   ```
3. 构建 tirt_gazebo_ros2 包：
   ```
   cd ~/dev_ws && colcon build --symlink-install
   ```
4. 包环境设置：
   ```
   source ./install/setup.bash
   ```

## 使用方法

通过修改以下参数可以进行调整：

| 参数名称 | 数据类型 | 详细信息                                       |
| -------- | -------- | ---------------------------------------------- |
| model    | 字符串   | 设置Turtlebot3机器人模型。 <br/>默认值：`null` |

1. 添加永久性工作空间环境变量：

   注：「{TURTLEBOT3_MODEL}」代表所使用的模型名称：「burger」、「waffle」或「waffle_pi」。
   ```
   echo "export TURTLEBOT3_MODEL={TURTLEBOT3_MODEL}" >> ~/.bashrc
   ```
   ```
   source ~/.bashrc
   ```
2. 启动仿真世界：
   ```
   ros2 launch tirt_gazebo_ros2 turtlebot3_tirt.launch.py
   ```
   
## 参考资料

- Install Gazebo using Ubuntu packages (https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
- TurtleBot3 Simulation (https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)
- TIRT (https://www.tirtpointsrace.org/)
