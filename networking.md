# Networking

Networking is how individual machines become part of a functioning system. Understanding networking fundamentals, from the physical cable up to how traffic is controlled and segmented, is essential for both IT support and security, since almost every attack and every defence involves the network in some way.

## Where this comes from

Across both my IT MSP and cybersecurity placements, I did hands-on structured cabling work: cutting and crimping PoE (Power over Ethernet) cables, arranging the wire pairs in the correct order, fitting connectors, testing continuity, and then implementing the cables into the live network. This gave me a genuinely physical understanding of networking: a "connection" isn't just a line on a diagram, it's real cabling that has to be correctly terminated to function at all, let alone securely.

I also oversaw, during my MSP placement, the implementation of a firewall used to segment the MSP's network from other companies operating in the same building, as well as from the building's CCTV service — a practical example of network segmentation as a real security control.
## Core concepts

| Term | What it means |
|---|---|
| **LAN (Local Area Network)** | A network confined to one physical location, e.g. an office or building |
| **WAN (Wide Area Network)** | A network spanning multiple locations, typically connecting LANs together over larger distances (e.g. the internet itself) |
| **VLAN (Virtual LAN)** | A logically separated network within the same physical infrastructure: allows traffic separation (e.g. staff devices vs guest Wi-Fi) without needing separate physical cabling |
| **Subnetting** | Dividing a network into smaller sub-networks, improving organisation, performance, and security by limiting broadcast traffic and containing potential breaches |
| **DNS (Domain Name System)** | Translates human-readable domain names (e.g. google.com) into IP addresses computers actually use to communicate |
| **DHCP (Dynamic Host Configuration Protocol)** | Automatically assigns IP addresses to devices joining a network, rather than requiring manual configuration on each device |
| **Router** | Directs traffic between different networks (e.g. between a LAN and the internet) |
| **Switch** | Connects devices within the same network, forwarding traffic only to the intended device rather than broadcasting to all |
| **Ports and protocols** | Ports identify specific services on a device (e.g. port 443 for HTTPS); protocols define the rules for how data is exchanged (e.g. TCP for reliable delivery, UDP for speed over reliability) |

## Firewalls and segmentation

A firewall controls what traffic is allowed to pass between networks, based on defined rules, typically operating on a "default deny" basis, where only explicitly permitted traffic is allowed through.

The firewall implementation I oversaw at my MSP placement is a real-world example of this: separating the MSP's own network traffic from other companies in the same building, and from the CCTV system, meant that even if one network was compromised, it couldn't automatically reach the others. This is the core principle behind **network segmentation**, reducing the "blast radius" of any single security incident.

## Relevence to security

- **Physical layer matters** - a badly terminated cable isn't just an inconvenience, in some cases (e.g. exposed wiring, unsecured patch panels) physical network access is itself a security risk
- **Segmentation limits damage** - separating networks (via VLANs or firewalls, as with the MSP/CCTV example) means a breach in one area doesn't automatically compromise everything else
- **DNS and DHCP are common attack targets** - DNS spoofing and rogue DHCP servers are real techniques attackers use to redirect or intercept traffic, which is why understanding normal behaviour matters for spotting abnormal behaviour
- **Firewalls are only as good as their rules** - a firewall with overly permissive rules provides a false sense of security, which is why the specific configuration matters as much as having one at all
