# Rover-Compatible End Effector for Autonomous Spotted Lanternfly Removal

**Team:** The Bug Busting Crew  
**Members:** Grant Corso, Roman Bicknell, Ben Hur, Monna Li, Gwendolyn Simon  
**Course:** MAE 2250  
**Institution:** Cornell University  
**Semester:** Spring 2026  

---

## Overview

This project focuses on designing a **rover-compatible end effector** capable of physically removing spotted lanternflies from vineyard environments. While existing agricultural robots excel at navigation and monitoring, they lack manipulators for direct pest removal. This work addresses that gap.

---

## Context and Problem Statement

Agricultural rovers currently support:
- Scouting
- Transport
- Row navigation  

However, they typically **lack manipulators** for real-time pest removal.

### Key Design Requirement
- Must integrate with **existing robotic platforms**
- Avoid reliance on a fully custom rover system

### Engineering Challenges
A viable field manipulator must:
- Approach irregular targets
- Conform without crushing them
- Operate with minimal actuator mass and complexity

### Design Direction
- Lightweight, servo-driven system
- Compliant gripping paddles
- Modular and adaptable architecture

---

## Final Prototype and Application

### Degrees of Freedom (DOF)
The final prototype includes **4 DOF**:
- Gripping (paddle motion)
- Telescoping extension
- Wrist bending
- Wrist rotation

### Mechanical System
- Two servos control paddle motion via sliders on stainless steel rods
- One servo enables telescoping via pivot shift
- Additional joints provide wrist articulation

### Control System
- **GUI:** Python-based interface
- **Microcontroller:** ESP32-S3
- **Driver:** PCA9685 servo controller
- **Communication:** Serial interface

### Capabilities
- Open-loop operation
- Manual or upstream robotic control
- Real-time visualization via GUI

### Potential Applications
- Pest removal (primary)
- Fruit harvesting
- Handling irregular industrial parts
- Gentle robotic manipulation tasks

---

## Testing and Results

Testing focused on:
- Strength
- Range of motion
- Speed

---

### Strength Testing

| Object     | Mass | Static Hold | Dynamic Hold | Notes |
|-----------|------|------------|-------------|------|
| Washer    | 0.5 g | Yes | Yes | Stable in all orientations |
| Hex nut   | 2 g   | Yes | Yes | Easy pickup |
| Eraser    | 4 g   | Yes | Yes | Most stable |
| Screw     | 14 g  | Yes | Yes | Less stable dynamically |
| Keys      | 46 g  | Yes | No  | Failed in dynamic motion |

---

### Motion Performance

| Motion           | Goal        | Result       | Observation |
|------------------|------------|-------------|------------|
| Wrist rotation   | 180°       | 270°        | Improved off-axis reach |
| Wrist bend       | ±45°       | ±90°        | Doubled target |
| Paddle opening   | 40 mm      | 80 mm       | Handles irregular shapes |
| Telescope travel | 25 mm      | 30 mm       | Exceeded goal |

---

### Speed Performance

| Motion         | Range (10 trials) | Average | Notes |
|---------------|------------------|--------|------|
| Paddle close  | 0.48–0.58 s      | 0.53 s | Fastest motion |
| Telescope     | 0.68–0.77 s      | 0.72 s | Consistent |
| Wrist bend    | 0.92–1.00 s      | 0.96 s | Slowest but <1s |

---

### Key Findings
- Strength exceeded **5 g target by ~10x**
- Motion range exceeded all design goals
- All actions completed in **under 1 second**

---

## Prototype and Design Details

### Mechanical Design
- Lightweight linkage system (no ball screw)
- Stainless steel guide rods
- PTFE washers to reduce friction
- Modular, serviceable assembly

### Assembly Strategy
1. Mount servos
2. Attach arm links and rods
3. Install pivot and upper linkages

---

### Control System

Components:
- ESP32-S3 devkit
- PCA9685 servo driver
- Python GUI

Features:
- Real-time geometry visualization
- Adjustable servo limits
- Pre-programmed motion demos

---

### Key Limitation
- No onboard sensing or vision
- Requires external system for:
  - Target detection
  - Grasp planning

---

### Gripper Design Innovation

**Compliant Paddle System:**
- Mesh + foam structure
- Improves:
  - Grip adaptability
  - Handling of fragile objects
  - Shape conformity

---

## Conclusion and Recommendations

### Achievements
- Met all benchtop success criteria
- Exceeded motion and speed targets
- Demonstrated strong gripping capability

### Current Limitations
- Open-loop control
- No autonomous perception
- Tested only in controlled environments

---

### Next Steps

1. **Integrate AI Vision**
2. **Improve System Integration**
3. **Enhance Durability**

---

## Bill of Materials

**Total Cost:** $164.19

---

## References

- Penn State Extension – Spotted Lanternfly Guide  
- SARE Project GNE22-288  
- Rutgers Plant & Pest Advisory  

---

## Portfolio Notes

This project demonstrates:
- Mechanical design and prototyping
- Embedded systems integration
- Mechatronics and control systems
- Experimental validation and testing
