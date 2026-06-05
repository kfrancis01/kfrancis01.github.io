---
layout: default
title: Adaptive Gamification for Dementia Care
---

# Adaptive Gamification for Dementia Care
**WPI RoboCare Lab | 2024 – Present**

[← Back to Projects](/)

---

## Overview

Designed and built a modular autonomous engagement system for the Pepper humanoid robot to promote physical activity in older adults with dementia. The system uses real-time computer vision, LLM-driven adaptive dialogue, and motion-gated gameplay to create personalized exercise interactions that adapt to each patient's physical capabilities.

---

## Problem

Physical inactivity is a significant challenge in dementia care. Existing robotic engagement systems used static, scripted interactions that couldn't adapt to individual patient behavior or real-time movement variability. This limits their therapeutic effectiveness in a population where cognitive and physical capacity varies significantly between sessions and individuals.

---

## System Architecture

The system is built around three loosely coupled layers coordinated through ZMQ pub/sub messaging:

### Perception Layer
- MediaPipe-based skeletal pose estimation for real-time wrist and shoulder tracking
- Visibility thresholding and coordinate normalization relative to patient shoulder position
- Frame smoothing to reduce noise in landmark detection

### Decision Layer
- LLM-driven adaptive dialogue via ChatGPT API
- Context-aware response generation based on patient movement and game state
- Natural language interaction that adjusts encouragement and instruction in real time

### Actuation Layer
- Touchscreen game interface running locally on Pepper
- Physical movement detected by Pepper's cameras directly gates game progression
- Game does not advance until the desired motion is detected and validated

---

## Game Modes

Each game mode targets different movement patterns relevant to upper body physical therapy:

| Game | Target Movement | Therapeutic Goal |
|------|----------------|-----------------|
| Apple Picking | Upward reach | Shoulder flexion |
| Window Washing | Circular arm motion | Shoulder rotation |
| Marching | Alternating arm swing | Bilateral coordination |

---

## Technical Evolution

A previous iteration used dockerized ROS2 communication to integrate browser-based graphics controlled by MediaPipe tracking on an external machine. This architecture was restructured into a self-contained system running locally on Pepper, with ZMQ pub/sub messaging replacing the ROS2 communication layer — improving deployment reliability and reducing external dependencies.

---

## Key Engineering Challenges

**Stable cross-layer communication** — maintaining reliable data flow across three loosely coupled layers while preserving the ability to modify each independently required careful interface design. Pose landmark data required smoothing, visibility thresholding, and coordinate normalization before it could reliably gate game progression.

**Motion-gating interface design** — the boundary between the perception layer and game logic layer required particularly careful design so that changes to the tracking pipeline did not cascade into game behavior and vice versa.

**Constrained embedded platform** — the system needed to support real-time closed-loop human-robot interaction combining computer vision, natural language generation, and physical actuation simultaneously on Pepper's limited onboard compute.

---

## Results

- Successfully demonstrated real-time closed-loop HRI on a constrained embedded platform
- Modular architecture enables independent validation and modification of each layer
- Deployable platform for SAR-based exercise engagement research in dementia care settings

---

## Presentations

- **NHCGNE Annual Conference (2025)** — *Adaptive Gamified Robotic Interventions for Mitigating Physical Inactivity Among Persons with Dementia* — Virtual Podium Presentation
- **MassITC Conference** — Live Demo: Adaptive Gamification in Dementia Care

---

## Stack

Python | Docker | ZMQ | MediaPipe | ChatGPT API | JavaScript | React | Pepper SDK
