# Lab 3 — File Inclusion and SQL Injection Security Assessment

## Overview

This lab assessed two categories of server-side input weaknesses across two intentionally
vulnerable web applications running in an isolated Kali Linux VM (VMware NAT):

- **Local/Remote File Inclusion (LFI/RFI)** — DVWA File Inclusion module and OWASP Mutillidae II's
  arbitrary-file-inclusion challenge.
- **SQL Injection** — DVWA SQL Injection module and Mutillidae's SQLi User Lookup challenge.

Testing followed the nine required hands-on phases sequentially: baseline capture, LFI validation,
RFI validation (conditional), a secure-mode comparison for file inclusion, SQL baseline, boolean/
behavioural SQLi discovery, minimal authentication/marker-data proof, a secure-mode comparison for
SQLi, and remediation planning.

Full submission details (student information, course, and assessment metadata) are on the cover
page of `lab-03.pdf`.

## Targets

| Application | URL |
|---|---|
| DVWA | `http://127.0.0.1:42001` |
| OWASP Mutillidae II | `http://127.0.0.1:42002` |

Both applications were tested exclusively inside the isolated lab VM and were never exposed publicly.

## Key Findings

- Both applications are vulnerable to LFI and SQL Injection at their default/low security settings.
- DVWA's **High** security level changes the delivery mechanism for both vulnerability classes
  (filename whitelist for LFI; session-based parameter delivery + `LIMIT 1` for SQLi) but does **not**
  fix the underlying root cause — the classic SQLi boolean injection still succeeds at High security.
- Mutillidae's **Secure (Level 5)** setting fully blocks both vulnerability classes without disclosing
  errors, consistent with genuine allow-list validation and parameterised query handling.
- Mutillidae's default/low setting also disclosed a full raw SQL error (query text, DB engine, file
  path, line number, and stack trace) on a malformed SQLi input — a standalone information-disclosure
  finding documented in the report.
- All evidence was collected using only a benign, off-application local marker file (for LFI) and the
  applications' own built-in fictional demo accounts (for SQLi) — no real secrets, credentials, or
  unrelated data were accessed at any point.

Full findings, evidence, analysis, and remediation recommendations are in `lab-03.pdf`. All request/
response evidence, the marker file hash, and the evidence register are embedded directly in the
report rather than shipped as separate raw export files.

## Repository Contents

| File | Description |
|---|---|
| `README.md` | This file |
| `lab-03.pdf` | Full assessment report — 9-phase evidence walkthrough, analysis questions, remediation table, evidence register, evidence-minimisation statement, and cleanup log |

## Methodology

Traffic was intercepted and analysed using Burp Suite Community Edition (Proxy, Intercept, Repeater,
and HTTP History). Boolean-based SQL Injection was proven by holding a base value constant and
varying only the truth value of an injected `AND` clause, observing a deterministic flip between
"record found" and "record not found" states — distinguishing genuine query-logic manipulation from
mere syntax errors. File inclusion was proven using a uniquely hashed, disposable marker file created
independently of either application.

## Cleanup

Per the lab's cleanup and restoration requirements: the local marker file was deleted, both
applications' security levels were reset to their default/low baseline, both application databases
were reset via their built-in reset functions, and no database dump files were created or retained.
Full checklist is included at the end of `lab-03.pdf`.

## Scope Note

RFI (Phase 3) was scoped out of this assessment: `allow_url_include` was not confirmed enabled in the
lab environment, and Mutillidae additionally reported a missing PHP Curl dependency required by its
remote-fetch code paths. This is documented in the report rather than forced against an unconfigured
target, per the "only if deliberately enabled" instruction in the lab brief.
