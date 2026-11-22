# 2. Architecture and Data Flow

## 2.1 Logical components

The tutorial-aligned baseline uses a virtualised attacker/test workstation and a Windows endpoint. Splunk is used as the SIEM in the associated tutorial series, and Sysmon supplies detailed Windows telemetry. Confirm the precise topology and versions from your own build.

| Component | Responsibility |
|---|---|
| Hypervisor | Runs isolated guest operating systems on the host. |
| Kali Linux VM | Generates authorised test activity within the lab. |
| Windows VM | Target endpoint; produces Windows and Sysmon events. |
| Sysmon | Records selected low-level system activity. |
| Splunk | Receives, indexes, searches, and visualises ingested data. |

## 2.2 Data flow

1. An operator performs a controlled action from the test workstation.
2. Windows processes the action and may generate Windows event records.
3. Sysmon records configured telemetry about selected activity.
4. A configured collection/forwarding mechanism sends the relevant records to Splunk.
5. Splunk indexes the data.
6. An analyst searches the indexed events and evaluates whether they support a security finding.

**Important:** The exact forwarding method, input configuration, ports, and data source names are environment-specific. Document the actual configuration rather than assuming a universal setup.

## 2.3 Network design

Record:
- hypervisor network mode: `[NAT / NAT Network / Host-only / Internal / other]`
- subnet and mask: `[ADD PRIVATE LAB SUBNET]`
- Kali address: `[REDACT OR ADD PRIVATE LAB IP]`
- Windows address: `[REDACT OR ADD PRIVATE LAB IP]`
- SIEM address: `[ADD ONLY IF APPLICABLE]`
- permitted paths between VMs: `[DESCRIBE]`
- internet access from each VM: `[DESCRIBE]`

Use an isolated/internal network where feasible. If internet access is needed for updates, separate that requirement from the test network and avoid exposing deliberately vulnerable services to the public internet.

## 2.4 Diagram

The supplied SVG is a conceptual diagram. Change it to match the actual implementation. It does not assert a particular network mode or forwarding mechanism.
