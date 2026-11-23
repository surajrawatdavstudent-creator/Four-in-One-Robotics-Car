# Reference Projects and Research Notes

A small selection of public GitHub projects was reviewed to understand how other builders organise robot-car projects. These repositories are references for general design ideas, not proof that this project has implemented the same features.

No source code, images, circuit diagrams, or README paragraphs from these repositories have been copied into this project.

## 1. Combined line following and obstacle avoidance

**Repository:** [salvatore-arienzo/Arduino-Robot-Car-Line-Following-Obstacle-Avoidance](https://github.com/salvatore-arienzo/Arduino-Robot-Car-Line-Following-Obstacle-Avoidance)

**What was studied:** Its overview describes a robot that combines line following and obstacle avoidance on an Arduino-based platform, using separate sensing inputs and a motor-driver stage.

**Useful design lesson:** Develop each sensing behaviour separately, then define how the robot continues its path after handling an obstacle.

## 2. Basic Arduino line follower

**Repository:** [42Bots/Arduino-Line-Follower](https://github.com/42Bots/Arduino-Line-Follower)

**What was studied:** A simple Arduino Uno line-following robot using an L298N motor driver, DC geared motors, and reflective IR sensing components.

**Useful design lesson:** Start with a simple line-following system. Sensor placement and calibration matter, and a basic working mode is a better starting point than combining every feature immediately.

## 3. Wireless control with ESP32 and Arduino

**Repository:** [Rao2906/esp32-gesture-cont-4wd-car](https://github.com/Rao2906/esp32-gesture-cont-4wd-car)

**What was studied:** The README describes a transmitter/receiver arrangement in which an ESP32 reads motion-sensor input and wireless messages are used to control a vehicle through an Arduino and motor driver.

**Useful design lesson:** Separate command generation from vehicle-side control. This makes wireless communication easier to test before connecting it to the motors.

## 4. Bluetooth command-based control

**Repository:** [Nandhakumar-code/gesture-control-car-project](https://github.com/Nandhakumar-code/gesture-control-car-project)

**What was studied:** The project overview describes sending simple movement commands over a wireless connection to a vehicle-side controller.

**Useful design lesson:** A small, clearly defined command set is easier to debug than complicated control data. Stop behaviour should be part of the command design.

## 5. Modular rover design

**Repository:** [Jiayi-Pan/MarsRover](https://github.com/Jiayi-Pan/MarsRover)

**What was studied:** The project presents a rover as a modular platform with different functional modules.

**Useful design lesson:** Treat the chassis, drive system, controller, and optional features as separate modules. This supports testing and later expansion.

## Attribution and licence note

These links acknowledge the public projects consulted during research. A public GitHub repository is not automatically permission to reuse its code or media. Before adapting an implementation, check the source repository's current licence and follow its conditions. Where a repository has no clear licence, do not assume that copying or redistribution is allowed.

The architecture and wording in this repository are written for this project. Any third-party code or assets deliberately reused in the future must be documented here with the original author, source link, licence, and files or changes involved.

## Scope of this research

This is a focused sample of relevant projects, not a survey of every robotics repository on GitHub. The references were selected because they relate to one or more of the four intended capabilities.
