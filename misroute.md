---
layout: default
title: Misroute Classification System
---

# Misroute Classification System
**2025 – Present**

[← Back to Projects](/)

---

## Overview

Designed and built an NLP-based ticket classification system to identify and reduce misrouted support tickets across engineering queues. The system uses weighted keyword scoring and confusion matrix validation to automatically classify tickets, achieving 90-96% precision with a human-in-the-loop QA process — nearly tripling the initial 5% reduction target by delivering a 9-14% reduction in misrouted tickets.

---

## Problem

A significant portion of support tickets were being assigned to incorrect engineering teams, causing them to sit dormant in wrong queues before being identified and manually rerouted. This idle queue time directly extended mean time to resolution and diverted engineering resources from actual problem-solving to routing corrections.

No formal methodology existed to track or quantify the problem — teams were troubleshooting based on queue assignment alone without validating whether tickets had been correctly routed.

---

## Approach

**Phase 1 — Baseline Establishment**

Established the first formalized misroute identification methodology for the team. Coordinated a team of 5 engineers to manually analyze thousands of tickets in batches of 350, creating a validated training dataset. Implemented a QA process that reviewed and corrected manual classifications before they were used for model training.

**Phase 2 — Automated Classification**

Built a Python keyword scoring program using NLP entity recognition:
- Text preprocessing and tokenization
- Weighted keyword scoring based on technical terms and domain-specific vocabulary
- Combination keyword analysis for improved accuracy
- Integration of ticket metadata for additional signal

**Phase 3 — Validation and Refinement**

Implemented confusion matrix analysis tracking four metrics per keyword:
- True Positives — correctly identified misrouted tickets
- False Positives — incorrectly flagged tickets
- False Negatives — missed misrouted tickets
- True Negatives — correctly identified valid tickets

Precision and accuracy scores calculated per keyword set, with performance thresholds determining inclusion in the production model.

---

## Results

| Stage | Precision Range |
|-------|----------------|
| Initial manual analysis | 60-80% |
| Post-QA manual analysis | 70-100% |
| Automated without QA | ~82% average |
| Automated with QA | 90-96% |

**Misrouted ticket reduction: 9-14%** — substantially exceeding the initial 5% target.

The human-in-the-loop QA process proved critical — reducing human error rate to 5-10 tickets per 350 analyzed and consistently pushing precision into the 90-96% range.

---

## Key Findings

- QA process significantly improves precision — human validation in the training phase is essential
- Combination keyword analysis outperforms single keyword scoring for ambiguous ticket types
- Manual process established crucial baseline data that automated system could not have generated independently
- System consistently exceeds performance targets across thousands of validated tickets

---

## Future Enhancements

- Bayesian analysis integration for tickets with medium to low keyword correlation scores
- Real-time ticket analysis and routing
- Feedback mechanisms for continuous model improvement
- Enterprise-wide implementation across additional engineering teams

---

## Stack

Python | NLP | SQL | Excel | Confusion Matrix Analysis | Data Visualization
