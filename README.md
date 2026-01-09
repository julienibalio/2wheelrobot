# 🚗 Arduino Bluetooth 2WD Remote Car

This project demonstrates how to control a **2-wheel drive (2WD) car** using an Arduino and Bluetooth module.  
The car can move forward, backward, turn left/right, stop, and adjust speed levels via Bluetooth commands.

---

## 📌 Features
- 🔹 Remote control via Bluetooth (HC-05/HC-06 module)
- 🔹 2WD motor driver setup (L298N or similar)
- 🔹 10 adjustable speed levels (PWM control)
- 🔹 Commands for **Forward, Backward, Left, Right, Stop**
- 🔹 Serial feedback for debugging and monitoring

---

## 🛠️ Hardware Requirements
- Arduino Uno / Nano / Mega
- L298N Motor Driver (or equivalent)
- HC-05 / HC-06 Bluetooth Module
- 2 DC Motors + Wheels (2WD setup)
- Power supply (Battery pack)
- Jumper wires

---

## ⚡ Pin Configuration
| Component | Arduino Pin | Description |
|-----------|-------------|-------------|
| Left Motor Dir1 | 9  | Motor A direction |
| Left Motor Dir2 | 8  | Motor A direction |
| Right Motor Dir1 | 7  | Motor B direction |
| Right Motor Dir2 | 6  | Motor B direction |
| Left Motor Speed | 10 | PWM (Motor A enable) |
| Right Motor Speed | 5  | PWM (Motor B enable) |

---

## 🎮 Bluetooth Commands
| Command | Action |
|---------|--------|
| `F` | Forward |
| `B` | Backward |
| `L` | Turn Left |
| `R` | Turn Right |
| `S` | Stop |
| `1`–`9` | Speed levels 1–9 |
| `0` | Speed level 10 (max) |

---

## 📜 Code Overview
- **Movement Functions:** `forward()`, `backward()`, `turnLeft()`, `turnRight()`, `Stop()`
- **Speed Control:** `setSpeed(index)` adjusts PWM values for left/right motors
- **Bluetooth Input:** Commands are read via `Serial.read()` and mapped to actions

---

## ▶️ Getting Started
1. Upload the provided Arduino sketch to your board.
2. Pair your Bluetooth module with your phone (default password: `1234` or `0000`).
3. Use a Bluetooth terminal app to send commands (`F`, `B`, `L`, `R`, `S`, `1`–`0`).
4. Watch your car respond in real time!

---

## 📫 Author
**Julien G. Ibalio**  

---

## 🌟 Acknowledgments
This project blends **Arduino robotics** with **Bluetooth control**, making it a fun and practical way to learn about embedded systems, motor drivers, and wireless communication.
