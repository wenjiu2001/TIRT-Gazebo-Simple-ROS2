# TIRT-Gazebo-Simple-ROS2

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)
[![Ubuntu:Focal](https://img.shields.io/badge/Ubuntu-Focal-brightgreen)](https://releases.ubuntu.com/focal/)
[![ROS:Foxy](https://img.shields.io/badge/ROS-Foxy-blue)](https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html)

<kbd> <br> [English][en] <br> </kbd>
<kbd> <br> [简体中文][zh-CN] <br> </kbd>
<kbd> <br> 繁體中文 <br> </kbd>

[en]: README.md
[zh-CN]: README_zh-CN.md

“tirt_gazebo_ros2” ROS2 軟體套件旨在為 TIRT 智慧服務競賽 - 送餐機器人組提供簡易的模擬驗證工具。

## 軟體需求

- Gazebo
   ```
   sudo apt-get install gazebo11 && sudo apt-get install libgazebo11-dev
   ```
- Turtlebot3
   ```
   sudo apt-get install ros-foxy-turtlebot3*
   ```

## 安裝並建置

1. 導覽至您的工作空間內的「src」目錄：
   ```
   cd ~/dev_ws/src
   ```
2. 從 GitHub 複製 tirt_gazebo_ros2 套件至本地端：
   ```
   git clone https://github.com/wenjiu2001/TIRT-Gazebo-Simple-ROS2.git tirt_gazebo_ros2
   ```
3. 建置 tirt_gazebo_ros2 套件：
   ```
   cd ~/dev_ws && colcon build --symlink-install
   ```
4. 套件環境設定：
   ```
   source ./install/setup.bash
   ```

## 使用方法

透過修改以下參數可以進行調整：

| 參數名稱 | 資料類型 | 詳細資訊                                       |
| -------- | -------- | ---------------------------------------------- |
| model    | 字串     | 設定Turtlebot3機器人模型。 <br/>預設值：`null` |

1. 新增永久性工作空間環境變量：

   註：「{TURTLEBOT3_MODEL}」代表所使用的模型名稱：「burger」、「waffle」或「waffle_pi」。
   ```
   echo "export TURTLEBOT3_MODEL={TURTLEBOT3_MODEL}" >> ~/.bashrc
   ```
   ```
   source ~/.bashrc
   ```
2. 啟動模擬世界：
   ```
   ros2 launch tirt_gazebo_ros2 turtlebot3_tirt.launch.py
   ```
   
## 參考資料

- Install Gazebo using Ubuntu packages (https://classic.gazebosim.org/tutorials?tut=install_ubuntu)
- TurtleBot3 Simulation (https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/)
- TIRT (https://www.tirtpointsrace.org/)
