# Tabletop Exercise: Ransomware Scenario — After-Action Report

**Organization:** Solstice Retail Group (fictitious company, used for portfolio purposes)
**Exercise date:** 2026-05
**Facilitator:** Security & GRC Team
**Exercise type:** Discussion-based tabletop

## 1. Objectives

1. Validate the Incident Response Policy's roles, escalation paths, and severity classification under a realistic ransomware scenario.
2. Identify gaps in cross-team coordination (IT, Legal, Communications, Executive).
3. Produce concrete, owned action items — not just observations.

## 2. Participants

| Role | Function Represented |
|---|---|
| Incident Commander | Security & GRC |
| Security Analyst | Security & GRC |
| IT Operations Lead | Infrastructure |
| Legal Counsel | Legal & Compliance |
| Communications Lead | Marketing/Comms |
| Executive Sponsor | Leadership |

## 3. Scenario

> 8:14 AM: A store-operations employee reports their workstation displaying
> a ransom note. Shortly after, IT Operations confirms file shares on a
> regional file server are encrypted. Initial triage shows the entry point
> was a phishing email opened two days earlier, with lateral movement to
> the file server overnight.

The exercise proceeded through four scripted "injects" (new information
introduced at intervals) to simulate how the situation would evolve:

| Time (simulated) | Inject |
|---|---|
| T+0 | Initial report of ransom note on a single workstation |
| T+30 min | Confirmation that a regional file server is encrypted; backups for that server are 36 hours old |
| T+90 min | Attacker contact via the ransom note demanding payment within 72 hours, threatening data publication |
| T+3 hrs | Media inquiry received, asking whether customer data was affected |

## 4. Key Decisions Made During Exercise

- Incident Commander classified the event as **P1 – Critical** at T+30 min once server-level encryption was confirmed, per the severity matrix in the Incident Response Policy.
- IT Operations isolated the affected VLAN immediately rather than waiting for full scope confirmation, accepting some loss of forensic visibility in exchange for faster containment.
- Executive Sponsor and Legal Counsel were *not* looped in until T+90 min (after the ransom contact), rather than at initial P1 declaration.
- Communications Lead drafted a holding statement for the media inquiry but had not been pre-briefed on what could/couldn't be confirmed about customer data exposure.

## 5. What Went Well

- Severity classification and IT containment actions matched the documented policy closely — the IR Policy's escalation matrix was usable in practice, not just on paper.
- Technical containment (VLAN isolation) was fast and decisive.

## 6. Gaps Identified

| Gap | Impact | Recommendation |
|---|---|---|
| Legal & Comms engaged late (T+90 min instead of at P1 declaration) | Delayed assessment of notification obligations and media readiness | Update IR Policy paging chain so Legal & Comms are included in the *initial* P1 notification, not after ransom contact |
| Backup recency for regional file servers (36 hrs old) extended potential data loss window | Recovery would have meant losing up to 36 hours of operational data | Move regional file servers to a more frequent backup schedule (target: every 4–6 hours) |
| No pre-approved media holding statement template existed | Comms had to draft language live during a live-fire scenario | Create pre-approved holding statement templates for common incident types, reviewed by Legal in advance |
| Ransom decision authority (pay/don't pay) was discussed but no named decision-maker was confirmed in the moment | Risk of delay or confusion in a real event | Document in IR Policy that ransom payment decisions require Executive Sponsor + Legal sign-off, never IT/Security alone |

## 7. Action Items

| Action | Owner | Target Date | Status |
|---|---|---|---|
| Update IR Policy paging chain to include Legal & Comms at initial P1 declaration | Security & GRC | 2026-07 | Open |
| Increase backup frequency for regional file servers | IT Operations | 2026-08 | Open |
| Draft pre-approved media holding statement templates | Communications + Legal | 2026-07 | Open |
| Document ransom payment decision authority explicitly in IR Policy | Legal + Executive Sponsor | 2026-07 | Open |

## 8. Conclusion

The exercise validated that the technical response process works well, but
surfaced a real coordination gap around when non-technical stakeholders
(Legal, Comms, Executive) are engaged. All four action items have been
fed into the risk register and IR Policy update cycle.
