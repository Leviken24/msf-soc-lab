# 6. Detection and Investigation

## 6.1 Analyst workflow

1. Validate the alert or event exists and note its timestamp.
2. Identify the host and user context.
3. Inspect the process, parent process, command line, and file path where available.
4. Review associated network events and destination details where collected.
5. Search a time window around the event for related activity.
6. Compare observations with expected administrative or test activity.
7. State a conclusion with confidence and supporting evidence.
8. Recommend containment or remediation only when justified by the findings.

## 6.2 Investigation questions

- Which endpoint generated the event?
- What time did it occur, and what timezone is used?
- Which process was involved?
- What was the parent process?
- Which user context was recorded?
- Was a network connection recorded? If so, which process and endpoints?
- Are there related file or registry events?
- Does the evidence match the controlled test timeline?
- What alternative benign explanation exists?
- What evidence is still missing?

## 6.3 ATT&CK mapping

MITRE ATT&CK is a knowledge base of adversary tactics and techniques based on observed behaviours. Map a technique only when the observed behaviour supports it. Do not map a technique merely because a tool could perform it.

For every mapping, record:
- ATT&CK tactic;
- technique/sub-technique ID and name;
- exact observed behaviour;
- event/log evidence;
- confidence and caveats.

Reference: https://attack.mitre.org/

## 6.4 Incident report template

Use `incident-reports/IR-001-template.md`. Keep the report factual and distinguish confirmed facts from hypotheses.
