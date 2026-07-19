# Smart-Study-Assistant-Robot
FreeRTOS-based Smart Study Assistant Robot using ESP32-WROOM-DA featuring autonomous navigation, IoT dashboard, dual-core multitasking, OLED interaction, and productivity assistance.

![Platform](https://img.shields.io/badge/Platform-ESP32-blue)

![Language](https://img.shields.io/badge/Language-C++-lightpink)

![RTOS](https://img.shields.io/badge/RTOS-FreeRTOS-skyblue)

![IoT](https://img.shields.io/badge/IoT-WiFi-purple)

![License](https://img.shields.io/badge/License-MIT-lavender)



## Project Overview

The Smart Study Assistant Robot is an autonomous educational robot developed using the ESP32-WROOM-DA microcontroller. The system combines embedded systems, FreeRTOS multitasking, IoT communication, and autonomous robotics to create an interactive study companion.

The robot can navigate autonomously, avoid obstacles, detect table edges, display emotional expressions, provide Pomodoro study reminders, and be remotely controlled using a WiFi-based web dashboard.

## Features

- Autonomous Navigation

- Obstacle Avoidance

- Edge Detection

- FreeRTOS Multitasking

- Dual-Core Task Scheduling

- OLED Facial Expressions

- WiFi Web Dashboard

- Manual and Autonomous Modes

- Study Timer

- Sound Interaction

- Battery Powered

- Embedded IoT System

## Hardware Used

| Component | Quantity |
|-----------|----------|
| ESP32-WROOM-DA | 1 |
| L298N | 1 |
| HC-SR04 | 1 |
| Servo | 1 |
| IR Sensor | 2 |
| OLED | 1 |
| Sound Sensor | 1 |
| Buzzer | 1 |
| 18650 Battery | 2 |

## Software Stack

-Arduino IDE

-Embedded C++

-FreeRTOS

-HTML

-CSS

-JavaScript

-Git

-GitHub

## System Architecture

## FreeRTOS Architecture

The project implements twelve concurrent FreeRTOS tasks distributed across both ESP32 cores.

Core 0

-WiFi

-Dashboard

-Study Timer

-System Monitoring

Core 1

-Obstacle Detection

-Motor Control

-Servo

-OLED

-Navigation

-IR Detection

-Buzzer

## Installation Guide

### Software Requirements

- Arduino IDE 2.x (or later)
- ESP32 Board Package
- USB Driver (CP210x or CH340, depending on the ESP32 board)

### Required Libraries

Install the following libraries from the Arduino Library Manager:

- WiFi
- WebServer
- ESP32Servo
- Adafruit GFX
- Adafruit SSD1306
- Adafruit BusIO

### Clone the Repository

```bash
git clone https://github.com/immaculatesuganthi/Smart-Study-Assistant-Robot.git
```

### Open the Firmware

1. Launch Arduino IDE.
2. Open the `firmware` folder.
3. Open the main project file (`main.ino`).

### Configure the ESP32

Board:
ESP32 Dev Module

Flash Size:
4 MB

Upload Speed:
115200 baud

Partition Scheme:
Default

COM Port:
Select the connected ESP32 port.

### Upload the Firmware

1. Connect the ESP32 using a USB cable.
2. Click **Verify** to compile the project.
3. Click **Upload** to flash the firmware.
4. Open the Serial Monitor at **115200 baud**.

### Connect to the Robot

1. Turn on the robot.
2. Connect your phone or laptop to the robot's Wi-Fi network.
3. Open a web browser.
4. Enter the ESP32 IP address:

http://192.168.4.1

### Web Dashboard

The dashboard provides:

- Manual movement controls
- Autonomous/Manual mode selection
- Live obstacle distance
- Sound detection status
- Robot emotion display
- Study timer

### Hardware Connections

| Component | ESP32 GPIO |
|-----------|-----------:|
| Ultrasonic Trigger | GPIO 18 |
| Ultrasonic Echo | GPIO 19 |
| Servo | GPIO 13 |
| OLED SDA | GPIO 21 |
| OLED SCL | GPIO 22 |

For the complete wiring diagram, refer to:

`hardware/Circuit_Diagram.pdf`

### Verify Operation

After successful installation:

- OLED displays the startup animation.
- Robot creates a Wi-Fi access point.
- Dashboard opens successfully in a browser.
- Motors respond to manual commands.
- Autonomous mode performs obstacle avoidance.
- Study timer and buzzer operate correctly.
