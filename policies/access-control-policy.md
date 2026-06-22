# Access Control Policy

**Organization:** Solstice Retail Group (fictitious company, used for portfolio purposes)
**Document owner:** Security & GRC Team
**Classification:** Internal
**Version:** 1.0
**Last reviewed:** 2026-06

## 1. Purpose

Defines the principles and minimum controls governing how access to
Solstice systems and data is granted, reviewed, and revoked, to limit
exposure from compromised credentials and insider risk.

## 2. Guiding Principles

- **Least privilege** – users are granted the minimum access required to perform their job function, nothing more.
- **Need-to-know** – access to sensitive data is restricted to roles that require it for a defined business purpose.
- **Separation of duties** – no single individual should be able to both initiate and approve a high-risk action (e.g., creating a vendor *and* approving its payment).
- **Default deny** – access is off by default and explicitly granted, not the reverse.

## 3. Account Lifecycle

| Stage | Requirement |
|---|---|
| Provisioning | Access requests require manager approval and map to a defined role/group — no standing individual permissions outside documented roles. |
| Periodic Review | Access reviews conducted quarterly for standard accounts, monthly for privileged/admin accounts. Unused access flagged and revoked if not justified within 5 business days. |
| Deprovisioning | All access revoked within 4 hours of termination notice for involuntary terminations; same business day for voluntary terminations. |

## 4. Authentication Requirements

- Multi-factor authentication (MFA) is required for: all remote access, all administrative/privileged accounts, and all access to systems handling customer payment or PII data.
- Passwords must meet a minimum of 14 characters with no forced periodic rotation (rotation only required upon suspected compromise), consistent with NIST SP 800-63B guidance.
- Shared/generic accounts are prohibited except for documented service accounts, which must be vaulted and have no interactive login.

## 5. Privileged Access Management

- Privileged (admin-level) accounts are separate from standard user accounts — no individual uses an admin account for routine work (email, browsing, ticketing).
- All privileged session activity is logged and retained for a minimum of 1 year.
- Just-in-time elevation is preferred over standing privileged access where tooling supports it.

## 6. Exceptions

Any deviation from this policy (e.g., a vendor requiring standing access outside normal review cycles) requires written approval from the Security & GRC Team and is logged in the risk register (see `/risk-management/risk-register.md`) with a documented compensating control and review date.

## 7. Enforcement

Violations of this policy are handled per the Acceptable Use Policy and may result in access suspension pending investigation, in coordination with HR and Legal.

## 8. Policy Review

Reviewed annually, and following any access-related security incident.
