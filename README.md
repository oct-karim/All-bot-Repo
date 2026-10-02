

<div align="center">

# ALL-BOT 

A smart tracked robot focused on modularity and efficiency

![Hardware](https://img.shields.io/badge/Hardware-Robotics-red.svg)
![Firmware](https://img.shields.io/badge/Firmware-Python%2FROS-blue.svg)
![Status](https://img.shields.io/badge/Status-Prototype-orange.svg)

<img width="916" height="613" alt="image" src="https://github.com/user-attachments/assets/d51cf143-5784-4ecd-be88-2d1d3e1d7a11" />


</div>

## Overview

This tracked robot is designed to accomplish various tasks, ranging from a desk assistant to a mobile weather station. It is highly modular and allows mounting a robotic arm, a solar panel, or a screen on its top structure. The original microcontroller was replaced by a Raspberry Pi 4B to enable advanced capabilities like AI, computer vision, and ROS integration.

## Features
- **Pulley Transmission**: 1:4 ratio (15 teeth to 60 teeth) to drastically increase the motor torque
- **Skeleton Modular Chassis**: Lightweight and cost-effective design with an upper hexagonal grill for cooling and module mounting
- **Dual PCB Architecture**: Separation of electronics into a "Sensor Board" (logic) and a "Power Board" (power supply and drivers) to mitigate electromagnetic interference and heat buildup
- **Obstacle Avoidance**: Utilizes 3 ultrasonic sensors and a TOFsense M-S Lidar sensor (65° diagonal field of view)
- **Integrated Monitoring**: LM75C temperature sensor via I2C and a battery capacity measurement circuit

## Hardware Overview

| Component | Function |
| :--- | :--- |
| **Raspberry Pi 4B** | Main microcomputer  handling logic and sensors. |
| **NEMA 17** | Stepper motors (x2) handling track propulsion |
| **TMC2209** | Motor drivers with 1/256 microstepping capabilities |
| **TOFsense M-S** | Lidar sensor for spatial mapping and obstacle avoidance |
| **BNO055** | IMU sensor (I2C) calculating direction, position, and X/Y angles |
| **MP2307 & AMS1117** | Buck and LDO regulators stepping down the 11.1V battery to 5V and 3.3V |
| **3S Battery** | 11.1V 4200mAh LiPo battery with an XT60 connector |
