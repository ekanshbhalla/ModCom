# ModCom
📘 PROJECT REPORT

Project Title

MODCOM: A Modular, Low-Cost RF Control Platform for Hands-On Embedded Systems Education


---

Team Name

MODCOM


---

Track

Hardware Track
SDG 4 – Quality Education


---

1. Abstract

MODCOM is a modular, low-cost RF-based transmitter–receiver platform designed to enable hands-on learning of embedded systems, wireless communication, and real-time control. The system consists of an Arduino UNO–based transmitter and an STM32F103 (Blue Pill)–based receiver, connected via long-range NRF24L01 PA+LNA modules. The project emphasizes modularity, precision control, safety, and reusability by incorporating a standardized 2S 18650 battery pack with BMS protection and a self-built high-precision joystick mechanism. By keeping the total system cost below ₹5,000, MODCOM makes advanced hardware concepts accessible to students, educators, and hobbyists, directly supporting Sustainable Development Goal 4 (Quality Education).


---

2. Motivation and Problem Statement

Practical education in wireless control systems, embedded firmware, and real-time hardware design is often limited by:

High cost of commercial RC transmitters and receivers

Closed-source, non-modular systems

Poor exposure to real-world RF communication and control loops

Lack of reusable and standardized power systems across projects


As a result, students rarely gain hands-on experience with professional-grade embedded architectures, sensor integration, and system-level design.


---

3. Proposed Solution

MODCOM addresses these challenges through a modular and educational hardware platform that offers:

One transmitter controlling multiple receivers

Long-range RF communication using NRF24L01 PA+LNA

Precision control via self-built gimbal-style joysticks

Real-time stabilization using an IMU and STM32 microcontroller

A reusable, standardized battery system across projects

Open, extensible, and repairable hardware design


The system is designed to be both instructional and practical, suitable for labs, workshops, and prototyping environments.


---

4. System Architecture Overview

4.1 Transmitter Unit (Arduino UNO)

The transmitter is responsible for user interaction and command generation.

Key components:

Arduino UNO microcontroller

Two DIY precision joysticks (Yaw + Throttle, Roll + Pitch)

Auxiliary tuning potentiometers

Trim buttons for fine control

Rotary encoder and OLED display for menu navigation

3-way toggle switches for mode selection

NRF24L01 PA+LNA RF module

Modular 2S 18650 battery pack with BMS


The transmitter handles input acquisition, user interface logic, packet formation, and RF transmission.


---

4.2 Receiver Unit (STM32F103 Blue Pill)

The receiver is responsible for real-time control and stabilization.

Key components:

STM32F103C8T6 (Blue Pill) microcontroller

NRF24L01 PA+LNA RF module

MPU6050 IMU (gyroscope + accelerometer)

Hardware PWM outputs for actuators

Dedicated power regulation and failsafe logic

Modular 2S 18650 battery pack with BMS


The receiver processes incoming control data, performs sensor fusion and PID stabilization, and generates precise PWM signals.


---

5. Communication Architecture

Communication between transmitter and receiver uses structured RF packets:

[Receiver ID | Control Channels | Trim Data | Mode Flags | Telemetry | Checksum]

Each receiver has a unique ID

Only the addressed receiver responds

Prevents cross-interference

Supports scalability and multi-device control



---

6. Precision Control Design

6.1 DIY Precision Joystick

Instead of low-cost joystick modules, MODCOM uses a self-built gimbal-style joystick, inspired by professional RC transmitters. Each axis uses a 10kΩ linear potentiometer, providing:

Better centering accuracy

Higher mechanical resolution

Adjustable tension

Easy repair and calibration


This design also enhances educational value by combining mechanical and electronic learning.


---

6.2 Trims and Auxiliary Controls

Trim buttons allow fine adjustment of joystick centers

Auxiliary potentiometers allow real-time sensitivity and gain tuning

All adjustments can be visualized and modified via the OLED interface



---

7. Stability and Control System

The receiver integrates an MPU6050 IMU for stabilization:

Roll, pitch, and yaw data acquisition

PID-based control loop running on STM32 hardware timers

Adjustable PID parameters from the transmitter

Option to enable or disable stabilization dynamically


This demonstrates real-world control theory implementation.


---

8. Modular Battery System

A key design innovation in MODCOM is the standardized modular battery system:

2× 18650 Li-ion cells (2S configuration)

2S BMS for overcharge, over-discharge, and short-circuit protection

Custom connector and 3D-printed battery enclosure

Universal dock design for reuse across multiple projects


This reduces cost, improves safety, and supports sustainable hardware practices.


---

9. Safety and Reliability Considerations

Dedicated 3.3V regulation for RF modules

Bulk and bypass capacitors to prevent voltage dips

Failsafe logic on signal loss (neutral controls, throttle cut)

Physical power switches for safe operation

Modular wiring and protected enclosures



---

10. SDG Alignment – SDG 4: Quality Education

MODCOM directly contributes to SDG 4 by:

Making advanced embedded systems affordable

Enabling hands-on RF, control, and firmware learning

Encouraging open-source, modular hardware design

Supporting experimentation, repair, and reuse

Reducing dependency on expensive proprietary platforms



---

11. Cost Analysis

The complete transmitter–receiver system costs approximately ₹4,800, including power, RF, control, and mechanical components. This is significantly lower than commercial alternatives while offering greater educational flexibility.


---

12. Limitations

No RF encryption in the current prototype

Limited enclosure optimization

Manual assembly required


These limitations are intentional to maintain simplicity and educational transparency.


---

13. Future Scope

Encrypted RF communication

STM32-based transmitter

Custom PCB design

Advanced sensor fusion

Multi-receiver and swarm control

Open-source curriculum integration



---

14. Conclusion

MODCOM demonstrates that professional-grade wireless control systems can be built affordably, modularly, and safely using open-source hardware. By combining precision control, real-time embedded processing, and reusable power design, the project serves as a powerful educational platform for future engineers while remaining practical and scalable.


---

15. References

Arduino Documentation
STM32F103 Reference Manual
NRF24L01+ Datasheet
MPU6050 Datasheet
chatgpt
gemini
