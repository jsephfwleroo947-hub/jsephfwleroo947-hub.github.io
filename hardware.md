# Inside a Computer

During my first MSP placement, I quickly learnt that understanding what is physically happening inside a computer is essential, even in this day and age. It's the foundation everything else in IT and cybersecurity sits on top of because you can't properly secure, troubleshoot, or explain an attack on a system you don't understand at a fundamental level. This section covers the core hardware components, what each one does, and how they work together.

## Where this comes from

During my IT MSP placement, I worked hands-on with laptop builds, which included fully disassembling and reassembling machines and wiping SSDs before redeployment. Taking a laptop apart down to its individual components (Rather than just reading about the parts)  made the relationship between hardware and software much more accessable to me. It's one thing to read that a CPU "processes instructions" but it's another to have the autonomy and responsability to physically hold the component and understand its place in the whole system.

## The core components

A useful comparison I came across on TryHackMe treats a computer like a body; each part has a distinct job, and the "body" only functions when they work together correctly.

| Component | Body analogy | What it actually does |
|---|---|---|
| **CPU (Central Processing Unit)** | Brain | Executes instructions and performs calculations - the component actually "thinking" and processing everything the computer does |
| **RAM (Random Access Memory)** | Short-term memory | Temporarily holds data and instructions the CPU is actively using; fast but wiped when powered off |
| **SSD/HDD (Storage)** | Long-term memory | Stores the operating system, applications, and files permanently, even when powered off |
| **Motherboard** | Nervous system/skeleton | Connects every component together, allowing them to communicate |
| **Power Supply Unit (PSU)** | Heart | Converts and delivers power to every component |
| **GPU (Graphics Processing Unit)** | Visual cortex | Handles rendering images/video; also used for parallel processing tasks beyond graphics |
| **Cooling system (fans/heatsinks)** | Sweat glands | Prevents components (especially the CPU) from overheating under load |
| **Peripherals (keyboard, mouse, screen)** | Senses/limbs | Input and output - how a user interacts with the machine |

## The boot process (briefly)

When a computer powers on:
1. **BIOS/UEFI** runs first = a small firmware program that checks hardware is present and functioning
2. It hands control to the **bootloader**, which locates the operating system
3. The OS loads into **RAM** and takes over, ready for user interaction

## Why this is relevent for security

Understanding hardware directly informs real security practice:
- **RAM (volatile memory)** can contain sensitive data like passwords or encryption keys while a system is running, which is why RAM analysis is a real forensic technique after an incident
- **Storage wiping** (like the SSD wipes I did during laptop builds) matters because deleted files aren't necessarily gone - improper wiping can leave recoverable data behind, a real risk when redeploying or disposing of devices
- **Firmware-level security (BIOS/UEFI)** is an attack surface - malware that infects the boot process can persist even through OS reinstalls, which is why boot security (e.g. Secure Boot) exists
- Knowing what's physically happening in a machine means you can reason about *where* an attack or vulnerability actually lives, as opposed to treating "the computer" as a black box
