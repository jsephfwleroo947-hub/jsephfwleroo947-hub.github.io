## Cyber Essentials and Cyber Essentials Plus

Cyber Essentials (CE) is a UK government-backed certification scheme that verifies an organisation has basic security controls in place, covering five areas: firewalls, secure configuration, access control, malware protection, and patch management. It's based on **self-assessment**, verified by an external assessor reviewing the organisation's answers.

**Cyber Essentials Plus (CE+)** covers the same five areas, but adds an **independent technical audit** — an assessor actively tests the organisation's systems (e.g. vulnerability scans, checking real device configuration) rather than relying on self-reported answers.

### The five controls in practice

| Control | What it actually requires |
|---|---|
| **Firewalls** | A properly configured firewall on every device and network boundary; default passwords on firewall admin interfaces must be changed; unnecessary services/ports blocked by default |
| **Secure configuration** | Removing or disabling unnecessary user accounts and software; changing all default passwords; disabling auto-run features that could launch malicious files without user action |
| **Access control** | Each user has their own account (no shared logins); admin/privileged accounts are only given to those who need them; multi-factor authentication (MFA) required for cloud services and admin access |
| **Malware protection** | Anti-malware software installed and kept up to date on all devices, or application allow-listing used instead to only permit approved software to run |
| **Patch management** | Security updates applied within 14 days of release for high/critical vulnerabilities; unsupported software (no longer receiving security updates) removed or isolated |

### Why the distinction matters

- CE demonstrates baseline awareness and policy — an organisation self-reports that these controls exist
- CE+ demonstrates that those policies are actually implemented correctly in practice, not just on paper — for example, an organisation could claim MFA is enforced for CE, but CE+'s technical audit would actively verify it's genuinely configured that way across real devices, rather than taking the claim at face value

This gap between "documented policy" and "verified practice" is a genuinely important distinction in security more broadly, not just within Cyber Essentials specifically — a policy that exists on paper but isn't actually enforced provides no real protection.

### Why this matters practically

For UK organisations, Cyber Essentials matters beyond compliance box-ticking:
- It's often a **contractual requirement** for bidding on UK government contracts
- It's increasingly requested by private clients as proof of basic security hygiene before doing business with a supplier
- The five controls themselves aren't arbitrary — they target the most common ways organisations are actually breached (unpatched systems, weak access control, missing MFA), meaning certification reflects genuine risk reduction, not just a badge to display

Understanding what each certification actually verifies — and what it doesn't — is practically useful knowledge for anyone working in UK IT or security, not just theoretical exam content.
