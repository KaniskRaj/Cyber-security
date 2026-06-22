# Third-Party / Vendor Risk Assessment Template

**Organization:** Solstice Retail Group (fictitious company, used for portfolio purposes)
**Document owner:** Security & GRC Team

## 1. Purpose

Standardizes how vendors are evaluated for security risk before
onboarding and at periodic reassessment, so that risk tiering and
required controls are consistent across procurement decisions.

## 2. Risk Tiering Methodology

Tier is determined by the combination of **data sensitivity** the vendor
will access and **level of system access** granted.

| Tier | Criteria | Reassessment Frequency |
|---|---|---|
| Critical | Access to customer PII/payment data, or direct production system access | Annual + on any material change |
| High | Access to internal confidential data, no direct customer data | Annual |
| Medium | Limited internal data access, no sensitive data | Every 2 years |
| Low | No data access (e.g., physical facilities vendor) | Onboarding only |

## 3. Assessment Questionnaire (Summary Categories)

1. **Data handling** – What data is accessed/stored/processed? Where (geography)? Is it encrypted at rest and in transit?
2. **Access control** – How is access to our data/systems authenticated? Is MFA enforced? Is access logged?
3. **Compliance certifications** – SOC 2 Type II, ISO 27001, PCI-DSS (if applicable)? Date of most recent audit?
4. **Incident history** – Any breaches or significant incidents in the past 3 years? How were they disclosed and remediated?
5. **Business continuity** – RTO/RPO commitments? Subcontractor (fourth-party) dependencies disclosed?
6. **Contractual** – Breach notification clause and timeline? Right-to-audit clause? Data deletion upon contract termination?

## 4. Worked Example: Vendor Assessment

**Vendor:** "PayFlow Processing" (fictitious payment processor)
**Assessment date:** 2026-04
**Proposed tier:** Critical (handles customer payment data)

| Category | Finding | Risk Flag |
|---|---|---|
| Data handling | Card data tokenized at point of capture; PCI-DSS Level 1 certified | None |
| Access control | MFA enforced for all admin access; API keys rotated quarterly | None |
| Compliance | Valid PCI-DSS attestation (AOC) on file, dated within 12 months; SOC 2 Type II report provided | None |
| Incident history | One disclosed incident in 2024 (third-party library vulnerability, no customer data affected, patched within 48 hrs) | Low — disclosed proactively, fast remediation |
| Business continuity | RTO of 4 hours, RPO of 15 minutes; documented failover region | None |
| Contractual | 24-hour breach notification clause; right-to-audit included; data deletion confirmed within 30 days of offboarding | None |

**Outcome:** Approved as Critical-tier vendor. Scheduled for annual
reassessment. Logged in risk register as R-003 (third-party payment
processor breach) with current residual risk rated Low-Medium based on
the controls above.

## 5. Escalation Criteria

A vendor assessment is escalated to the Security & GRC Team lead (rather
than approved by the requesting business owner alone) if any of the
following apply:
- Tier is Critical
- No SOC 2/ISO 27001 equivalent certification exists for a Critical or High tier vendor
- Any undisclosed-until-asked incident history surfaces during assessment
- Vendor cannot commit to a breach notification window of 72 hours or less
