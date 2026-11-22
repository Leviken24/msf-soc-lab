# SOC Home Lab — Threat Simulation, Telemetry & Detection

> **Project report and evidence repository.** This repository documents a controlled, virtualised security-monitoring lab inspired by the *Build A Basic Home Lab* series by MyDFIR.

## Important accuracy note

This repository contains technical explanations, a reporting structure, and an evidence checklist. It does **not** claim that every screenshot, alert, event, or detection described in the templates was produced in the author's environment.

The original video URL supplied for this project is **Build A Basic Home Lab (Part 3)**. A publicly available first-person write-up of the same tutorial series describes a VirtualBox environment with Kali Linux, Windows 10, Splunk, and Sysmon, and documents network setup and a controlled Meterpreter reverse-TCP demonstration. The author's exact local configuration and results must be confirmed from their own screenshots/logs before publication.

**Do not publish this repository as a completed validation of a test unless you have the corresponding evidence.** Replace every `[ADD ...]` field, remove inapplicable sections, and mark each test `PASS`, `FAIL`, or `NOT TESTED` based on observed results.

## Project objective

Build a small, isolated lab to understand the relationship between:
1. activity generated on an endpoint;
2. telemetry recorded by the operating system and Sysmon;
3. forwarding and indexing of events by a SIEM;
4. analyst review of events and potential indicators.

The lab is educational. It is not a production SOC and does not establish that a system is secure.

## Lab overview

The tutorial series is associated with the following core components:

| Component | Role | Evidence to add |
|---|---|---|
| Kali Linux VM | Controlled test/attacker workstation | Screenshot of VM and its lab IP |
| Windows 10 VM | Test endpoint | Screenshot of VM and its lab IP |
| Splunk | SIEM/search and analysis platform in the tutorial series | Screenshot of Splunk instance and received events |
| Sysmon | Windows system telemetry source | Service/configuration and Event Viewer evidence |
| VirtualBox | Hypervisor used in the public walkthrough write-up | VM list and network settings |

**Verify the actual components you used.** Do not add Ubuntu, Wazuh, TheHive, Shuffle, or other products unless they were genuinely part of your implementation.

## Architecture

See [`diagrams/lab-architecture.svg`](diagrams/lab-architecture.svg). Update it if your actual topology differs. Add actual private lab IP addresses only if safe; otherwise use documentation-only placeholders such as `192.0.2.10`.

## Repository map

- `docs/` — concepts, methodology, validation, and limitations.
- `evidence/screenshots/` — your own screenshots, named using the checklist.
- `evidence/logs/` — sanitised event exports or search results, if safe to share.
- `incident-reports/` — evidence-based investigation write-ups.
- `diagrams/` — architecture diagram.

## Evidence status

The folders are intentionally supplied without fabricated screenshots or log files. Add original evidence from your own lab. A screenshot should show enough context to establish what it demonstrates, while hiding passwords, tokens, public IPs, personal usernames, and unrelated personal data.

See [`docs/08-evidence-checklist.md`](docs/08-evidence-checklist.md).

## Suggested reading order

1. [Scope and methodology](docs/01-scope-and-methodology.md)
2. [Architecture and data flow](docs/02-architecture-and-data-flow.md)
3. [Tools and technical concepts](docs/03-tools-and-concepts.md)
4. [Telemetry and event interpretation](docs/04-windows-and-sysmon-telemetry.md)
5. [Controlled test methodology](docs/05-test-methodology.md)
6. [Detection and investigation](docs/06-detection-and-investigation.md)
7. [Results and limitations](docs/07-results-and-limitations.md)
8. [Evidence checklist](docs/08-evidence-checklist.md)

## Safety and responsible use

- Run tests only on systems you own or are explicitly authorised to test.
- Keep the lab isolated from production networks and personal devices.
- Use disposable snapshots and benign test data wherever possible.
- Do not upload executable payloads, credentials, session tokens, private logs, or malware samples.
- Do not disable endpoint protections on a daily-use machine. If a tutorial requires a deliberately weakened test VM, keep it isolated and revert it afterwards.
- A successful connection or generated event is not, by itself, proof that a SIEM detection worked.

## Attribution

This is an independent learning report based on a publicly available tutorial. The tutorial creator retains ownership of the original instructional material. This repository should not reproduce their video, screenshots, or substantial text. Cite the tutorial and explain your own implementation and observations.

## References

- MyDFIR, [Build A Basic Home Lab (Part 3)](https://www.youtube.com/watch?v=-8X7Ay4YCoA).
- Efam Harris, [My First Attempt at Building a Simple Home Lab for Threat Detection and Monitoring](https://medium.com/@efamharris/my-first-attempt-at-building-a-simple-home-lab-for-threat-detection-and-monitoring-a0e6513e5432) — a separate learner's account of the series; useful corroborating context, not proof of this repository owner's results.
- Microsoft Sysinternals, [Sysmon](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon).
- Splunk, [Search Manual](https://docs.splunk.com/Documentation/Splunk/latest/Search/Aboutthesearchlanguage).
- MITRE, [ATT&CK](https://attack.mitre.org/).
- NIST, [Computer Security Incident Handling Guide (SP 800-61 Rev. 2)](https://csrc.nist.gov/pubs/sp/800/61/r2/final).

## Author's implementation details

- Hypervisor: `[ADD ACTUAL HYPERVISOR/VERSION]`
- Host OS and hardware: `[ADD ONLY WHAT YOU ARE COMFORTABLE SHARING]`
- Guest OS versions: `[ADD EXACT VERSIONS]`
- SIEM: `[CONFIRM ACTUAL PRODUCT AND VERSION]`
- Sysmon version/configuration: `[ADD VERSION/CONFIG SOURCE]`
- Lab network mode/subnet: `[ADD ACTUAL MODE; REDACT PUBLIC DETAILS]`
- Completion date: `[ADD DATE]`
