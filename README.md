# Cloud Digital Evidence Analyzer — Cloud Log Analysis & Investigation Platform

B.Tech Capstone, Computer Science & Engineering, JNTUH University College of Engineering, Hyderabad

A cloud-based digital forensics platform built to investigate cybercrime and security incidents at scale. Traditional forensic tools struggle with the volume of evidence in cloud environments, so the Digital Evidence Analyzer (DEA) moves the investigation workflow onto cloud infrastructure — evidence is centralized, ingested, and analyzed with parallel processing, and the full forensic toolkit runs against it from anywhere.

The system was deployed live, demonstrated for evaluation, and then taken down to control cloud costs.

## What It Does

- **Centralized evidence in the cloud** — Bitrix24 integrated with AWS (EC2/S3) to store and centralize cloud logs and case evidence, with automated ingestion and processing driven by Python and SQL.
- **Forensically sound acquisition** — disk imaging with FTK Imager, verified with MD5 and SHA1 checksums so evidence integrity is provable end to end.
- **Disk forensics** — Autopsy used to recover deleted data, extract file metadata, credentials, hash values, permissions, and geolocation of retrieved artifacts.
- **Memory forensics** — Volatility framework used to analyze RAM dumps and extract process artifacts (PID, PPID, threads, handles, sessions, start locations).
- **Malware analysis** — Pestudio static analysis to check target data for malware and worms before deeper investigation.
- **Secure investigation environments** — SIFT Workstation as the forensic analysis environment, Kali Linux as a supporting framework, and TAILS (amnesic live system over Tor) for secure, trace-free handling of sensitive evidence.
- **Hardware attack awareness** — a dedicated study of O.MG cable attacks (keystroke-injection charging cables), detection, and mitigations including Unified Endpoint Management (UEM) controls such as USB file-transfer restrictions.

## Investigation Workflow

1. Acquire — image the target media (in this project, a USB drive carrying corporate data) with FTK Imager.
2. Verify — tally MD5/SHA1 hashes against the image verification results.
3. Screen — run Pestudio malware checks on the target data.
4. Analyze the disk — Autopsy: deleted-file recovery, timeline, web artifacts, registry, metadata extraction.
5. Analyze memory — Volatility: process and artifact extraction from RAM captures.
6. Report — consolidate findings from the cloud workspace for the investigation report.

## Tools

| Area | Tools |
|---|---|
| Cloud & Platform | AWS (EC2, S3), Bitrix24 |
| Automation & Query | Python, SQL |
| Disk Forensics | Autopsy, FTK Imager, HxD |
| Memory Forensics | Volatility |
| Malware Analysis | Pestudio |
| Environments | SIFT Workstation, Kali Linux, TAILS |

## Repository Contents

- `docs/digital_evidence_analyzer_report.docx` — the full capstone report: literature survey, system scope and architecture, implementation walkthrough for each tool (FTK, Autopsy, SIFT, Volatility, Kali, TAILS), the O.MG cable countermeasures study, results, merits/demerits, and conclusion.

## Team

Team capstone by **Syed Abdul Malik**, **Madhurika Das Piyal**, and **M. Sai Harshith Goud**, under the guidance of **Dr. R. Sridevi**, Professor of CSE, JNTUH-UCESTH.

## Author

**Syed Abdul Malik** — B.Tech CSE, JNTUH Hyderabad · M.S. Cybersecurity, Yeshiva University
[LinkedIn](https://www.linkedin.com/in/syed-abdul-malik-5837981b8/) · [Portfolio](https://portfolio-syed.lovable.app)
