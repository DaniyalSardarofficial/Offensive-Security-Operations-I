# Offensive Security Operations I

Practical lab work for the **ICDFA Ethical Hacking Internship Training Program**. This repository documents hands-on exercises in offensive security, written up lab by lab so the process, the commands, and the lessons are easy to follow and revisit.

![Program](https://img.shields.io/badge/Program-ICDFA%20Ethical%20Hacking%20Internship-blue)
![Focus](https://img.shields.io/badge/Focus-Offensive%20Security-red)
![Labs](https://img.shields.io/badge/Labs-1%20and%20counting-orange)
![Purpose](https://img.shields.io/badge/Purpose-Educational-green)

---

## Table of Contents

- [Overview](#overview)
- [Lab Index](#lab-index)
- [Repository Structure](#repository-structure)
- [Lab Methodology](#lab-methodology)
- [Lab Environment](#lab-environment)
- [Legal and Ethical Notice](#legal-and-ethical-notice)
- [How to Use This Repository](#how-to-use-this-repository)
- [Author](#author)
- [Disclaimer](#disclaimer)

---

## Overview

Ethical hacking means testing systems the way an attacker would, but with permission and with the goal of making them safer. This repository collects the practical side of that training: each lab is a self-contained exercise carried out in a controlled environment, with the steps and findings recorded.

It serves two purposes:

- A learning log of the skills built during the internship.
- A reference for anyone starting out in penetration testing and red team fundamentals.

---

## Lab Index

| Lab | Folder | Status |
|-----|--------|--------|
| Lab 01 | [Lab-01](./Lab-01) | Completed |

New labs are added as the program moves forward.

---

## Repository Structure

```text
Offensive-Security-Operations-I/
├── Lab-01/
│   └── ...
└── README.md
```

Each lab lives in its own folder named `Lab-XX`, so the repo stays tidy as it grows.

---

## Lab Methodology

Every lab follows the same general flow, which mirrors a real penetration test:

1. **Objective**: what the lab is meant to teach or prove.
2. **Reconnaissance**: gathering information about the target.
3. **Scanning and enumeration**: finding open ports, services, and weak points.
4. **Exploitation**: using a weakness to gain access, in a lab setting only.
5. **Post-exploitation**: understanding what access means in practice.
6. **Findings and mitigation**: what went wrong on the target and how to fix it.

---

## Lab Environment

All work is done in an isolated, intentionally vulnerable environment built for practice, such as virtual machines on a private network. Nothing here targets real systems, real organizations, or real people.

---

## Legal and Ethical Notice

Hacking without permission is illegal. The techniques shown here must only be used:

- On systems you own.
- On systems where you have clear, written permission to test.
- Inside lab environments built for practice.

Use these skills to defend and to learn. Never use them to harm.

---

## How to Use This Repository

1. Clone the repo:
   ```bash
   git clone https://github.com/DaniyalSardarofficial/Offensive-Security-Operations-I.git
   cd Offensive-Security-Operations-I
   ```
2. Open a lab folder and read through it in order.
3. Recreate the exercise in your own isolated lab to learn by doing.

---

## Author

**Daniyal Sardar**
GitHub: [@DaniyalSardarofficial](https://github.com/DaniyalSardarofficial)

Questions, corrections, and suggestions are welcome. Open an [issue](https://github.com/DaniyalSardarofficial/Offensive-Security-Operations-I/issues) to get in touch.

---

## Disclaimer

This repository is for **educational purposes only**. The author is not responsible for any misuse of the information provided. You are fully responsible for following the laws that apply where you live.
