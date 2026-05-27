# Kea Francis
### Robotics Systems Engineer | MS Robotics Engineering, WPI (August 2026) | ASEP Certified

---

I'm a robotics systems engineer with 5+ years of hands-on experience in autonomous systems, hardware-software integration, and applied robotics research. My work spans large-scale warehouse robotics at Amazon Robotics, humanoid robot research at WPI's RoboCare Lab, and embedded systems engineering across multiple robotics domains.

I hold an Associate Systems Engineering Professional (ASEP) certification from INCOSE and am completing my MS in Robotics Engineering at Worcester Polytechnic Institute in August 2026.

📧 keamfrancis96@gmail.com | [LinkedIn](https://www.linkedin.com/in/kea-francis-880052156/) | [GitHub](https://github.com/kfrancis01)

---

## Featured Projects

---

### Adaptive Gamification for Dementia Care
**WPI RoboCare Lab | 2024 – Present**

Designed and built a modular autonomous engagement system for the Pepper humanoid robot to promote physical activity in older adults with dementia.

**System Architecture:**
- **Perception Layer:** MediaPipe-based skeletal pose estimation for real-time wrist and shoulder tracking
- **Decision Layer:** LLM-driven adaptive dialogue via ChatGPT API for context-aware interaction
- **Actuation Layer:** Motion-gated touchscreen game interface where detected movement gates game progression
- **Communication:** ZMQ pub/sub messaging coordinating data between loosely coupled layers

**Game modes include:** Apple picking, window washing, and marching — each requiring different movement targets evaluated in real time.

A previous iteration used dockerized ROS2 communication integrating browser-based graphics with MediaPipe tracking on an external machine, which informed the current self-contained architecture running locally on Pepper.

**Presented at:**
- NHCGNE Annual Conference 2025 — Virtual Podium Presentation
- MassITC Conference — Live Demo

**Stack:** Python | ROS2 | Docker | ZMQ | MediaPipe | ChatGPT API | JavaScript | React

---

### Autonomous Cart Diagnostic Tool
**Amazon Robotics AI via Experis | 2021 – 2022**

Built a Python SSH tool to automate access into autonomous mobile robots and retrieve diagnostic logs across a 30-60 robot fleet spanning two remote sites in Colorado and Washington.

**Problem:** Manual cart access and log retrieval was taking 2+ minutes per cart, creating bottlenecks during overnight deployments when rapid diagnosis across multiple robots was critical.

**Solution:** Automated the full SSH access and log retrieval process, reducing cart diagnostic access from 2 minutes to 10 seconds.

**Impact:** Tool was shared with and adopted by the broader engineering team after initial development for personal use during overnight deployments.

**Stack:** Python | Linux | SSH | Bash

---

### Misroute Classification System
**Amazon Robotics | 2025 – Present**

Designed and built an NLP-based ticket classification system to identify and reduce misrouted support tickets across engineering queues.

**The Problem:** Manual analysis revealed a significant percentage of support tickets were being assigned to incorrect engineering teams, causing idle queue time and extended resolution timelines. No formal methodology existed to track or quantify the problem.

**Approach:**
- Established the first formalized misroute identification methodology for the team
- Coordinated a team of 5 engineers to manually analyze thousands of tickets as training data
- Built a Python keyword scoring program using NLP entity recognition and weighted scoring
- Implemented confusion matrix validation tracking precision and accuracy
- Developed a human-in-the-loop QA process that improved precision from 60-80% to 90-96%

**Results:**
- 9-14% reduction in misrouted tickets — nearly triple the initial 5% target
- 90-96% precision with QA validation
- Foundation established for enterprise-wide automated routing

**Stack:** Python | NLP | SQL | DataGrip | Excel | Confusion Matrix Analysis

---

### Automated Diagnostic Pipeline
**Amazon Robotics | 2024 – 2025**

Developed a data pipeline that translated operational robotic failure data into structured, actionable datasets for AI research teams.

**Problem:** ML diagnostic tool outputs contained gaps that prevented research teams from efficiently retraining models — the raw failure data wasn't structured in a way that mapped to actionable training signal.

**Solution:** Built a pipeline that ingested operational failure data, classified failure modes, and generated structured datasets that research teams could directly use for model retraining.

**Impact:** Accelerated model retraining cycles and improved the quality of training signal available to AI research teams.

**Stack:** Python | Data Pipelines | SQL | Machine Learning

---

### Rapiro Social Robot Interface
**UTK Research | 2017 – 2019**

Built a Bluetooth communication and data-sharing interface on Raspberry Pi 3 for a social robot used in pediatric speech therapy research.

**Research Context:** Investigated whether children respond differently to feedback delivered by a human versus a social robot. Developed the robot control and communication system to enable the experimental setup.

**Implementation:**
- Designed Bluetooth interface between Raspberry Pi 3 and Android phone application
- Built Android app using MIT App Inventor for real-time and pre-programmed robot control
- Enabled simultaneous control of Rapiro's physical actions and verbal output through serial communication

**Published:** *The Comparison of Verbalized Feedback in Human to Computer Interfacing Versus Human to Human Interaction* — University of Tennessee, 2019

**Stack:** Python | Raspberry Pi | Bluetooth | Android | MIT App Inventor

---

## Technical Skills

| Category | Skills |
|----------|--------|
| **Languages** | Python, C/C++, SQL, Bash, MATLAB, JavaScript |
| **Robotics** | ROS2, Gazebo/RViz, OpenCV, MediaPipe, Arduino, Raspberry Pi, Particle |
| **Tools** | Docker, Linux (Ubuntu/Raspbian), JIRA, SolidWorks, Git |
| **Domains** | Autonomous Systems, Human-Robot Interaction, Fleet Diagnostics, NLP, ML |

---

## Education

**Worcester Polytechnic Institute**
MS in Robotics Engineering | Expected August 2026
*Relevant Courses: Robot Dynamics, Robot Control, ML for Robotics, Human-Robot Interaction, Systems Engineering*

**Worcester Polytechnic Institute**
Graduate Certificate in Robotics Engineering | August 2025

**University of Tennessee Knoxville**
BS in Mechanical Engineering | May 2019

---

## Certifications

- Associate Systems Engineering Professional (ASEP) | INCOSE | November 2024
- Level One Certified Airborne Ultrasound Inspector | September 2016

---

## Presentations & Demonstrations

- **NHCGNE Annual Conference (2025)** — *Adaptive Gamified Robotic Interventions for Mitigating Physical Inactivity Among Persons with Dementia* — Virtual Podium Presentation
- **MassITC Conference** — Live Demo: Adaptive Gamification in Dementia Care

---

*Last updated May 2026*
