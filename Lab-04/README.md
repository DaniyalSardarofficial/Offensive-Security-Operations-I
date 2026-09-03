# Lab 04 — XSS, Session Management & Authentication Resilience Assessment

**Course:** CIP-A104 — Offensive Security Operations I
**Program:** ICDFA Ethical Hacking Internship Training Program
**Student:** Daniyal Ahmed
**Registration Number:** C11/26/EHIT/17331
**Submission Date:** 2 September 2026

## Overview

This lab assesses reflected, stored and DOM-based Cross-Site Scripting (XSS); session cookie
behaviour including rotation and logout invalidation; and a tightly bounded authentication-resilience
test, performed exclusively against a locally hosted DVWA instance and OWASP Mutillidae II v2.12.7
instance inside an isolated Kali Linux VM (VMware NAT).

- DVWA: `http://127.0.0.1:42001`
- Mutillidae: `http://127.0.0.1:42002`

No cookie theft, session hijacking, phishing overlays, credential stuffing or password spraying was
performed. All authentication testing was capped at five failed attempts against one dedicated,
non-administrative account per target, per the lab's prohibited-actions list.

## Contents

| File | Description |
|---|---|
| `lab-04.pdf` | Full assessment report — baseline mapping, XSS proofs, secure-mode retest, session lifecycle, cookie attributes, authentication resilience, comparative analysis, remediation and cleanup. |
| `dvwa_requests.txt` | Captured request/response evidence for DVWA test cases. |
| `mutillidae_requests.txt` | Captured request/response evidence for Mutillidae test cases. |
| `marker_hashes.txt` | Hash of the harmless marker string used throughout testing, for integrity verification. |

## Phases Completed

1. XSS baseline (input/output mapping) — 6 vectors across both applications
2. Reflected/DOM XSS proof — harmless marker (`<script>alert('XSS-Test')</script>`)
3. Stored XSS cross-session persistence proof
4. XSS secure-mode retest (DVWA High / Mutillidae raised security)
5. Session lifecycle — cookies pre-login, post-login, post-logout
6. Cookie attribute review (Secure, HttpOnly, SameSite, domain, path, expiry)
7. Authentication resilience — 5-attempt test per target
8. Comparative analysis — DVWA vs Mutillidae
9. Remediation and cleanup

## Key Findings

- Reflected, Stored and DOM XSS confirmed exploitable on both applications at default/low security.
- DVWA's High security setting blocks Reflected/Stored XSS via tag-stripping, but has no effect on its
  DOM XSS module, since the vulnerable client-side code is identical across security levels.
- Mutillidae does not rotate its session identifier at login (session-fixation risk); DVWA does.
- Mutillidae's session cookie is `HttpOnly: false`, combined with confirmed stored XSS — a realistic
  (but not exploited, per lab scope) cookie-theft chain.
- Neither application implements rate-limiting or lockout after repeated failed logins.

Full detail, evidence, and remediation recommendations are in `lab-04.pdf`.

## Environment

- Kali Linux VM (VMware NAT)
- DVWA (security levels: Low, High)
- OWASP Mutillidae II v2.12.7 (security levels: 0, raised)
- Burp Suite (Repeater)

## Cleanup Confirmation

All stored XSS markers were removed/reset, HTML5 Storage test entries cleared, all test sessions
(including incognito) logged out, browser profiles cleared, and test accounts confirmed unlocked
following the authentication-resilience test.
