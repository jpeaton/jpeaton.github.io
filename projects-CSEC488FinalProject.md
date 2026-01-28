---
layout: default
title: CSEC 488 Final Project: CTF and Pen Test Report
permalink: /projects/CSEC488FinalProject
---

# Project Overview

This project is my **solo final lab for CSEC 488**, delivered as a Capture the Flag (CTF)–style engagement that simulates a real penetration test—except instead of dramatic music, it’s mostly terminal output and quiet reflection. The mission: compromise multiple target systems in a controlled lab environment and retrieve flags using realistic, entry-level offensive security techniques.

The operating mode was **locked in**, **no script-kiddie behavior**, **brain fully online**. This wasn’t a speedrun exercise—it was a methodical, exam-condition engagement focused on doing things *the right way*. This overview stays intentionally high-level so it doesn’t accidentally turn into an academic integrity incident.

---

## Scope & Environment

* **Engagement Type:** Academic CTF / simulated penetration test
* **Targets:** Multiple isolated systems in a private lab network (mixed OSes, mixed services)
* **Constraints:**

  * Solo engagement (me vs. the machines)
  * Time-bound final exam
  * Required recon → analyze → exploit → validate workflow

No button-mashing. No tool spamming. Just professional curiosity and patience.

## Engagement Context

This entire project was conducted against a fictional organization with me acting as a simulated third-party penetration testing vendor.

The framing mirrored a real consulting-style engagement:

* The target environment represented a client-owned network and systems.

* I operated as an external tester, not an internal administrator.

* All findings, actions, and reporting were scoped to what a contracted penetration testing firm would be authorized to perform.

This perspective influenced both the technical approach and the documentation style—treating the work as a client-facing assessment rather than an internal lab exercise.

---

## Tools & Technologies Used

### Core Tooling

* **Nmap** – Host discovery, port scanning, service enumeration (industry standard, still goated)
* **Dirb / directory discovery tools** – Surfacing web content that probably shouldn’t be public
* **Metasploit Framework** – Exploit research and controlled execution
* **Linux (Kali / Ubuntu)** – Attacker environment
* **Windows & Linux systems** – Target environments

### Supporting Concepts

* CVE research and vulnerability validation
* Credential discovery and reuse analysis
* File system enumeration and privilege boundary awareness
* Command-line tooling and light scripting for verification

---

## Methodology & Approach

I followed a structured penetration testing workflow—the kind that doesn’t fall apart outside a classroom:

1. **Recon & Enumeration**

   * Identified live hosts and exposed services
   * Enumerated ports, versions, and reachable web content

2. **Vulnerability Analysis**

   * Translated scan output into actual hypotheses
   * Researched CVEs and common misconfiguration patterns

3. **Exploitation (Intentional, Not Reckless)**

   * Used only techniques aligned with learning objectives
   * Avoided automation-for-the-sake-of-automation behavior

4. **Post-Exploitation Awareness**

   * Validated access levels responsibly
   * Enumerated artifacts relevant to flag discovery
   * Clearly separated user access from elevated privileges

5. **Documentation**

   * Tracked findings per system
   * Left notes for future-me (a real stakeholder)

---

## Final Deliverable: Written Report

In addition to the hands-on lab work, this project concluded with a formal written report documenting the engagement at a professional level.

The report was structured to mirror how real penetration testing or security assessment findings are communicated to stakeholders:

* **Engagement overview and scope definition**

* **High-level methodology** used across all target systems

* **Summarized findings per system** (without unnecessary technical noise)

* **Clear separation** between discovery, validation, and outcomes

* **Professional tone and formatting**, suitable for non-technical readers as well as technical reviewers

Rather than serving as a step-by-step exploit guide, the report focused on **clarity, reasoning, and risk context**—explaining what was discovered, why it mattered, and how it fit into the overall security posture of the environment.

This deliverable reinforced the idea that strong security work isn’t finished when access is obtained—the real value is in how clearly findings are documented, communicated, and contextualized.

---

## What I Did (High-Level)

* Performed full network and service enumeration across all assigned targets
* Identified exposed services and exploitable misconfigurations
* Discovered credentials through enumeration and analysis (no brute force, no guessing)
* Validated access paths and retrieved required flags
* Managed multiple attack paths without losing scope, logic, or sanity
* Authored a formal, client-facing penetration testing report documenting scope, methodology, high-level findings, and outcomes in a professional format

---

## Skills Demonstrated

* **Offensive Security Fundamentals** – Recon, exploitation, validation
* **Analytical Thinking** – Turning raw scan data into decisions
* **Tool Maturity** – Knowing when *not* to run things
* **Ethical Judgment** – Staying inside rules of engagement
* **Technical Communication** – Documentation that explains *why*, not just *what*

---

## Learning Outcomes

Hard truths reinforced by this project:

* Enumeration carries harder than exploits
* Misconfigurations are the main character
* Tools don’t replace understanding (unfortunately)
* Notes are OP

This lab bridged classroom theory and real-world attacker mindset—especially around patience, restraint, and methodical execution.

---

## Career Relevance

This project aligns with expectations for:

* Security Analyst roles
* SOC Analyst positions
* Junior Penetration Testing roles
* IT / Infrastructure roles with security ownership

The emphasis on structure, judgment, and documentation reflects how actual security teams operate. No chaos, no shortcuts, no ego.

---

## Academic Integrity Note

Specific exploits, commands, flags, IP addresses, and step-by-step solutions are intentionally excluded to comply with course policy and preserve academic integrity. This overview focuses on **process, skills, and outcomes**, not answers.

---
