---
layout: default
title: Autonomous Robot Diagnostic Tool
---

# Autonomous Robot Diagnostic Tool
**2021 – 2022**

[← Back to Projects](/)

---

## Overview

Built a Python-based SSH diagnostic tool to streamline autonomous mobile robot diagnostics. The tool enables engineers to execute Linux commands across multiple robots sequentially without maintaining persistent shell connections — reducing diagnostic access time from over two minutes to under ten seconds.

---

## Problem

Diagnosing issues across a fleet of autonomous mobile robots required manually establishing SSH connections to each robot individually, executing diagnostic commands, and closing connections — a repetitive process that created significant bottlenecks when multiple robots needed simultaneous diagnosis during time-sensitive operations.

When operating alone across two remote sites, the time cost of manual cart-by-cart access was particularly impactful. Issues often affected multiple robots simultaneously, and slow diagnostic access meant delayed identification of fleet-wide failure patterns.

---

## Solution

Built a Python tool using the Paramiko secure shell library that automates the full SSH access and log retrieval workflow:

- Accepts cart identifier, IP address, credentials, and command as inputs
- Opens a secure shell connection
- Executes the specified Linux command
- Captures and formats output with color-coded terminal display
- Closes the connection automatically
- Supports sequential execution across multiple carts

Credentials are stored in separate modules excluded from distribution, maintaining security while enabling streamlined access.

---

## Impact

- Reduced diagnostic access time from 2+ minutes to under 10 seconds per cart
- Enabled rapid sequential diagnosis across multiple robots without maintaining persistent connections
- Tool was adopted by the broader engineering team after initial development
- Particularly valuable for overnight operations where rapid fleet-wide diagnosis was critical

---

## Technical Details

**Core Library:** Paramiko SSH implementation for secure shell access

**Key Features:**
- Automated shell connection management — opens and closes connections per command
- Color-coded output display using Colorama for improved readability
- Error capture and display separate from standard output
- Modular credential management for security

---

## Stack

Python | Paramiko | SSH | Linux | Colorama | Bash
