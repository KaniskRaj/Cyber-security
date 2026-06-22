# Incident Response Policy

**Organization:** Solstice Retail Group (fictitious company, used for portfolio purposes)
**Document owner:** Security & GRC Team
**Classification:** Internal
**Version:** 1.0
**Last reviewed:** 2026-06

## 1. Purpose

This policy defines how Solstice Retail Group detects, responds to, and
recovers from cybersecurity incidents, and assigns clear ownership at each
stage so that response time and decision-making are not blocked by
ambiguity during an active incident.

## 2. Scope

Applies to all employees, contractors, and third parties with access to
Solstice systems, networks, or data, and to all incidents affecting
confidentiality, integrity, or availability of company or customer data.

## 3. Definitions

| Term | Definition |
|---|---|
| Event | Any observable occurrence in a system or network. |
| Incident | An event that violates security policy or threatens confidentiality, integrity, or availability of data/systems. |
| Breach | An incident resulting in confirmed unauthorized access to or disclosure of sensitive data. |

## 4. Severity Classification

| Severity | Criteria | Initial Response Target |
|---|---|---|
| P1 – Critical | Active data breach, ransomware, or customer-facing outage caused by an attack | 15 minutes |
| P2 – High | Confirmed compromise with no active data loss (e.g., isolated malware, compromised single account) | 1 hour |
| P3 – Medium | Suspicious activity requiring investigation, no confirmed compromise | 4 hours |
| P4 – Low | Policy violations, low-risk anomalies | 1 business day |

## 5. Roles & Responsibilities

| Role | Responsibility |
|---|---|
| Incident Commander (IC) | Owns the response, coordinates workstreams, makes containment decisions |
| Security Analyst(s) | Triage, investigation, evidence collection, containment actions |
| IT Operations | Executes technical containment/recovery (isolating hosts, resetting credentials, restoring from backup) |
| Legal & Compliance | Assesses breach notification obligations (state/federal law, contractual) |
| Communications | Manages internal and customer-facing messaging |
| Executive Sponsor | Approves disclosure decisions, resourcing, and external engagement (forensics, law enforcement) |

## 6. Incident Response Lifecycle

This policy follows the NIST SP 800-61 lifecycle:

1. **Preparation** – Maintain IR runbooks, tooling, contact lists, and conduct tabletop exercises (see `/incident-reports/tabletop-exercise-ransomware.md` for an example).
2. **Detection & Analysis** – Triage alerts, confirm scope and severity, classify per Section 4.
3. **Containment** – Isolate affected systems/accounts to stop spread without destroying evidence.
4. **Eradication** – Remove the root cause (malware, unauthorized access, vulnerability).
5. **Recovery** – Restore systems to normal operation, validate integrity before reconnecting to production.
6. **Post-Incident Review** – Conduct a blameless retrospective within 5 business days; document root cause, timeline, and corrective actions.

## 7. Reporting & Notification

- All P1/P2 incidents must be reported to the Incident Commander immediately upon detection.
- Legal & Compliance must assess regulatory notification timelines (e.g., 72-hour breach notification windows where applicable) within 24 hours of confirmed breach.
- A post-incident report must be filed for every P1/P2 incident and retained for a minimum of 3 years.

## 8. Policy Review

This policy is reviewed annually or after any P1 incident, whichever comes first.
