# Lab 01 — Lab Assurance, HTTP Mapping and Attack-Surface Reconnaissance

This repository folder contains the submission materials for **Lab 01** of **Offensive Security Operations I (CIP-A104)**.

The lab focused on validating an isolated vulnerable-application environment and performing HTTP mapping, technology fingerprinting, input and cookie analysis, low-rate content discovery, and comparative attack-surface reconnaissance of **DVWA** and **OWASP Mutillidae II**.

## Files

```text
Lab-01/
├── README.md
├── lab-01.pdf
├── dvwa_gobuster.txt
└── mutillidae_gobuster.txt
```

* **lab-01.pdf** — Complete Lab 01 investigation report, including methodology, evidence, analysis, findings, and conclusions.
* **dvwa_gobuster.txt** — Raw low-rate Gobuster content-discovery output for DVWA.
* **mutillidae_gobuster.txt** — Raw low-rate Gobuster content-discovery output for OWASP Mutillidae II.

## Scope

All testing was performed exclusively against locally installed and isolated training instances of:

* DVWA — `http://127.0.0.1:42001/`
* OWASP Mutillidae II — `http://127.0.0.1:42002/`

No public, production, third-party, or otherwise out-of-scope systems were tested.

## Key Activities

* Environment and network isolation validation
* Application readiness and baseline reset
* Snapshot and rules-of-engagement verification
* HTTP GET and POST request mapping
* Cookie and input-point inventory
* Technology fingerprinting
* Low-rate content discovery with Gobuster
* Manual validation of discovered resources
* Comparative attack-surface analysis
* Cleanup and restoration to baseline

## Academic Integrity

All requests, responses, screenshots, tool output, observations, and conclusions submitted for this lab were produced as part of individual practical work within the authorised training environment.

> **Authorised training environment only.**
