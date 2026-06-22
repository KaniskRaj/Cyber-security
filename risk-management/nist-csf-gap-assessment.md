# NIST Cybersecurity Framework (CSF 2.0) Gap Assessment

**Organization:** Solstice Retail Group (fictitious company, used for portfolio purposes)
**Document owner:** Security & GRC Team
**Assessment date:** 2026-06
**Framework version:** NIST CSF 2.0

## Purpose

This assessment evaluates Solstice Retail Group's current security
maturity against the six NIST CSF 2.0 functions, identifies gaps, and
prioritizes remediation. Maturity is rated using NIST's tier model:

- **Tier 1 – Partial:** ad hoc, reactive practices
- **Tier 2 – Risk Informed:** risk-aware but not consistently applied
- **Tier 3 – Repeatable:** formal policies, consistently applied
- **Tier 4 – Adaptive:** continuously improved based on lessons learned and threat intel

## Summary by Function

| Function | Current Tier | Target Tier | Key Gap | Priority |
|---|---|---|---|---|
| **Govern (GV)** | 2 | 3 | No formal risk appetite statement approved by leadership; risk register exists but isn't tied to a documented governance cadence beyond monthly GRC review | High |
| **Identify (ID)** | 3 | 3 | Asset inventory is maintained but doesn't yet include shadow IT/SaaS discovery | Medium |
| **Protect (PR)** | 2 | 3 | MFA rollout incomplete on legacy admin accounts (see R-010); POS systems are end-of-life with limited compensating controls (see R-004) | High |
| **Detect (DE)** | 3 | 3 | EDR and network monitoring in place; detection coverage on cloud infrastructure (CSPM) is newer and less mature than endpoint coverage | Medium |
| **Respond (RS)** | 3 | 3 | Incident Response Policy is documented and exercised (see tabletop-exercise-ransomware.md); communications/legal coordination during tabletops surfaced timing gaps | Medium |
| **Recover (RC)** | 2 | 3 | Backup processes exist but disaster recovery failover has not been tested in 12+ months (see R-009) | High |

## Detailed Findings

### Govern
- **Strength:** A risk register is actively maintained and reviewed monthly.
- **Gap:** No board/executive-approved risk appetite statement exists to anchor prioritization decisions (e.g., what residual risk level is acceptable before requiring executive sign-off).
- **Recommendation:** Draft and obtain executive sign-off on a risk appetite statement; tie it explicitly to the existing risk register scoring thresholds.

### Identify
- **Strength:** Core infrastructure and application assets are inventoried.
- **Gap:** No automated discovery process for unsanctioned SaaS tools (shadow IT), which limits visibility into where company data may live outside approved systems.
- **Recommendation:** Evaluate a SaaS discovery/CASB tool; incorporate findings into the asset inventory quarterly.

### Protect
- **Strength:** Access Control Policy defines least privilege, MFA requirements, and periodic access reviews.
- **Gap:** Legacy POS systems and a subset of admin accounts are not yet covered by current controls (tracked as R-004 and R-010 in the risk register).
- **Recommendation:** Prioritize POS refresh and complete MFA rollout — both already have committed remediation timelines.

### Detect
- **Strength:** EDR deployed fleet-wide; SIEM aggregates logs from core infrastructure.
- **Gap:** Cloud security posture monitoring is functional but newer, with less tuning than endpoint detection — higher false-negative risk for cloud misconfigurations.
- **Recommendation:** Run a focused tuning exercise on CSPM alert thresholds over the next quarter.

### Respond
- **Strength:** Documented Incident Response Policy with defined severity tiers and roles; tested via tabletop exercise.
- **Gap:** The ransomware tabletop exercise (see `/incident-reports/tabletop-exercise-ransomware.md`) identified a delay in Legal & Compliance engagement during the simulated incident.
- **Recommendation:** Add Legal & Compliance to the initial P1 paging chain rather than looping them in after initial containment.

### Recover
- **Strength:** Nightly backups are in place for core systems.
- **Gap:** Documented failover process for the core e-commerce database has not been tested in the past 12 months (R-009).
- **Recommendation:** Schedule and execute a full failover test, document results, and feed lessons learned back into the Recovery runbook.

## Next Steps

1. Present this assessment to leadership alongside the risk register for prioritization.
2. Track all "High" priority gaps as formal risk register entries with owners and target dates.
3. Re-assess maturity tiers in 6 months to measure progress.
