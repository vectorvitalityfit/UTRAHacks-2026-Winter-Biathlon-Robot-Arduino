# 🤖 Winter Biathlon Robot (UTRAHacks 2026)

Codebase for an autonomous Arduino robot designed to compete in the Winter Olympics Biathlon & Obstacle Challenge. This project prioritizes a **"Middle Pace" strategy** by balancing speed with high-torque precision to minimize penalties.

## 🏆 Key Features
* **Finite State Machine (FSM):** Modular architecture handling distinct phases (Box Pickup, Ramp Ascent, Target Logic, Obstacle Avoidance).
* **PID Control Loop:** Smooth line following implementation to maintain steady pace on "Straight" and "Curved" ramps.
* **Sensor Fusion:** Integrates Ultrasonic Color and IR sensors for robust "Perception, Reasoning, and Actuation".

## 🛠️ Hardware Stack
* **MCU:** Arduino Uno (USB-C)
* **Sensors:** Ultrasonic (HC-SR04), Color Sensor, IR Line Detectors
* **Actuators:** 2 DC Motors (Drive), 2 Servo Motors (Claw/Arm)

## 🧩 Software Architecture
The robot logic is divided into two primary execution modes based on the course split:
1. **Section 1 (Biathlon):** Color-guided navigation to center on the target rings (Blue -> Red -> Green -> Black).
2. **Section 2 (Obstacle Course):** Sonar-based interrupt logic to navigate around obstructions without wheel contact.

## 🚀 Setup & Usage
1.  Clone the repo.
2.  Calibrate `BASE_SPEED` in `config.h` based on current battery voltage (4x 9V setup)
3.  Upload `main.ino` to the Arduino Uno.
