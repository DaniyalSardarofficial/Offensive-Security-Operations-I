# Offensive Security Operations I

Lab reports and evidence for the **Offensive Security Operations I** course, completed as part of the **ICDFA Ethical Hacking Internship Training Program**. Four hands-on labs are documented here, moving from discovery and enumeration through injection flaws, cross-site scripting, and session and authentication testing.

![Course](https://img.shields.io/badge/Course-Offensive%20Security%20Operations%20I-blue)
![Program](https://img.shields.io/badge/Program-ICDFA%20Ethical%20Hacking%20Internship-purple)
![Labs](https://img.shields.io/badge/Labs-4-orange)
![Purpose](https://img.shields.io/badge/Purpose-Educational-green)

---

## Table of Contents

- [Overview](#overview)
- [Lab Index](#lab-index)
- [Skills Covered](#skills-covered)
- [Repository Structure](#repository-structure)
- [Lab Methodology](#lab-methodology)
- [Lab Environment](#lab-environment)
- [Legal and Ethical Notice](#legal-and-ethical-notice)
- [How to Use This Repository](#how-to-use-this-repository)
- [Author](#author)
- [Disclaimer](#disclaimer)

---

## Overview

Ethical hacking means testing systems the way an attacker would, with permission and with the goal of making them safer. This repository is the practical record of that training. Each lab has its own folder containing a written report and the supporting evidence, so the work can be followed step by step and reviewed later.

The labs build on each other. Early work focuses on finding what a target exposes, and later work moves into exploiting common web application weaknesses and judging how well a system holds up under attack.

---

## Lab Index

| Lab | Topic | Folder |
|-----|-------|--------|
| Lab 01 | Content discovery and enumeration with Gobuster | [Lab-01](./Lab-01) |
| Lab 02 | Lab report with supporting evidence files | [Lab-02](./Lab-02) |
| Lab 03 | Local and remote file inclusion (LFI/RFI) and SQL injection assessment | [Lab-03](./Lab-03) |
| Lab 04 | Cross-site scripting (XSS), session handling, and authentication resilience | [Lab-04](./Lab-04) |

---

## Skills Covered

- Discovering hidden directories and files on a web target
- Gathering and organizing evidence during a test
- Finding and exploiting local and remote file inclusion flaws
- Testing for and exploiting SQL injection
- Identifying cross-site scripting vulnerabilities
- Assessing session management and authentication weaknesses
- Writing clear technical reports with findings and fixes

---

## Repository Structure

```text
Offensive-Security-Operations-I/
├── Lab-01/
├── Lab-02/
├── Lab-03/
├── Lab-04/
└── README.md
```

Each `Lab-XX` folder holds the report for that lab along with any evidence files, such as tool output and screenshots.

---

## Lab Methodology

Every lab follows the same flow, which mirrors a real penetration test:

1. **Objective**: what the lab is meant to teach or prove.
2. **Reconnaissance and enumeration**: finding what the target exposes.
3. **Testing and exploitation**: confirming weaknesses in a controlled setting.
4. **Evidence**: recording commands, output, and screenshots.
5. **Findings and mitigation**: explaining what went wrong and how to fix it.

---

## Lab Environment

All work was done in an isolated, intentionally vulnerable environment built for practice. Nothing in this repository targets real systems, real organizations, or real people.

---

## Legal and Ethical Notice

Testing systems without permission is illegal. The techniques documented here must only be used:

- On systems you own.
- On systems where you have clear, written permission to test.
- Inside lab environments built for practice.

Use these skills to defend and to learn. Never use them to cause harm.

---

## How to Use This Repository

1. Clone the repo:
   ```bash
   git clone https://github.com/DaniyalSardarofficial/Offensive-Security-Operations-I.git
   cd Offensive-Security-Operations-I
   ```
2. Open the labs in order, from `Lab-01` to `Lab-04`.
3. Read each report, then recreate the exercise in your own isolated lab to learn by doing.

---

## Author

**Daniyal Sardar**
GitHub: [@DaniyalSardarofficial](https://github.com/DaniyalSardarofficial)

Questions, corrections, and suggestions are welcome. Open an [issue](https://github.com/DaniyalSardarofficial/Offensive-Security-Operations-I/issues) to get in touch.

---

## Disclaimer

This repository is for **educational purposes only**. The author is not responsible for any misuse of the information provided. You are fully responsible for following the laws that apply where you live.
