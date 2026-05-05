# 🐞 Rover-Compatible End Effector for Autonomous Spotted Lanternfly Removal

![Status](https://img.shields.io/badge/status-Completed-brightgreen)
![Course](https://img.shields.io/badge/course-MAE%202250-blue)
![Institution](https://img.shields.io/badge/Cornell-University-red)
![Build](https://img.shields.io/badge/build-Prototype-orange)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

---

## 📸 Project Preview

![Prototype Overview](images/prototype_main.jpg)
*Main prototype of the rover-compatible gripper*

---

## 📌 Overview

This project presents a **lightweight, rover-compatible robotic end effector** designed to remove **spotted lanternflies** directly from vineyard environments.

While modern agricultural robots excel at navigation and monitoring, they lack the ability to **physically interact with pests**. This system fills that gap with a compliant, adaptable gripping mechanism.

---

## 🎯 Key Features

- 🔧 **4 Degrees of Freedom (DOF)**
  - Gripping
  - Telescoping
  - Wrist bending
  - Wrist rotation  

- 🤖 **Rover-compatible design**
- 🪶 **Lightweight and low-cost (~$164)**
- 🧠 **GUI-controlled via Python + ESP32**
- 🫱 **Compliant gripping (mesh + foam paddles)**

---

## 🖼️ System Architecture

![System Diagram](images/system_diagram.png)
*Control and hardware architecture*

### Control Stack
- **Microcontroller:** ESP32-S3  
- **Servo Driver:** PCA9685  
- **Interface:** Python GUI (serial communication)

---

## ⚙️ Mechanical Design

![Mechanism](images/mechanism.jpg)
*Three-servo linkage and guide rods*

### Design Highlights
- Servo-driven linkage (no ball screw)
- Stainless steel guide rods
- PTFE washers for reduced friction
- Modular, serviceable assembly

---

## 🦾 Gripper Design

![Gripper Closeup](images/gripper.jpg)
*Compliant mesh paddle system*

### Innovation
- Mesh + foam structure introduces **passive compliance**
- Improves:
  - Grip stability
  - Shape adaptability
  - Handling of fragile targets

---

## 🧪 Testing & Results

![Testing Setup](images/testing.jpg)
*Benchtop testing configuration*

### Strength Testing

| Object | Mass | Static | Dynamic | Result |
|--------|------|--------|---------|--------|
| Washer | 0.5 g | ✅ | ✅ | Stable |
| Hex Nut | 2 g | ✅ | ✅ | Easy pickup |
| Eraser | 4 g | ✅ | ✅ | Most stable |
| Screw | 14 g | ✅ | ✅ | Slight instability |
| Keys | 46 g | ✅ | ❌ | Failed dynamically |

---

### Motion Performance

| Motion | Goal | Result |
|--------|------|--------|
| Wrist Rotation | 180° | 270° |
| Wrist Bend | ±45° | ±90° |
| Paddle Opening | 40 mm | 80 mm |
| Telescope | 25 mm | 30 mm |

---

### Speed Performance

| Motion | Average Time |
|--------|-------------|
| Paddle Close | 0.53 s |
| Telescope | 0.72 s |
| Wrist Bend | 0.96 s |

---

## 📊 Key Results

- 💪 Strength exceeded target by **10×**
- ⚡ All motions completed in **< 1 second**
- 📏 Range of motion exceeded all design goals

---

## 🚧 Limitations

- ❌ Open-loop control system  
- 👁️ No onboard vision or sensing  
- 🌱 Tested only in controlled environments  

---

## 🚀 Future Work

- 🧠 Integrate **AI-based vision**
  - Object detection
  - Pose estimation
  - Autonomous grasping  

- 🔌 Improve **rover integration**
  - Mounting interfaces
  - Power systems  

- 🛠️ Enhance **durability**
  - Field-ready materials
  - Repeatability improvements  

---

## 💰 Bill of Materials

| Component | Cost |
|----------|------|
| ESP32 | $16.39 |
| Servos | $17.99 |
| Driver Board | $13.99 |
| Power Supply | $13.90 |
| Mechanical Components | ~$100 |
| **Total** | **$164.19** |

---

## 📁 Repository Structure

```
.
├── images/              # Project images (add your own)
├── code/                # Control scripts (Python/ESP32)
├── hardware/            # CAD, schematics, drawings
├── docs/                # Reports and documentation
└── README.md
```

---

## 📚 References

- Penn State Extension – Spotted Lanternfly Guide  
- SARE Project GNE22-288  
- Rutgers Plant & Pest Advisory  
- Agricultural rover platforms (Burro, Bonsai Amiga)  

---

## 👥 Team

**The Bug Busting Crew**
- Grant Corso  
- Roman Bicknell  
- Ben Hur  
- Monna Li  
- Gwendolyn Simon  

---

## 🏫 Course Info

**MAE 2250 – Engineering Design Project**  
Cornell University, Spring 2026  

---

## ⭐ Portfolio Value

This project demonstrates:

- Mechanical design & prototyping  
- Embedded systems integration  
- Mechatronics & robotics  
- Experimental testing & validation  

---

## 📬 Contact

Feel free to reach out or connect if you're interested in robotics, agriculture tech, or mechatronics!
