# Cyber-security

A GRC / security analyst portfolio: policies, risk management artifacts,
incident response documentation, and assessments, written around a
consistent fictitious organization (**Solstice Retail Group**) so the
work reads as a connected body of analysis rather than disconnected
samples.

> All company names, incidents, and figures in this repository are
> fictitious and created for portfolio/demonstration purposes.

## Structure

```
.
├── policies/
│   ├── incident-response-policy.md      # IR roles, severity tiers, lifecycle
│   └── access-control-policy.md         # Least privilege, MFA, access review cadence
├── risk-management/
│   ├── risk-register.md                 # 10 sample risks, scored and tracked
│   └── nist-csf-gap-assessment.md        # Maturity assessment against NIST CSF 2.0
├── incident-reports/
│   ├── incident-report-network-traffic-analysis.pdf
│   ├── incident-report-template.pdf
│   └── tabletop-exercise-ransomware.md   # Tabletop exercise after-action report
└── assessments/
    ├── controls-and-compliance-checklist.pdf
    ├── vendor-risk-assessment-template.md  # Tiering methodology + worked example
    └── vulnerability-assessment-summary.md # Sample internal vuln scan report
```

## How these pieces connect

This isn't a random folder of templates — each document references the
others the way a real GRC program would:

- The **risk register** is the central tracking artifact. Risks identified in the **NIST CSF gap assessment**, the **vulnerability assessment**, and the **vendor risk assessment** all map back to specific risk IDs (e.g., `R-004`, `R-009`).
- The **tabletop exercise** report tests the **Incident Response Policy** in practice and produces action items that feed back into both the policy and the risk register.
- The **access control policy** sets the requirements (MFA, access reviews) that the **gap assessment** and **risk register** measure compliance against.

## Why this structure

Real security/GRC work product isn't just incident writeups — it's the
ongoing cycle of: assess risk → set policy → test the policy → find
gaps → feed gaps back into the risk register → reassess. This repo is
organized to show that cycle rather than just a pile of one-off reports.

## License

MIT — see [LICENSE](LICENSE). Feel free to use these as reference
templates for your own GRC documentation.
