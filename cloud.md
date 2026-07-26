# Cloud Computing

Cloud computing has massively changed how organisations run their IT operations. Instead of maintaining all infrastructure on-site, businesses increasingly rely on remote, provider-managed services. Understanding why this shift happened, and the different models of cloud service, is crucial context for any modern IT or security role.

## Where this comes from

My direct hands-on cloud experience so far has been through Microsoft Entra, used for identity management and device compliance checks. Beyond that, my understanding of cloud computing comes from seeing, across placements, how much of modern IT and security tooling is now cloud-based by default rather than an optional add-on. Identity, device management, and monitoring are increasingly run from the cloud rather than on local servers.

## Why organisations move to the cloud

- **Scalability** - resources can be increased or decreased on demand, without needing to buy and install physical hardware in advance
- **Cost efficiency** - shifts spending from large upfront hardware costs to ongoing operational costs, and avoids paying for unused capacity
- **Security** - major cloud providers invest heavily in security infrastructure that most individual organisations couldn't replicate on their own, though this comes with a shared responsibility (see below)
- **Collaboration** - cloud-based tools allow teams to access and work on the same systems/data from anywhere, rather than being tied to a physical office network

## Service models

| Model | What the provider manages | What the customer manages | Example |
|---|---|---|---|
| **IaaS (Infrastructure as a Service)** | Physical hardware, virtualisation, networking | Operating system, applications, data | Virtual machines (e.g. Azure VMs, AWS EC2) |
| **PaaS (Platform as a Service)** | Infrastructure + OS + runtime environment | Applications and data only | App development platforms (e.g. Azure App Service) |
| **SaaS (Software as a Service)** | Everything - infrastructure through to the application itself | Just the data and how it's used | Microsoft 365, Entra, Google Workspace |

The general pattern: moving from IaaS toward SaaS means less to manage yourself, but also less direct control. This is a trade-off organisations weigh depending on their needs.

## Shared responsibility

Cloud security isn't purely the provider's job because even with a secure cloud platform underneath, the customer is typically still responsible for things like access control, data classification, and correctly configuring the services they use. A well-secured cloud platform can still be compromised through poor configuration on the customer's end. This is a common real-world cause of cloud breaches, not a flaw in the cloud provider itself.

## Relevance to security

- **The shift to cloud changes the attack surface** - instead of securing a physical perimeter, organisations now need to secure identity and access, since that's often the real "front door" (tying directly back to conditional access and Entra device compliance covered earlier)
- **Misconfiguration, not the provider, is the most common cloud security failure** - understanding shared responsibility means knowing where your own responsibility actually starts
- **Collaboration tools widen the attack surface too** - more access points and integrations mean more potential entry points, which is why identity-based security (rather than just network-based) has become the priority
