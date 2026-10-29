# CYBERSECURITY INTRO, WHAT IS A SOC

SN	TABLE OF CONTENT

1	Objective
2	Introduction
3	The CIA Triad
4	Threat vs Vulnerability vs Risk
5	What Is SOC/Purpose of SOC
6	L1, L2, L3 Analyst and their Responsibilities
7	Difference Between Blue Team and Red Team
8	Conclusion
9	Resources
10	TryHackMe rooms completed

# OBJECTIVE

The objective of this assignment is to master foundational cybersecurity principles and examine modern security operations. This assignment explores the CIA Triad and clarifies the distinct relationships between Threats, Vulnerabilities, and Risks. Additionally, it provides an in-depth look at the architecture of a Security Operations Center (SOC), detailing the operational roles of L1, L2, and L3 Analysts. Finally, this paper analyzes the mechanics of Incident Response and Threat Hunting, while contrasting the offensive and defensive strategies of Red Teams and Blue Teams.


# INTRODUCTION

Cybersecurity is no longer optional for modern organizations. To protect sensitive data, companies use a framework called the CIA Triad, which focuses on keeping data confidential, accurate, and accessible. Managing this security requires understanding how a Threat can exploit a Vulnerability to create a serious business Risk.

To manage these risks day in and day out, companies set up a Security Operations Center (SOC). The SOC is a dedicated team that monitors network traffic around the clock. This assignment looks closely at how a SOC functions, specifically focusing on the roles of L1, L2, and L3 analysts as they handle Incident Response and Threat Hunting. We will also explore the difference between the Blue Team (the defenders) and the Red Team (the attackers), and see how they work together to keep an organization secure.


THE CIA TRIAD

The CIA triad is a foundational cybersecurity model based on three core principles: Confidentiality, Integrity, and Availability. 
It is important because it serves as the ultimate blueprint for designing, auditing, and maintaining an organization's entire information security infrastructure. Rather than treating security as a series of random fixes, the triad forces organizations to view security through a structured framework that protects data from every angle.

**The Three Pillars**

1	Confidentiality:

•	Keeps sensitive data private and blocks unauthorized access.
•	Uses tools like encryption, multi-factor authentication (MFA), and access controls. 

2	Integrity:

•	Ensures data is accurate, complete, and trustworthy over its lifecycle.
•	Prevents accidental or malicious tampering using cryptographic hashing, digital signatures, and checksums.

3	Availability:

•	Guarantees that authorized users can access systems and data whenever needed.
•	Relies on redundancy, backups, disaster recovery, and DDoS protection. 

# Importance of CIA triad to modern cybersecurity:
1. Provides a Comprehensive Security Framework
   
The triad ensures that security teams don’t focus on one threat while leaving other doors wide open. Without it, a company might build massive walls to protect data privacy (Confidentiality) but completely forget to back up their servers, leaving them vulnerable to a system crash (Availability).

2. Helps Balance the "Security Trade-Offs"

Security is a constant balancing act. Maximizing one pillar often weakens another. The triad helps organizations weigh these trades-offs and find a balance. 

3. The Conflict: If you implement ten-factor authentication and strict encryption to maximize Confidentiality, you make data much harder to reach, hurting Availability.

4. The Solution: The triad helps security architects design a system that is secure enough to protect data but functional enough for employees to actually do their jobs.

5. Guides Risk Assessment and Compliance
   
Every business faces different threats. The triad allows organizations to categorize their data assets and prioritize their budget based on what matters most to their industry.
When a cyberattack happens, the CIA triad acts as a triage tool. It allows incident response teams to instantly categorize the breach and execute the right containment strategy:
Going one more step beyond the CIA security triad, we can think of:
•	Authenticity: Authentic means not fraudulent or counterfeit. Authenticity is about ensuring that the document/file/data is from the claimed source.
•	Nonrepudiation: Repudiate means refusing to recognize the validity of something. Nonrepudiation ensures that the original source cannot deny that they are the source of a particular document/file/data. This characteristic is indispensable for various domains, such as shopping, patient diagnosis, and banking.
These two requirements are closely related. The need to tell authentic files or orders from fake ones is indispensable. Moreover, ensuring that the other party cannot deny being the source is vital for many systems to be usable.
The opposite of the CIA Triad would be the DAD Triad: Disclosure, Alteration, and Destruction.
Consider the previous example of patient records and related systems:
•	Disclosure: As in most modern countries, healthcare providers must maintain medical records’ confidentiality. As a result, if an attacker succeeds in stealing some of these medical records and dumping them online to be viewed publicly, the health care provider will incur a loss due to this data disclosure attack.
•	Alteration: Consider the gravity of the situation if the attacker manages to modify patient medical records. This alteration attack might lead to the wrong treatment being administered, and consequently, this alteration attack could be life-threatening.
•	Destruction/Denial: Consider the case where a medical facility has gone completely paperless. If an attacker manages to make the database systems unavailable, the facility will not be able to function properly. They can go back to paper temporarily; however, the patient records won’t be available. This denial attack would stall the whole facility.

DIFFERENCE BETWEEN THREAT, VULNERABILITY AND RISK
There are three terms that we need to take note of to avoid any confusion.
•	Vulnerability: Vulnerable means susceptible to attack or damage. In information security, a vulnerability is a weakness.

•	Threat: A threat is a potential danger associated with this weakness or vulnerability.

•	Risk: The risk is concerned with the likelihood of a threat actor exploiting a vulnerability and the consequent impact on the business.
Consider this example directly related to information systems. You work for a hospital that uses a particular database system to store all the medical records. One day, you are following the latest security news, and you learn that the used database system is not only vulnerable but also a proof-of-concept working exploit code has been released; the released exploit code indicates that the threat is real. With this knowledge, you must consider the resulting risk and decide the next steps.



WHAT IS THE DEFINITION OF SOC AND ITS PURPOSE?
What is SOC?
A SOC (Security Operations Center) is a centralized unit or team of IT security professionals responsible for continuously monitoring, detecting, analyzing, and responding to cybersecurity threats across an organization's entire digital infrastructure. 
Purpose of a SOC
The primary purpose of a SOC is to protect an organization's sensitive assets—such as employee data, intellectual property, business systems, and brand reputation—from cyberattacks.
Its core functions divide into two main areas: 
•	Reactive Defense: Catching, investigating, and containing security incidents in real time (e.g., malware outbreaks, unauthorized access, or data breaches) before they cause major damage.

•	Proactive Defense: Continuously hardening networks, analyzing threat intelligence, managing security tools (like SIEM and EDR systems), and closing vulnerabilities so Continuously hardening networks, analyzing threat intelligence, managing security tools (like SIEM and EDR systems), and closing vulnerabilities so future attacks have fewer entry points.

•	24/7/365 Vigilance: Operating around the clock (often in shifts) because cyber threats occur at all hours, not just during standard business days. 






Responsibilities of L1, L2 and L3 Analyst
Tier	Role / Title	Core Responsibilities	Technical Skills & Focus

Tier 1 (L1)	Triage / Security Analyst	• Monitors SIEM alerts 24/7/365.
• Filters out false positives.
• Logs, categorizes, and prioritizes valid alerts.
• Escalates suspicious or complex threats to L2.	• High-level understanding of networks and OS.
• Familiarity with basic SIEM and EDR tool alerts.
• Follows standard operational playbooks.
Tier 2 (L2)	Incident Responder	• Investigates escalated alerts from L1.
• Determines the scope and depth of an attack.
• Executes containment and eradication protocols.
• Configures and tunes security rules.	• Deep knowledge of system forensics and logs.
• Proficiency in threat hunting and malware analysis.
• Strong understanding of attacker tactics (MITRE ATT&CK).
Tier 3 (L3)	Subject Matter Expert / Threat Hunter	• Proactively hunts for hidden threats missed by automated tools.
• Leads advanced forensics and reverse engineering.
• Develops incident response playbooks.
• Acts as a major incident commander during a breach.	• Advanced malware reverse-engineering.
• Scripting and automation (Python, PowerShell).
• Expert knowledge of architecture, cryptography, and cloud security.






DIFFERENCE BETWEEN BLUE TEAM AND RED TEAM
The fundamental difference between a Red Team and a Blue Team is their objective: 
The Red Team plays offense by simulating attackers to find security weaknesses. 
The Blue Team plays defense by monitoring, protecting, and defending the organization's infrastructure against attacks.
Together, they form a cooperative ecosystem known as Purple Teaming, where the insights gained from the Red Team's attacks are used directly by the Blue Team to harden the organization's overall security posture.

Direct Comparison: Red Team vs. Blue Team

Feature	 
Red Team (Offense)	 
Blue Team (Defense)
Primary Goal	Breach defenses and expose security vulnerabilities before real malicious actors do.	Protect organizational assets, detect active threats, and mitigate security breaches.
Mindset	Attacker/Adversarial: Creative, deceptive, and persistent.	Defender/Analytical: Vigilant, systematic, and process-driven.
Core Functions	• Penetration testing
• Social engineering (phishing, vishing)
• Physical security breaching
• Exploiting software vulnerabilities	• 24/7 Security operations (SOC)
• Incident response & containment
• Digital forensics & log analysis
• Patching & network hardening
Key Metrics	• Number of successful breaches
• Time taken to compromise a system
• Vulnerabilities discovered	• Mean Time to Detect (MTTD)
• Mean Time to Respond (MTTR)
• Reduction in successful breaches
Common Tools	Kali Linux, Metasploit, Nmap, Cobalt Strike, Burp Suite	SIEMs (Splunk, Microsoft Sentinel), EDR tools, Firewalls, Wireshark


CONCLUSION
Throughout this assignment, I explored core cybersecurity fundamentals, including the CIA Triad and the distinctions between Threats, Vulnerabilities, and Risks. Additionally, the research covered the definition and purpose of a Security Operations Center (SOC), alongside a detailed breakdown of the unique responsibilities held by L1, L2, and L3 SOC Analysts.



RESOURCES
TryHackMe rooms (Security Principles and Pentesting fundamentals)
Google








Prepared by: NITA ILEM

Cybersecurity Intern at TechBizAcademy

October 17, 2026






 


 

 
