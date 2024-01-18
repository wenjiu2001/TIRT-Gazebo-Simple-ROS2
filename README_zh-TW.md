# TIRT-Gazebo-Simple-ROS2

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
![ROS](https://img.shields.io/badge/ROS-Dashing_|_Foxy_|_Humble-blue)
[![Robot](https://img.shields.io/badge/Robot-TurtleBot3-brightgreen)](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#gazebo-simulation)

<kbd> <br> [English][en] <br> </kbd>
<kbd> <br> [简体中文][zh-CN] <br> </kbd>
<kbd> <br> 繁體中文 <br> </kbd>

[en]: README.md
[zh-CN]: README_zh-CN.md

“tirt_gazebo_ros2” ROS2 軟體套件旨在為 TIRT 智慧服務競賽 - 送餐機器人組提供簡易的模擬驗證工具。

## 安裝並建置

1. 導覽至您的工作空間內的「src」目錄：
   ```
   cd ~/dev_ws/src
   ```
2. 從 GitHub 複製 tirt_gazebo_ros2 套件至本地端：
   ```
   sudo apt install git
   ```
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple-ROS2.git tirt_gazebo_ros2
   ```
3. 建置 tirt_gazebo_ros2 套件：
   ```
   sudo apt install python3-colcon-common-extensions
   ```
   ```
   cd ~/dev_ws && colcon build --symlink-install
   ```
4. 套件環境設定：
   ```
   source ./install/setup.bash
   ```

## 使用方法

1. 新增永久性工作空間環境變量：

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
   - 重新載入.bashrc文件
     ```
     source ~/.bashrc
     ```
2. 啟動模擬世界：
   ```
   ros2 launch tirt_gazebo_ros2 turtlebot3_tirt.launch.py
   ```