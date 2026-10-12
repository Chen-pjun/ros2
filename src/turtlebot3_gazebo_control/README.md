# Turtlebot3 机器人 Gazebo 仿真与键盘控制

## 项目介绍

本示例使用 Gazebo 物理仿真环境，加载 Turtlebot3（Waffle 型号）机器人，并编写 Python 键盘控制节点。

核心逻辑是监听终端键盘输入，将其映射为线速度和角速度，并通过 `/cmd_vel` 话题持续发送，控制机器人在物理仿真环境中移动。

用户按下 `W`、`A`、`S`、`D` 等按键时，程序会解析对应的速度系数，封装为 `geometry_msgs/Twist` 消息类型，驱动仿真环境中的机器人执行前进、后退、转向等动作。

松开按键或按下停止键，机器人随即停止运动，达到实时闭环控制的目的。

## 运行环境

- Ubuntu 20.04 (VMware 虚拟机)
- ROS Noetic
- Python 3.8
- Gazebo 
- Turtlebot3（waffle）
### 运行成功动图
![运行成功动图]（"https://github.com/user-attachments/assets/71f535c1-828f-45bb-85b2-bde929db2038" /）

## 项目结构

```text
turtlebot3_gazebo_control/
├── launch/
│   └── gazebo_simulation.launch
├── scripts/
│   └── main.py
└── README.md