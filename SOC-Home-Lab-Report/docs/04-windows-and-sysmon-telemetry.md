# 4. Windows and Sysmon Telemetry

## 4.1 Windows Event Log

Windows components and applications publish event records to channels such as Application, System, and Security. Additional providers create their own channels. The Security log's contents depend on audit policy and permissions.

## 4.2 Sysmon Operational channel

Sysmon writes to:

`Applications and Services Logs/Microsoft/Windows/Sysmon/Operational`

The exact events recorded depend on the Sysmon version and active configuration. Preserve the configuration used during the test because it determines what telemetry is available.

## 4.3 Common Sysmon event IDs

These are commonly documented Sysmon event identifiers. Their presence in a particular run must be verified in the actual logs.

| Event ID | Event name | Typical investigative value |
|---:|---|---|
| 1 | Process Create | Process image, command line, parent process, hashes (depending on configuration). |
| 3 | Network Connection | Process-associated network connection; collection is configuration-dependent. |
| 5 | Process Terminated | Process termination. |
| 7 | Image Loaded | Module/DLL load; can be high-volume and is often filtered. |
| 10 | Process Access | One process accessed another; requires careful interpretation. |
| 11 | File Create | File creation. |
| 12 | Registry Object Create/Delete | Registry key/value creation or deletion. |
| 13 | Registry Value Set | Registry value modification. |
| 22 | DNS Query | DNS query activity. |

Do not claim that every event ID was collected. Confirm the event ID and fields in Event Viewer or the SIEM.

## 4.4 Useful investigation fields

Depending on the event type and source, fields may include:
- event timestamp;
- computer/host;
- provider and channel;
- event ID;
- process image and process ID;
- parent image and parent process ID;
- command line;
- user;
- source and destination IP/port;
- file path and hash.

Field names vary between raw Windows XML, Sysmon, and SIEM-normalised events. Record the exact field names shown in your data.

## 4.5 Evidence to capture

- Sysmon version and service status.
- Active Sysmon configuration (redact local paths/usernames if needed).
- Event Viewer showing the Sysmon Operational channel.
- One genuine event record generated during the test.
- Corresponding SIEM event, if ingestion was configured.

Never invent an event record or copy another person's log as if it came from your machine.
