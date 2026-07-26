# Systems Administration

Systems administration is the continuous maintenance of an organisation's devices, accounts, and access secure and functional. A lot of real-world security comes down to sysadmin discipline: patched systems, correctly scoped access, and enforced policy, rather than any single defence.

## Where this comes from

During my cybersecurity placement, a key focus was routine patch management; applying security updates to fix known vulnerabilities and bugs before they could be exploited. I also worked hands-on with Active Directory as an administrator, including configuring conditional access policies, managing privileged access, and applying Group Policy rules. I used Microsoft Entra to check whether company devices were up to date, properly configured, and conforming to company policy, giving me direct exposure to how organisations manage device compliance at scale, rather than relying on individual users to keep their own machines updated.

## Core concepts

| Term | What it means |
|---|---|
| **Active Directory (AD)** | Microsoft's directory service for managing users, devices, and permissions across a network from a central point |
| **Microsoft Entra** | Cloud-based identity and access management, used to manage sign-ins, device compliance, and policy enforcement across an organisation's devices |
| **Conditional Access** | Rules that grant or block access based on context e.g. requiring multi-factor authentication if a sign-in comes from an unfamiliar location or device |
| **Group Policy** | A set of rules applied to users/devices within AD to enforce consistent configuration (e.g. password requirements, restricted settings) across an organisation |
| **Privileged Access** | Elevated permissions (e.g. admin rights) that allow greater control over a system - carefully restricted since compromised privileged accounts cause the most damage |
| **Least Privilege** | The principle that users/systems should only have the minimum access necessary to do their job, reducing the impact if an account is compromised |
| **Zero Trust** | A security model based on "never trust, always verify" - no user or device is trusted by default, even if already inside the network, and access is continuously verified |
| **Patch Management** | The process of regularly applying updates to fix known vulnerabilities, bugs, and security flaws in software and operating systems |

## How this works in practice

 All of these work together:
- **Least privilege** limits what an account can do
- **Conditional access** adds context-aware checks on top of that (device, location, risk level)
- **Zero trust** ties both together as an overarching philosophy; assume breach is always possible, and verify constantly rather than trusting anything by default just because it's "inside" the network
- **Patch management and device compliance checks (via Entra)** ensure the devices themselves aren't a weak point, regardless of how well access is otherwise controlled

## Relevance to security

- **Unpatched systems are one of the most common real-world breach causes** - many major incidents exploit known vulnerabilities that had a patch available but hadn't been applied yet, which is exactly why routine patching was a priority during my placement
- **Privileged accounts are high-value targets** - attackers specifically seek out admin credentials, which is why least privilege and careful management of privileged access directly reduce risk
- **Conditional access and device compliance checks** mean access isn't just "username and password" - a compromised password alone doesn't guarantee an attacker gets in, if the device or context doesn't also meet policy
- **Zero trust reflects how modern organisations actually operate** ; with remote work and cloud services, there's no longer a clearly defined "inside" the network to trust by default
