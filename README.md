# Cyber-security

A small collection of hands-on security-analyst exercise writeups: incident
report documentation and a controls/compliance assessment checklist.

## Contents

| File | Description |
|---|---|
| [`controls-and-compliance-checklist.pdf`](controls-and-compliance-checklist.pdf) | Controls assessment checklist covering least privilege, disaster recovery, password policy, separation of duties, firewalls, IDS, backups, antivirus, and legacy-system monitoring — mapped against common compliance frameworks. |
| [`incident-report-network-traffic-analysis.pdf`](incident-report-network-traffic-analysis.pdf) | Incident report analyzing a DNS/ICMP traffic capture where `tcpdump` revealed a "UDP port 53 unreachable" error, working through root-cause analysis of the affected web service. |
| [`incident-report-template.pdf`](incident-report-template.pdf) | Worked incident report example: an HTTP-based incident where users were redirected to a lookalike domain after downloading a file from a compromised site, analyzed in a sandboxed environment. |

## Purpose

These are practice writeups completed as part of cybersecurity-analyst
training — documenting how to identify, analyze, and report on security
incidents using standard tools (`tcpdump`, sandboxing) and standard report
structures (problem summary, root-cause analysis, remediation).

## License

Feel free to use these as reference templates for your own incident-report
or controls-checklist documentation.
