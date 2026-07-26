# Security Operations

Throughout my Cybersecurity placement, I thoroughly enjoyed seeing how security operations becomes daily practice. This was carried by means of monitoring systems, investigating alerts, and responding to incidents in real time. This section covers how a SOC (Security Operations Centre) functions, the incident response lifecycle, and my own hands-on experience working through real alerts and incidents.

## Where this comes from

I was directly involved in multiple meetings regarding the selection of a new SOC provider, which gave me real insight into what actually distinguishes a good SOC from an adequate one - not just theoretical knowledge of what a SOC does, but the practical considerations that go into choosing one (coverage, response times, escalation processes, and the difference true 24/7/365 surveillance makes versus more limited monitoring windows).

Beyond that, I was talked through the incident response lifecycle using both **Microsoft Defender** and **Huntress**, and given real autonomy to work through alert triage and incident handling myself, including following incidents through to eradication and educating end users, not just identifying and containing them.

## What a SOC actually does

A SOC is responsible for continuous monitoring, detection, and initial response to security events across an organisation. Key considerations that distinguish SOC quality:
- **Coverage model** 🡢 true 24/7/365 monitoring versus business-hours-only coverage; threats don't wait for office hours, so gaps in coverage are gaps in real protection
- **Response time (SLAs)** 🡢 how quickly an alert is triaged and escalated matters as much as whether it's caught at all
- **Analyst tiering** 🡢 SOCs typically use tiered analysts (Tier 1 handling initial triage, escalating complex cases to Tier 2/3), which affects how quickly and accurately incidents get properly investigated
- **Tooling and integration** 🡢 how well a SOC's tools integrate with an organisation's existing systems (e.g. Defender, Huntress) affects both detection accuracy and response speed

While obviously factoring in cost, selecting a SOC provider is about evaluating whether their coverage, speed, and process match the organisation's actual risk level.

## The incident response lifecycle

A structured response, rather than ad hoc reaction, is what separates effective incident handling from just "fixing the immediate problem":

1. **Preparation** 🡢 having tools, processes, and training in place before an incident happens
2. **Identification** 🡢 detecting and confirming that an incident is actually occurring
3. **Containment** 🡢 limiting the spread/impact of the incident (e.g. isolating an affected device)
4. **Eradication** 🡢 removing the actual root cause, not just the symptoms
5. **Recovery** 🡢 restoring affected systems to normal operation safely
6. **Lessons learned** 🡢 reviewing what happened and improving processes/defences to prevent recurrence

**Eradication in particular is a step that's easy to underweight.** Containing an incident stops it from spreading, but doesn't mean the threat is gone. If the root cause isn't properly eradicated, the same incident can recur, sometimes worse, once containment measures are lifted. This was something I saw emphasised directly while working through incidents in Defender and Huntress: containment buys time and limits damage, but the job isn't done until eradication is confirmed.

## Alert triage in practice

Not every alert represents a genuine incident. A large part of SOC/analyst work is **triage**: assessing which alerts are real threats requiring action, which are false positives, and which need escalation. Using Defender directly, I worked through this process myself, investigating alerts, determining appropriate action, carrying incidents through to eradication, and following up with end-user education where relevant (e.g. explaining to a user why a particular action triggered an alert, and what to avoid going forward). Being given real autonomy in this process meant learning to make genuine judgement calls, not just following a fixed script.

## Why this is relevant

Security operations is where all the earlier fundamentals like network segmentation, least privilege, patch management, CIA triad actually get tested in real time. A well-designed system with strong policies still needs active monitoring and a properly followed incident response process to be genuinely effective; prevention reduces risk, but detection and response are what determine the actual impact when something does get through.
