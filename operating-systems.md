# Operating Systems

An operating system is the layer that sits between hardware and the user, managing everything from memory and storage to running applications and controlling who can access what. Understanding how different operating systems approach these jobs — and why they differ — is core to working in IT, since every environment you touch will run on top of one.

## Where this comes from

During my IT MSP placement, after wiping SSDs on old laptops, part of the process was reconfiguring some of these devices with ChromeOS to be donated to charity rather than scrapped. This meant going from a full Windows install to a lightweight, cloud-first OS built around completely different assumptions — minimal local storage, browser-based everything, near-instant boot times. Seeing the same hardware run two fundamentally different operating systems side by side made the differences between them much more concrete than reading about them in the abstract.

## What an operating system actually does

Regardless of which OS, every one is responsible for the same core jobs:
- **Process management** — deciding what runs, when, and how CPU time is shared between programs
- **Memory management** — allocating RAM to running applications and reclaiming it when no longer needed
- **File system management** — organising how data is stored, read, and written on disk
- **Access control** — determining what users and programs are allowed to do

## Comparing OS types

| OS | Common use case | Notable traits |
|---|---|---|
| **Windows** | Business/enterprise, general consumer | Widest software compatibility, most targeted by malware due to market share, familiar GUI |
| **macOS** | Creative industries, general consumer | Tightly controlled hardware/software ecosystem (Apple builds both), often perceived as "just works" but with real limitations — less flexible for customisation, historically weaker gaming/enterprise software support, and a reputation among some users that's more about ecosystem lock-in than pure technical superiority |
| **Linux** | Servers, developers, security tooling | Open source, highly customisable, but often has a steeper learning curve for newcomers — command-line reliance and fragmented distributions (Ubuntu, Debian, Fedora, etc.) can be a real barrier despite being extremely powerful and lightweight |
| **ChromeOS** | Education, budget/charity devices, cloud-first use | Built around browser-based use and cloud storage rather than local installs, meaning it can breathe new life into older or lower-spec hardware — exactly why it suited the donated laptops from my placement |

## File systems and permissions (brief)

Different OSes also handle storage differently:
- **Windows** typically uses **NTFS**, with permissions managed through user/group access control lists
- **Linux/macOS** typically use **ext4** or **APFS**, with a simpler owner/group/other permission model (read, write, execute)

Understanding this matters practically — permission misconfigurations are a common real-world vulnerability, regardless of which OS is involved.

## Why this matters for security

- **Attack surface differs by OS** — Windows' large install base makes it the most common malware target, but that doesn't mean other OSes are inherently safer, just less frequently targeted
- **Permissions models** directly affect what an attacker can do if they gain access — a properly configured least-privilege system limits damage even after a breach
- **Lightweight/cloud-first OSes** (like ChromeOS) reduce local attack surface by design, since less sensitive data sits on the device itself — a real security advantage, not just a cost-saving one
- Being comfortable across multiple OS types matters practically too — an IT/security role rarely lets you stick to just one environment
