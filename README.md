# MODCOM – Modular Communication & Control Platform

## Overview

MODCOM (Modular Communication & Control Platform) is a low-cost, modular, and scalable wireless communication and control system designed for education, embedded systems development, robotics, UAV experimentation, industrial monitoring, and research prototypes.

The project aims to provide a practical platform for learning RF communication, control systems, telemetry, embedded firmware development, hardware design, and system architecture while maintaining affordability and modularity.

Unlike traditional transmitter-receiver systems that are designed for a single application, MODCOM is built around a universal transmitter architecture capable of communicating with multiple uniquely addressed receivers, enabling a single control platform to operate different projects such as robotic vehicles, UAVs, automation systems, sensor nodes, and future research platforms.

---

## Key Features

* NRF24L01+ PA+LNA long-range wireless communication
* Arduino UNO based transmitter platform
* STM32F103C8T6 (Blue Pill) receiver architecture
* 8-channel control system
* OLED-based user interface
* Receiver selection and addressing system
* Real-time telemetry display
* Modular battery architecture
* Expandable firmware architecture
* Future encryption support
* Future multi-receiver networking support
* PID control and stabilization roadmap

---

## System Architecture

### Transmitter

Hardware:

* Arduino UNO
* NRF24L01+ PA+LNA Module
* 0.96" SSD1306 SPI OLED Display
* Dual Precision Gimbal Joysticks
* 8 Trim Buttons
* 2 Auxiliary B10K Potentiometers
* 2 Three-Position Switches
* Rotary Encoder with Push Button
* 2S Li-Ion Battery Pack

Functions:

* Control signal generation
* Menu navigation
* Receiver selection
* Telemetry visualization
* Configuration management

---

### Receiver

Hardware:

* STM32F103C8T6 (Blue Pill)
* NRF24L01+ PA+LNA Module
* MPU6050 6-Axis IMU
* PWM Outputs
* Power Regulation Circuitry
* 2S Li-Ion Battery Interface

Functions:

* Wireless packet reception
* Sensor acquisition
* Telemetry generation
* PWM output generation
* Future stabilization algorithms

---

## Receiver Addressing System

One of the primary goals of MODCOM is universal control.

Each receiver is assigned a unique ID.

Example:

Receiver 001 → UAV Platform

Receiver 002 → Ground Rover

Receiver 003 → Robotic Arm

Receiver 004 → Sensor Station

The transmitter can select and connect to different receivers through an onboard menu system using the rotary encoder interface.

This architecture allows a single transmitter to be reused across multiple projects.

---

## Telemetry System

Future versions of MODCOM will support:

* Battery Voltage Monitoring
* IMU Status
* Signal Quality Monitoring
* Receiver Health Monitoring
* Sensor Data Streaming
* Custom Telemetry Packets

Telemetry information will be displayed directly on the OLED interface and may later be expanded to external monitoring dashboards.

---

## Power System

The platform utilizes a modular 2S lithium-ion battery architecture:

* 2 × 18650 Li-Ion Cells
* 2S BMS Protection Circuit
* Modular Docking Interface
* Dedicated Buck Converters
* 3.3V RF Power Regulation
* Decoupling Network for RF Stability

This design allows battery packs to be reused across future projects while simplifying charging and maintenance.

---

## Applications

MODCOM is being developed as a reusable platform for:

* UAV Systems
* Robotics
* Educational Laboratories
* Industrial Monitoring
* Remote Sensing
* Research Prototypes
* Autonomous Vehicles
* Formula Student Telemetry Systems
* Embedded Systems Training

---

## Development Roadmap

### Version 1.0

* Basic NRF24 communication
* 4-channel transmission
* STM32 receiver integration

### Version 2.0

* OLED menu system
* Receiver addressing
* Configuration interface

### Version 3.0

* Telemetry support
* Sensor feedback
* Diagnostics

### Version 4.0

* PID stabilization framework
* Advanced control algorithms

### Version 5.0

* Encrypted communication
* Multi-node networking
* Expanded telemetry ecosystem

---

## Learning Objectives

This project is intended to provide practical experience in:

* Embedded Systems
* STM32 Development
* Arduino Development
* RF Communication
* Control Systems
* Sensor Integration
* Hardware Design
* Power Electronics
* Telemetry Systems
* System Architecture
* Technical Documentation

---

## Current Status

Active Development

This repository documents the complete design, development, testing, and evolution of MODCOM from concept to fully functional modular communication platform.

---

## Author

Ekansh Bhalla

Computer Science Engineering Student

Project Focus:
Embedded Systems • Wireless Communication • Robotics • Telemetry • Control Systems • Product Development
