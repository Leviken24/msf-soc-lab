# 8. Evidence Checklist

Use your own screenshots. Save PNG/JPG files in `evidence/screenshots/` and refer to them in the report. Suggested filenames are below.

| ID | Suggested filename | What it should demonstrate | Status |
|---|---|---|---|
| E-01 | `E01-vm-inventory.png` | Hypervisor showing the actual lab VMs | TO ADD |
| E-02 | `E02-network-settings.png` | Actual virtual network mode/settings | TO ADD |
| E-03 | `E03-kali-ip.png` | Kali lab interface/IP (redact if needed) | TO ADD |
| E-04 | `E04-windows-ip.png` | Windows lab interface/IP | TO ADD |
| E-05 | `E05-sysmon-service.png` | Sysmon service/configuration status | TO ADD |
| E-06 | `E06-sysmon-event-viewer.png` | Sysmon Operational channel with a real event | TO ADD |
| E-07 | `E07-siem-home.png` | Actual SIEM product/dashboard | TO ADD |
| E-08 | `E08-siem-ingestion.png` | Search result proving event ingestion | TO ADD |
| E-09 | `E09-test-activity.png` | Sanitised evidence of the test action | TO ADD |
| E-10 | `E10-investigation.png` | Event details/search used in analysis | TO ADD |
| E-11 | `E11-network-observation.png` | Relevant connection evidence, if collected | OPTIONAL |
| E-12 | `E12-final-test-matrix.png` | Completed test results, if useful | OPTIONAL |

## Screenshot quality rules

- Capture the real application/terminal, not a recreated mock-up.
- Include the relevant title bar, event ID, timestamp, or query context.
- Avoid cropping away context needed to interpret the evidence.
- Redact passwords, tokens, private keys, personal email addresses, public IPs, and unrelated personal information.
- Do not expose real usernames if unnecessary.
- Use consistent filenames and reference each image from Markdown.
- Never alter an image in a way that changes its technical meaning.

## Logs

If you include logs:
- export only the relevant event range;
- remove credentials and personal data;
- retain timestamps and event identifiers;
- state the source machine and timezone;
- do not upload executables, memory dumps, or sensitive raw datasets;
- add a short note explaining how the log was collected.

## Evidence integrity

A screenshot is supporting evidence, not a guarantee of authenticity by itself. Keep original exports locally. Do not claim a screenshot proves more than the visible information supports.
