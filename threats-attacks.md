# Common Threats & Attacks

Understanding threats in the abstract is useful, but seeing them show up in real alerts and logs is what makes them concrete. This section covers common attack types, including ones I've directly observed and responded to during my cybersecurity placement, alongside the broader threat landscape and how it continues to evolve.

## Where this comes from

Working with real monitoring tools exposed me to genuine attack attempts, not just theoretical examples — including suspicious sign-ins from unexpected countries, brute force login attempts, and the ongoing need to actively encourage good security hygiene among end users to prevent social engineering from succeeding in the first place.

## Impossible travel / anomalous sign-ins

One pattern I saw directly was customer/user logins originating from countries far outside their normal usage pattern — sometimes referred to as "impossible travel" (e.g. a login from the UK followed shortly after by one from another continent, which isn't physically plausible). This is a strong signal of a compromised account, since it suggests someone other than the legitimate user has valid credentials. Tools like Defender flag this automatically by comparing sign-in location/time against a user's normal behaviour baseline.

## Brute force attacks

A brute force attack is where an attacker repeatedly attempts logins — either guessing passwords systematically or using previously leaked credentials (credential stuffing) — until one succeeds. In practice, I saw these attempts identified and stopped through **throttling**: limiting the number of login attempts allowed within a time window, which makes brute forcing impractical without blocking legitimate users outright. This is a good example of a control that's simple in concept but genuinely effective at scale.

## Social engineering

Social engineering targets people rather than technical systems — manipulating someone into bypassing security controls voluntarily (e.g. clicking a malicious link, revealing a password, approving a fraudulent request). Because this targets human behaviour rather than a technical flaw, technical controls alone can't fully prevent it. Part of the work I was involved in was actively encouraging better practice among end users, since awareness and good habits are a genuine part of the defence, not just a "nice to have" alongside technical controls.

## Password hygiene

Closely related, poor password hygiene (reused passwords, weak passwords, sharing credentials) directly increases the risk of the above threats succeeding — a brute force attempt is far more likely to succeed against a weak or reused password, and a leaked password from one breach becomes a real risk everywhere it's reused. Encouraging strong, unique passwords (or better, passwordless/MFA-based authentication) is a simple but genuinely high-impact control.

## Phishing and its variants

Phishing is deceptive communication designed to trick someone into revealing credentials, approving a fraudulent request, or installing malware. It's evolved well beyond just email:
- **Phishing** — the classic form, typically via email, often impersonating a trusted sender
- **Smishing (SMS phishing)** — the same tactic delivered via text message, often impersonating a delivery service, bank, or even an organisation's own IT department; effective partly because people are less naturally suspicious of texts than emails
- **Vishing (voice phishing)** — carried out over phone calls, sometimes combined with caller ID spoofing to appear legitimate
- **Spear phishing** — a targeted version aimed at a specific individual or organisation, using personal/organisational detail to appear more convincing than a generic mass attempt

The common thread across all variants is exploiting trust and urgency rather than a technical vulnerability, which is why user awareness remains essential regardless of the delivery method.

## Malware (brief)

Malicious software that, once installed, can steal data, provide ongoing unauthorised access, or cause direct damage. Common categories include ransomware (encrypting data and demanding payment), spyware (covertly monitoring activity), and trojans (disguised as legitimate software).

## Keeping up with an evolving threat landscape

Attack methods don't stay static, which means understanding today's threats isn't enough on its own — genuine cybersecurity competence includes staying aware of how attacks are changing. One of the most significant shifts currently is the use of **AI in both attacking and defending**:

- **Lowering the barrier to entry** — AI tools can help less skilled attackers ("script kiddies") generate more convincing phishing messages, basic malware variants, or automate parts of an attack that previously required real technical skill
- **Increasing sophistication at the top end** — more advanced attackers use AI to generate highly convincing deepfake audio/video for vishing-style attacks, write more evasive malware, or automate reconnaissance against a target at a scale manual effort couldn't match
- **AI in defence too** — the same shift applies to tools like Copilot for Security, which uses AI to help analysts triage and investigate faster, showing that this isn't a one-sided arms race

This matters practically: a portfolio or skillset that only reflects "traditional" threats risks going stale quickly. Keeping up with how attacks evolve, rather than treating security as a fixed list of known threats, is part of genuinely understanding the field rather than just memorising it at a point in time.

## Why this matters

Seeing these patterns firsthand made clear that most real-world attacks aren't especially sophisticated — brute forcing and social engineering succeed because of gaps in basic hygiene (weak passwords, lack of awareness) rather than advanced technical exploits. At the same time, the threat landscape is genuinely shifting with AI lowering the skill bar for attackers while also raising the ceiling for sophisticated ones. This is exactly why the fundamentals covered earlier in this portfolio — least privilege, MFA/conditional access, patch management, monitoring — matter so much in practice: they close off the easy, common routes attackers actually use, while staying aware of new trends keeps that defence from becoming outdated.
