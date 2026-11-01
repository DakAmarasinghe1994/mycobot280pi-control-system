# MyCobot280Pi Control System

Modular ROS 2 interfaces for controlling a myCobot 280 Pi
six-degree-of-freedom collaborative robot and its virtual model
using joint-space and Cartesian commands.

## Project Overview

This project combines robot-control software, hardware-platform
migration, UART communication, inverse kinematics, and RViz visualization.

I developed separate ROS 2 subsystems for controlling the physical robot
and its virtual model. Users can issue commands through an integrated
GUI or script-based ROS 2 interfaces.

The physical control platform evolved from the onboard Raspberry Pi
to an external PC and later an NVIDIA Jetson Orin Nano.

## My Contributions

- Programmed and controlled the myCobot 280 Pi collaborative robot.
- Upgraded the onboard computer from Raspberry Pi 4B to Raspberry Pi 5.
- Established external PC control through a CH340 USB-to-TTL
  connection to the robot's auxiliary ESP32 controller.
- Migrated external control to an NVIDIA Jetson Orin Nano.
- Implemented an Arduino Uno UART bridge when the Jetson did not
  recognize the CH340 converter.
- Developed modular ROS 2 interfaces for independent physical-robot
  and virtual-model control.
- Implemented joint-space and Cartesian command interfaces.
- Connected a pre-existing virtual-controller GUI through dedicated
  ROS 2 interfaces and launch configurations.
- Developed script-driven command publishers and launch configurations.
- Implemented a MoveIt 2 inverse-kinematics client for virtual-model
  joint targets and RViz visualization.
- Refined algorithms, parameters, and command execution to improve
  motion behavior and control responsiveness.

## Hardware and Control-Platform Evolution

1. Original myCobot 280 Pi with onboard Raspberry Pi 4B.
2. Onboard upgrade to Raspberry Pi 5.
3. External PC control through CH340 USB-to-TTL communication.
4. External NVIDIA Jetson Orin Nano control through an Arduino Uno
   UART bridge connected to the auxiliary ESP32 controller.

## Physical Robot Control

Developed ROS 2 interfaces that translate joint-space or Cartesian
commands into physical robot-control operations.

The hardware interface supports UART communication between the
external control computer and the robot's auxiliary controller.

## Virtual Robot Control

Developed a separate command path for the virtual robot model.

The MoveIt 2 inverse-kinematics client converts requested Cartesian
poses into joint-space targets for virtual-model control and
visualization in RViz.

Physical-robot control and virtual-model control are independent
subsystems; virtual commands should not be assumed to move the
physical robot automatically.

## GUI and Script-Based Commands

### GUI Integration

Integrated a pre-existing controller GUI by developing ROS 2
interfaces and launch configurations.

Interactive sliders allow users to specify joint angles or
end-effector poses, including position, roll, pitch, and yaw.

### Script-Based Interfaces

Developed ROS 2 nodes and launch configurations that allow users
to define joint-space or Cartesian targets in scripts and publish
them to the relevant control subsystem.

## Technologies and Hardware

**Software:** ROS 2, Linux, Python, MoveIt 2, RViz,
robot-model descriptions, and serial communication

**Hardware:** myCobot 280 Pi, Raspberry Pi 4B, Raspberry Pi 5,
external PC, NVIDIA Jetson Orin Nano, Arduino Uno,
CH340 USB-to-TTL converter, and auxiliary ESP32 controller

## Project Documentation

- [View Project Portfolio](./Dak-Amarasinghe-MyCobot-Control-Portfolio.pdf)
- [View Detailed Project Description](./MyCobot280Pi-Control-System-Project-Description.pdf)

The documents explain the platform evolution, software architecture,
control interfaces, communication setup, and RViz demonstrations.

## Engineering Skills Demonstrated

ROS 2 Software Development • Robot Control • Joint-Space Commands •
Cartesian Commands • Inverse Kinematics • GUI Integration •
UART Communication • Embedded Interfaces • Hardware Troubleshooting •
RViz Visualization • System Integration

## Contributions and Attribution

My contributions include the custom ROS 2 interfaces, command
publishers, launch configurations, hardware communication integration,
and MoveIt 2 inverse-kinematics client.

The controller GUI and underlying robotics libraries are existing
components integrated into the system.

## Author

**Dakshitha (Dak) Amarasinghe**

[GitHub Portfolio](https://github.com/DakAmarasinghe1994) |
[LinkedIn](https://www.linkedin.com/in/dak-amarasinghe-946aa71b1/)
