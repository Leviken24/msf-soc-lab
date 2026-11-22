# 7. Results, Limitations, and Lessons Learned

## 7.1 Results

Populate this section after reviewing your original evidence.

| Measure | Result |
|---|---|
| Virtual machines created | `[COUNT / NAMES]` |
| Endpoint telemetry source | `[CONFIRM]` |
| SIEM product | `[CONFIRM]` |
| Test scenarios performed | `[COUNT]` |
| Scenarios with endpoint events | `[COUNT]` |
| Scenarios with searchable SIEM events | `[COUNT]` |
| Scenarios that triggered a configured detection | `[COUNT OR NOT CONFIGURED]` |

Do not calculate a detection rate from a tiny tutorial exercise or treat untested scenarios as successful.

## 7.2 Limitations to discuss

Select only those that apply:
- Small number of endpoints and test scenarios.
- Single-host virtualisation and limited resources.
- Limited event coverage due to Sysmon configuration.
- No production-scale retention, redundancy, or access control validation.
- Detection rules may be default, tutorial-provided, or manually configured.
- No comprehensive false-positive/false-negative evaluation.
- Results depend on software versions and configuration at test time.
- Lab-generated traffic does not represent all real-world attack behaviour.

## 7.3 Lessons learned

Write your own reflections:
- What network issue did you troubleshoot?
- What telemetry was easiest/hardest to locate?
- Which event fields were useful?
- What did you initially misunderstand?
- What would you change in a second iteration?

## 7.4 Future improvements

Possible extensions, clearly labelled as future work rather than completed features:
- Add more endpoints and centralised identity telemetry.
- Develop and test custom detection rules.
- Enrich alerts with trusted threat intelligence.
- Add incident case management.
- Add response automation with approval gates.
- Test log integrity, access control, and retention.
- Build repeatable test cases and document expected telemetry.
