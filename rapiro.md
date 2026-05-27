---
layout: default
title: Rapiro Social Robot Interface
---

# Rapiro Social Robot Interface
**UTK Research | 2017 – 2019**

[← Back to Projects](/)

---

## Overview

Built a Bluetooth communication and data-sharing interface on Raspberry Pi 3 for a social robot used in pediatric speech therapy research. The system enabled simultaneous control of the robot's physical actions and verbal output, supporting a study investigating whether children respond differently to feedback delivered by a human versus a social robot.

---

## Research Context

The study examined human-computer interaction in a therapeutic setting — specifically whether the delivery mechanism of feedback (human vs robot) affects motor learning outcomes in children. Subjects attempted to hit an unseen target distance using a roller ball, receiving identical feedback from either a human experimenter or the Rapiro robot.

This research contributed to understanding how social robots can be effectively deployed in therapeutic contexts — an early exploration of the human-machine teaming challenges that define modern social robotics.

---

## System Architecture

**Hardware:**
- Rapiro humanoid robot — programmable DIY robot kit
- Raspberry Pi 3 B — primary controller
- Android smartphone — visual and audio interface

**Communication:**
- Bluetooth connection between Raspberry Pi and Android phone
- Serial communication for command transmission
- Real-time and pre-programmed control modes

**Software:**
- Python control scripts on Raspberry Pi
- Android application built with MIT App Inventor
- Pre-programmed phrase library for robot verbal output
- Real-time command input via terminal

---

## Implementation

The system enabled the experimenter to:
- Input desired robot speech through the Raspberry Pi terminal
- Transmit commands via Bluetooth to the Android phone
- Trigger pre-programmed physical Rapiro movements synchronized with verbal output
- Switch between real-time and pre-programmed control modes

This created a seamless interaction experience where the robot appeared to naturally respond to the subject's performance — matching the human experimenter condition for experimental validity.

---

## Future Enhancements Proposed

The research identified several directions for expanding the system:

- **Object detection** using TensorFlow and OpenCV on Raspberry Pi for eye contact simulation
- **Full autonomy** using Sharp distance sensors on Arduino to calculate puck distance and trigger appropriate Rapiro responses automatically
- **Bluetooth module** on Arduino for wireless data transmission to Raspberry Pi

---

## Publication

*The Comparison of Verbalized Feedback in Human to Computer Interfacing Versus Human to Human Interaction*
University of Tennessee, Mechanical, Aerospace, Biomedical Engineering Department, 2019
[View Publication](https://trace.tennessee.edu/handle/20.500.14382/53075)

---

## Stack

Python | Raspberry Pi 3 | Bluetooth | Android | MIT App Inventor | Rapiro SDK | Arduino
