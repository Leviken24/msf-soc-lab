# 5. Controlled Test Methodology

## 5.1 Safety prerequisites

- Use only virtual machines and systems you own or have explicit permission to test.
- Keep the environment isolated from public networks and production assets.
- Take clean snapshots before testing.
- Use dummy accounts and non-sensitive data.
- Do not upload executable payloads or live credentials to GitHub.
- Revert the test endpoint after the exercise.
- Record any security-control changes and restore them immediately after the lab.

## 5.2 Test record template

Create one record for every scenario actually performed.

| Field | Value |
|---|---|
| Test ID | `[T-001]` |
| Scenario | `[DESCRIBE OBSERVED TEST]` |
| Date/time and timezone | `[ADD]` |
| Source machine | `[ADD]` |
| Target machine | `[ADD]` |
| Preconditions | `[ADD]` |
| Action performed | `[HIGH-LEVEL DESCRIPTION; DO NOT PUBLISH LIVE PAYLOAD]` |
| Expected telemetry | `[HYPOTHESIS, NOT A RESULT]` |
| Actual telemetry | `[OBSERVED EVENT IDS/FIELDS]` |
| SIEM result | `[OBSERVED SEARCH/ALERT RESULT]` |
| Status | `PASS / FAIL / NOT TESTED` |
| Evidence | `[FILENAMES]` |
| Notes | `[LIMITATIONS/ERRORS]` |

## 5.3 Distinguish the stages

Report these separately:

1. **Action executed:** Did the test action run?
2. **Endpoint logged:** Did Windows/Sysmon record it?
3. **Data forwarded:** Did the configured collector send it?
4. **SIEM indexed:** Can the event be searched in Splunk?
5. **Detection fired:** Did an actual rule/alert trigger?
6. **Analyst validated:** Did the analyst review context and decide what the event means?

A successful result at one stage does not prove success at the next stage.

## 5.4 Test matrix

Fill only with results you personally observed.

| Test ID | Activity | Endpoint log | SIEM ingestion | Alert/detection | Outcome |
|---|---|---|---|---|---|
| T-001 | `[ACTUAL TEST]` | `[YES/NO/UNKNOWN]` | `[YES/NO/UNKNOWN]` | `[YES/NO/NOT CONFIGURED]` | `[PASS/FAIL/NOT TESTED]` |
| T-002 | `[ACTUAL TEST]` | `[YES/NO/UNKNOWN]` | `[YES/NO/UNKNOWN]` | `[YES/NO/NOT CONFIGURED]` | `[PASS/FAIL/NOT TESTED]` |

If the lab only demonstrated event visibility and not an alert rule, say so. Visibility and detection are different capabilities.
