# 1. Scope and Methodology

## 1.1 Purpose

The purpose of this project is to learn how endpoint activity becomes security telemetry and how an analyst can use that telemetry to investigate suspicious behaviour in a small lab.

The project is a learning exercise, not a formal penetration test, security audit, or production deployment.

## 1.2 Scope

**In scope (confirm against what you actually completed):**
- Virtual machines created for a controlled lab.
- Network connectivity between the lab machines.
- Windows endpoint event generation.
- Sysmon telemetry collection.
- SIEM ingestion and searching.
- A controlled, authorised test scenario.
- Review of the resulting events.

**Out of scope unless separately implemented and evidenced:**
- Enterprise-scale log retention or high availability.
- Production incident response.
- Threat-intelligence enrichment.
- Automated containment or SOAR.
- Proof of complete attack detection.
- Testing against third-party systems.

## 1.3 Method

The workflow is:

1. Build the virtual environment.
2. Configure the lab network.
3. Configure endpoint telemetry.
4. Confirm that telemetry is generated locally.
5. Configure forwarding to the SIEM.
6. Confirm that the SIEM receives searchable events.
7. Run only the authorised lab test(s).
8. Search for related telemetry and record findings.
9. Document gaps, false positives, and limitations.

Each stage should be supported by a screenshot, log excerpt, or configuration extract where possible.

## 1.4 Evidence standard

For every claim, retain:
- what was tested;
- when it was tested (timezone included);
- which machine generated the evidence;
- the exact observable result;
- the screenshot/log filename;
- whether the result passed, failed, or was not tested.

Do not infer a successful detection merely because a test ran or a connection was established.
