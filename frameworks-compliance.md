# Frameworks & Compliance

Security frameworks and compliance standards exist to turn good security practice into something structured, verifiable, and consistent — rather than relying on individual judgement alone. This section covers the wider compliance landscape beyond Cyber Essentials (covered in Cybersecurity Fundamentals), including data protection law and broader security frameworks.

## Where this comes from

During my placement, I was involved in a **Microsoft Purview** project focused on data protection. The company handled extremely high-stakes client information, meaning data protection wasn't a background compliance exercise but a genuinely central part of daily operations. This gave me direct, practical exposure to what GDPR compliance actually looks like in practice — not just the legal principles, but the real tooling and processes organisations use to enforce them.

## GDPR and UK Data Protection

The UK GDPR (alongside the Data Protection Act 2018) governs how organisations must handle personal data. Key principles include:

| Principle | What it means in practice |
|---|---|
| **Data minimisation** | Only collecting the personal data actually necessary for a specific purpose, not gathering data "just in case" |
| **Purpose limitation** | Data collected for one purpose shouldn't be reused for an unrelated purpose without proper basis |
| **Storage limitation** | Personal data shouldn't be kept longer than necessary |
| **Individual rights** | Includes the right to access data held about you, the right to have it corrected, and the right to have it erased in certain circumstances |
| **Breach notification** | Organisations must report certain data breaches to the ICO (Information Commissioner's Office) within 72 hours of becoming aware of them |

**Microsoft Purview**, the tool I worked with, supports this practically — it allows organisations to classify and label sensitive data (e.g. marking documents as confidential), apply data loss prevention (DLP) policies to stop sensitive information leaving the organisation inappropriately, and track where sensitive data lives and how it's being used. Seeing this in practice made clear that data protection compliance isn't just a legal document — it requires real technical enforcement across every system handling that data.

## ISO 27001 (brief overview)

ISO 27001 is an international standard for an **Information Security Management System (ISMS)** — essentially a structured, ongoing process for identifying risks, implementing controls, and continually reviewing and improving an organisation's security posture. Unlike Cyber Essentials, which checks specific technical controls, ISO 27001 certifies the *management process* around security as a whole — how an organisation identifies risk, decides on controls, and keeps improving over time.

## NIST Cybersecurity Framework (brief overview)

The NIST CSF, though originating in the US, is widely referenced internationally as a common language for managing cybersecurity risk. It organises security activity into five core functions:
- **Identify** — understanding assets, risks, and vulnerabilities
- **Protect** — implementing safeguards (access control, training, etc.)
- **Detect** — identifying security events as they happen
- **Respond** — taking action during an incident
- **Recover** — restoring normal operations afterward

## How these fit together

- **Cyber Essentials/CE+** — baseline technical controls, UK-specific, often contractually required
- **GDPR/Data Protection Act** — legal requirement for handling personal data, not optional or framework-dependent
- **ISO 27001** — a broader management system covering how security is organised and continually improved
- **NIST CSF** — a functional way of thinking about security activities, useful regardless of which specific standard an organisation follows

An organisation typically isn't choosing just one of these — legal compliance (GDPR) is mandatory regardless, while frameworks like Cyber Essentials, ISO 27001, and NIST CSF are often layered together depending on sector, client requirements, and risk appetite.

## Why this matters

Frameworks and compliance requirements aren't bureaucratic overhead — they exist because ad hoc security, left to individual discretion, fails at scale. Seeing Purview used in a real high-stakes environment showed me that compliance is only meaningful when backed by actual technical enforcement, not just policy documents — the same principle that distinguishes Cyber Essentials from Cyber Essentials Plus.
