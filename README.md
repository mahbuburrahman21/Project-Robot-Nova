<div align="center">
  <img src="DIY robot with glowing eyes.png" width="800"/>
  <h1>Nova: Expressive Voice-Controlled Automaton</h1>
  <p>An Offline Voice-Activated Robot with Dynamic OLED Facial Expressions</p>

  <a href="https://github.com/arduino/arduino-cli">
    <img src="https://img.shields.io/badge/Framework-Arduino-00979D?style=for-the-badge&logo=arduino" alt="Framework">
  </a>
  <a href="#">
    <img src="https://img.shields.io/badge/Hardware-DF2301Q_Voice-FF6F00?style=for-the-badge" alt="Voice Module">
  </a>
   <a href="#">
    <img src="https://img.shields.io/badge/Display-SH1106_OLED-36BCF7?style=for-the-badge" alt="Display">
  </a>

---

![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=22&pause=1000&color=36BCF7&center=true&vCenter=true&width=800&lines=Speak+commands+to+trigger+movement.;Dynamic+OLED+eyes+that+react+to+moods.;Offline+voice+processing+for+instant+response.)

</div>

---

## 📖 Overview

**VoxBot** is an interactive, voice-controlled robotic platform designed to blend mobility with personality. Unlike cloud-dependent assistants, VoxBot utilizes the **DFRobot DF2301Q** module for high-speed, offline voice recognition, allowing it to respond instantly to 15+ commands.

The robot features a "Digital Soul" powered by a **SH1106 OLED display**, which renders various facial expressions—from "Sleeping" and "Sad" to "Dancing" and "Ready"—coordinated with its physical movements. Whether it's guarding its station or performing a dance, VoxBot provides a tangible example of human-robot interaction.

---

## ✨ Key Features

-   **🎙️ Offline Voice Intelligence**: Responds to specific Command IDs (CMDIDs) without needing an internet connection.
-   **👁️ Reactive Expressions**: A custom-coded graphics engine using the `U8g2` library that changes eyes and mouth shapes based on the current action.
-   **🕹️ 4-Wheel Drive Mobility**: Controlled via an L298N/L293D driver for precise Forward, Reverse, and Turning maneuvers.
-   **🎭 Animated Sequences**: Complex "Dance" and "Guard" modes that combine servo head movements, wheel-base rotation, and facial animations.
-   **⚡ Real-time Feedback**: Serial monitoring of command IDs for easy debugging and interaction logging.

---

## 📸 Facial Expressions Preview

| Normal | Happy/Dance | Sleeping | Sad |
| :---: | :---: | :---: | :---: |
| `[  ][  ]` | `(^)(^)` | `z z Z` | `( T )( T )` |
<img src="Pixel art face expressions in blue glow.png" width="800"/>

---

## 🛠️ Hardware Requirements

| Component | Qty | Notes |
| :--- | :---: | :--- |
| **Arduino Uno/Nano** | 1 | Main Controller |
| **DFRobot DF2301Q** | 1 | I2C Voice Recognition Module |
| **SH1106 OLED (128x64)** | 1 | I2C Display for Facial Expressions |
| **L298N Motor Driver** | 1 | Drives the 4 DC Motors |
| **DC Motors + Wheels** | 4 | Robot Chassis |
| **SG90 Servo Motor** | 1 | Head/Arm rotation (Pin 12) |
| **7.4V Li-ion Battery** | 1 | Power source for motors |

---

## 🔌 Wiring Diagram

| Arduino Pin | Component | Function |
| :--- | :--- | :--- |
| **`A4 (SDA)`** | OLED & Voice Module | I2C Data |
| **`A5 (SCL)`** | OLED & Voice Module | I2C Clock |
| **`D12`** | SG90 Servo | Signal Wire |
| **`D8 / D9`** | Motor Driver | Speed Control (enA / enB) |
| **`D2, D3, D4, D5`**| Motor Driver | Direction (in1, in2, in3, in4) |

---

## 🗣️ Voice Command Map

| Command ID | Voice Trigger | Action | Face Style |
| :---: | :--- | :--- | :--- |
| **5** | "Start Forward" | Moves forward + Servo sweep | Blink / Smile |
| **7** | "Reverse" | Moves backward | Normal |
| **9** | "Guard Mode" | Pivot turns + scanning | Normal |
| **12** | "Tired" | Stop all motion | Sleepy (Zzz) |
| **13** | "Dance" | Fwd/Back + Servo + Smiles | Excited |
| **16** | "Sad" | Move back slowly | Crying Eyes |

---

## 🚀 Installation

1.  **Install Libraries**:
    - `DFRobot_DF2301Q`
    - `U8g2`
    - `Servo`
2.  **Upload Code**: Open the `.ino` file in Arduino IDE, select your board, and hit upload.
3.  **Calibrate Servo**: Ensure the servo is centered at 180 degrees during assembly to allow for the code's `180 -> 105` sweep.

---

<div align="center">
  <p>Created by Md Mahbubur Rahman.</p>
</div>
