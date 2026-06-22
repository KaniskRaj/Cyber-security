# Risk Register

**Organization:** Solstice Retail Group (fictitious company, used for portfolio purposes)
**Document owner:** Security & GRC Team
**Last updated:** 2026-06

Scoring: Likelihood and Impact rated 1 (Low) – 5 (High). Inherent Risk Score
= Likelihood × Impact. Residual Risk reflects the score after existing
controls are factored in.

| ID | Risk | Category | Likelihood | Impact | Inherent Score | Existing Controls | Residual Risk | Owner | Treatment Plan | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| R-001 | Phishing-driven credential theft leading to account takeover | Human/Technical | 4 | 4 | 16 | Security awareness training, email filtering, MFA on all accounts | Medium | Security & GRC | Maintain quarterly phishing simulations; expand MFA to legacy POS admin accounts | Open |
| R-002 | Ransomware via exposed RDP or unpatched VPN appliance | Technical | 3 | 5 | 15 | Endpoint detection (EDR), network segmentation, offline backups | Medium | IT Operations | Disable direct RDP exposure; enforce VPN + MFA for all remote access | Open |
| R-003 | Third-party payment processor breach exposing customer card data | Third-Party | 2 | 5 | 10 | Vendor requires PCI-DSS attestation; contractual breach notification clause | Low-Medium | GRC / Procurement | Annual vendor risk reassessment (see vendor-risk-assessment-template.md) | Monitoring |
| R-004 | Unpatched legacy point-of-sale (POS) systems | Technical | 4 | 4 | 16 | Network segmentation isolating POS VLAN; compensating monitoring | High | IT Operations | Budget approved for POS refresh, target completion Q4 | Open |
| R-005 | Cloud storage bucket misconfiguration exposing customer PII | Technical | 3 | 4 | 12 | Cloud security posture management (CSPM) tool, quarterly config audits | Low | Cloud/Infra Team | Automate public-access alerting (already in progress) | Mitigating |
| R-006 | Insider threat — unauthorized data exfiltration by privileged user | Human | 2 | 4 | 8 | Privileged access logging, DLP on email/USB, separation of duties on financial systems | Low | Security & GRC | Extend DLP coverage to cloud storage egress | Monitoring |
| R-007 | Vendor without independent security certification handling customer data | Third-Party | 3 | 3 | 9 | Vendor risk tiering process requires SOC 2 or equivalent for Tier 1 vendors | Medium | Procurement / GRC | Require remediation plan or replace vendor within 90 days if certification not obtained | Open |
| R-008 | BYOD device loss/theft exposing corporate email or data | Human/Technical | 3 | 3 | 9 | MDM enrollment required, remote wipe capability, disk encryption enforced | Low | IT Operations | No further action; monitor MDM compliance rate | Monitoring |
| R-009 | Single point of failure: no tested failover for core e-commerce database | Operational | 2 | 5 | 10 | Nightly backups; failover documented but untested in past 12 months | Medium | IT Operations | Schedule disaster recovery test in Q3 | Open |
| R-010 | Lack of MFA enforcement on a subset of legacy admin accounts | Technical | 3 | 4 | 12 | Partial MFA rollout; legacy accounts identified in access control policy review | Medium | Security & GRC | Complete MFA rollout to remaining accounts by end of quarter | Open |

## Review Cadence

This register is reviewed monthly by the Security & GRC team and presented
quarterly to leadership. Any risk scoring 15+ (inherent) requires an
executive-level treatment decision within 30 days of identification.
