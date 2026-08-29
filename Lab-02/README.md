# Lab 02 — File Upload and Command Execution Security Assessment

This repository folder contains the submission materials for Lab 02 of Offensive Security Operations I (CIP-A104).

The lab focused on assessing client/server file upload validation, filename and storage handling, and command-execution trust boundaries in DVWA and OWASP Mutillidae II, using harmless marker files and minimal-impact, non-destructive command-execution proofs. Insecure and stronger security modes were compared for both vulnerability classes.

## Files

```
Lab-02/
├── README.md
├── lab-02.pdf
├── dvwa_requests.txt
├── mutillidae_requests.txt
└── marker_hashes.txt
```

- **lab-02.pdf** — Complete Lab 02 investigation report, including methodology, evidence, analysis, security-level comparison, remediation recommendations, and conclusions.
- **dvwa_requests.txt** — Raw request/response captures for DVWA: baseline upload, mismatch upload, storage check, command injection baseline, minimal execution proof, and the Security: High retest.
- **mutillidae_requests.txt** — Raw request/response captures for Mutillidae: baseline upload, mismatch upload, storage check, command injection baseline, minimal execution proof, and the Security Level 5 retest.
- **marker_hashes.txt** — SHA-256 hashes, sizes, and detected types of all harmless marker files used for upload testing.

## Scope

All testing was performed exclusively against locally installed and isolated training instances of:

- DVWA — `http://127.0.0.1:42001/`
- OWASP Mutillidae II — `http://127.0.0.1:42002/`

No public, production, third-party, or otherwise out-of-scope systems were tested. No executable payloads, reverse shells, or destructive commands were used at any point.

## Key Activities

- Preparation and hashing of harmless upload markers
- Baseline upload testing on both applications
- Content/extension mismatch testing and validation-enforcement analysis
- Storage-location and web-accessibility assessment
- Command-execution baseline capture on both applications
- Minimal, non-destructive command-execution proof (`whoami`)
- Impact assessment (observed vs. potential)
- Security-level/mode comparison and retest (DVWA High, Mutillidae Level 5)
- Root-cause remediation recommendations
- Cleanup and restoration to baseline

## Academic Integrity

All requests, responses, screenshots, tool output, observations, and conclusions submitted for this lab were produced as part of individual practical work within the authorised training environment.

**Authorised training environment only.**
