# Lab 6 : CEG 3400

## Risk

Table of contents:
* [Background and Objectives](LAB6-INSTRUCTIONS.md#background-and-objectives)
* [Rubric](LAB6-INSTRUCTIONS.md#rubric)
* [Preparation](LAB6-INSTRUCTIONS.md#preparation)
* [Introduction](LAB6-INSTRUCTIONS.md#introduction)
* [Task 1: Home sweet home](LAB6-INSTRUCTIONS.md#task-1-home-sweet-home)
* [Task 2: Platform Inventory](LAB6-INSTRUCTIONS.md#task-2-platform-inventory)
* [Task 3: Guess who](LAB6-INSTRUCTIONS.md#task-3-guess-who)
* [Task 4: Eventually](LAB6-INSTRUCTIONS.md#task-4-eventually)
* [Task 5: Impact](LAB6-INSTRUCTIONS.md#task-5-impact)
* [Task 6: Risky business](LAB6-INSTRUCTIONS.md#task-6-risky-business)

---

#### Background and Objectives

In this lab students will perform a risk assessment of their home network and online presence.

Students should become familiar with the following:

* preparing for a risk assessment (purpose, scope, assumptions, and approach)
* identifying a personal inventory / attack vectors
* identify threat actors (capability, intent, and targeting)
* identify threat events
* assign likelihood and impact scores to threat events
* rank risks and choose an appropriate risk response
* determine an overall risk profile of their organization

In preparation for this you should read chapters 1 through 3 of the 
[NIST 800-30](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-30r1.pdf)
special publication, and skim Appendices D through I.  The tables used in this lab
(D-3 through D-5, E-2 through E-4, G-2, H-3, I-2, and I-3) all come from those appendices.

---

#### Rubric
| Item | # Points|
| --- | --- |
| 10 commits | 10 |
| Good markdown style | 20 |
| Introduction | 10 |
| Task 1 | 20 |
| Task 2 | 20 | 
| Task 3 | 20 |
| Task 4 | 20 |
| Task 5 | 20 |
| Task 6 | 20 |

---

#### Preparation

This lab will require all work be done on your home network.

Purpose of this assessment: to familiarize students with basic risk assessment 
vocabulary and practices, and to identify any personal high risk items in need of 
mitigation.  Since this is an initial assessment the main goal is to establish a 
baseline assessment of risk as well as identify threats, vulnerabilities, and their
likely impact on you as a student.  For the purpose of this lab, *the organization* 
is a not so fictitious **Your Name Inc.** and the primary goal of this organization is
for you to graduate.

Scope of this assessment: This assessment should apply primarily to the student
submitting this lab.  Any other users of the same network can be included as part
of this assessment.

This risk assessment should include all devices that are owned by the student and a part
of the student's home network.  It can include any other devices on the network
that you have obtained permission to include in this document.

---

### Introduction

Every NIST 800-30 assessment begins by preparing for the assessment (Step 1, Section 3.1).
Before starting Task 1, write a short introduction paragraph for **Your Name Inc.** in your
`README.md`.  You may reuse the purpose and scope given above, but put them in your own words.

> In one or two paragraphs, address all of the following:
>
> * **Purpose:** why Your Name Inc. is conducting this assessment and what decisions it will inform.
> * **Scope:** which devices, accounts, people, and data are included, and what is excluded.
> * **Time frame:** how long these results are expected to remain valid.
> * **Assumptions and constraints:** what you are taking as given (for example, that
>   housemates are trusted, or that your ISP router is out of your control) and what
>   limits your assessment (time, permissions, knowledge).
> * **Analytic approach:** that you are using a qualitative assessment with 0-10 semi-quantitative
>   scores from the NIST 800-30 tables, and whether your analysis is threat-oriented,
>   asset/impact-oriented, or vulnerability-oriented (see Section 2.3.3).
> * **Reassessment:** at least one event that would cause Your Name Inc. to repeat this
>   assessment (for example, a new job, moving, or a breach of a critical account).

---

### Task 1: `/home` sweet `/home`

Identify the data and resources you are protecting.  This involves four steps:

1. With permission from the network owner, scan your network with `nmap` and 
   see how many devices are on your network (do not fully scan all systems, 
   just get a count/list).  If you live on campus or anywhere else that you do NOT have permission, 
   perform the below alternate assignment.
   * Manually count all networked devices you own, and estimate the number of devices that likely share the same network 
     (assume most people on average have a similar number of devices as you do).  List ***3*** dream devices that would assist you
     in completing your organization's goal of graduating.
2. Make a list of all online accounts you hold that have either a 
   credit card attached to them, or data for/about you beyond basic 
   directory information (name, email, title, general location are all directory info).  
   * If you prefer, keep this list private and provide a count of the accounts.
3. List all social media platforms you currently use.  Also, if you prefer, keep this list private and simply provide a count of the accounts ;) .
4. List any personal electronic devices that you own that may not have shown 
   up in an nmap scan.  Wearable electronics and home automation devices might be included here (bluetooth, zwave, zigbee, home automation, etc.).

With the above information gathered, write a report in the Task 1 section of your `README.md` detailing the following:

> Describe the results of your scan.  Be verbose and address all of the following:
>
> * What are all CIDR's in use in your home network?
> * A count of the number of devices that respond (alternative, estimate how many devices are on your floor AND in your building if you are not permitted to perform the scan).
> * Can you identify all devices on your network? [ALTERNATIVE: what would the CIDR need to be to house the above number of devices?]
>
> Describe your online presence detailing the following:
>
> * How many online accounts and social media platforms are you on
>   that hold non-trivial data about you?
> * How many of these are critical for your organization's business goals?  
> * How do you feel about the number of non-business critical accounts that have more than directory information about you?
> * Do you know the Authentication policies of these critical accounts?
>   * List all primary and secondary authentication methods for your most 
>     important account, including non password related reset options 
>     that might be vulnerable to an attacker.


---

### Task 2: Platform Inventory

Identify the following:

* Review the 5 real CPE's from lab 5 that make up your laptop software stack.
* Identify the most recent CVE that affects each of these software platforms (ideally from this year, looking for a total of 5 CVE's)
* The top [MITRE ATT&CK](https://attack.mitre.org/) *Reconnaissance* or *Initial Access* technique that is most concerning to your organization

Write a report on the following in your `README.md`

> * List your 5 platforms and the 5 CVE's you identified with CVSS scores.
> * Which of your CPEs has the most CVE's since Jan 1, 2024?  How many?
> * What is the highest CVSS score of any 2024 CVE related to one of your CPE's?  Link the CVE.
> * Why might having the CPE lookup for your most critical software be important
>   for an organization to mitigate risk?
> 
> List your most concerning MITRE ATT&CK technique and why you chose it

---

### Task 3: Guess who

Potential adversarial threat vectors include the following:
  
* Malicious software
* Insider Threats (trusted person with intent to do harm)
* Outsider threats including ALL of the following:
  * Hackers
  * Crackers
  * Script Kiddie
  * Cyber Criminals
  * Cyber Terrorists
  * Hacktivists
  * State-Sponsored attackers

NIST 800-30 characterizes adversarial threat sources by three factors:
*capability* (Table D-3), *intent* (Table D-4), and *targeting* (Table D-5).

> In your `README.md`, list all of the adversarial threat actors above that might have the capability to 
> perform your chosen MITRE ATT&CK technique and why you believe they have that capability.
>
> For each actor you listed, also describe:
>
> * **Intent:** would this actor actually *want* to attack Your Name Inc., and what would they hope to gain?  Use Table D-4.
> * **Targeting:** would this actor target *you specifically*, or would you only be hit as part of a broad,
>   untargeted campaign?  Use Table D-5.
>
> Which actor is the most realistic threat to your organization once capability, intent, and targeting are all considered?  Why?
>
> List the top three non-adversarial threat events of concern to your organization (from the NIST reading appendix E-3)
> and describe why they are of concern to you.

---

### Task 4: Eventually

Read through Table E-2 and E-3. Look up the following Threat Events and state their relevance
to your organization (see table E-4) and the likelihood of threat event occurring (table G-2).

Use a 0-10 scale.

#### Adversarial

* Perform perimeter network recon/scanning
* Perform network sniffing
* Craft spear phishing attack
* Exploit poorly configured or unauthorized information systems exposed to the internet
* Exploit recently discovered vulnerabilities
* Conduct simple Denial of Service attacks
* Cause integrity loss by injecting false but believable data into org info systems
* Cause unauthorized disclosure and/or unavailability by spilling sensitive information
* Obtain sensitive data/info from publicly accessible information systems
* Obfuscate adversary actions

#### Non-adversarial

* Mishandling of critical and/or sensitive information by authorized users
* Communications contention
* Unreadable display
* Natural disaster at primary facility
* Introduction of vulnerabilities into software products
* Disk error

> Record your likelihood scores in the threat event table in your `README.md`, then answer:
>
> 1. List one other threat event that is likely and of concern to your organization.
> 2. Why did you choose this threat event?
> 3. Were there any other threat events that your organization should be concerned about?
> 4. What are the pros and cons of using a list of threat events such as the one included
>    in the NIST 800-30 tables E-2 and E-3?

---

### Task 5: Impact 

Measure the impact of each of the above threat events using the 0-10 scale found in 
table H-3.

> Record your impact scores in the threat event table in your `README.md`, then answer:
>
> 1. Which threat events were hardest to determine the likelihood and impact for?  Why?

---

### Task 6: Risky business

Using table I-2 assign a level of risk (0-10) based on the *Likelihood* and *Impact* 
of each threat event.  Look up the qualitative risk level in table I-2, then convert it
to a 0-10 value using table I-3.

> Record your risk scores in the threat event table in your `README.md`, then answer:
>
> 1. Add up all numbers in your risk column and list it here.
> 2. Rank your top five risks from highest to lowest.  For each, give its risk score and
>    explain any ties you had to break.  Which of these exceed what Your Name Inc. is willing
>    to tolerate (its *risk tolerance*)?
> 3. For your highest ranked risk, choose a risk response: **accept**, **avoid**,
>    **mitigate**, or **transfer/share**, and justify your choice.  If you choose to mitigate,
>    develop one strategy / policy / purchase to mitigate this threat event and describe it
>    (and how or why it reduces the likelihood or impact of that event).
> 4. What was the hardest part of this assessment (for you) and why?
