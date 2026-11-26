# Google Cybersecurity Professional Certificate Portfolio

Welcome to my Cybersecurity Portfolio! This repository documents my hands on projects/labs completed and technical skills obtained as part of the Google Cybersecurity Professional Certificate.

---

## Table of Contents
1. [Professional Statement (Lab 1)](#1-professional-statement)
2. [Conducting a Security Audit (Lab 2)](#2-conducting-a-security-audit)
3. [Analyzing Network Structure and Security using NIST CSF (Lab 3)](#3-analyzing-network-structure-and-security)
4. [Using Linux Commands to Manage File Permissions](#4-using-linux-commands-to-manage-file-permissions)
5. [Applying Filters to SQL Queries](#5-applying-filters-to-sql-queries)
6. [Identifying Vulnerabilities for a Small Business](#6-identifying-vulnerabilities-for-a-small-business)
7. [Documenting Incidents with an Incident Handler’s Journal](#7-documenting-incidents-with-an-incident-handlers-journal)
8. [Importing and Parsing a Text File in Python](#8-importing-and-parsing-a-text-file-in-python)

---

### 1. Professional Statement

Driven by my passion for digital innovation and software systems engineering, I am completing the Google Cybersecurity Professional Certificate to bridge the gap between complex engineering software systems and secure operational design. Building on my background in technical program management, R&D engineering, and software development, I am excited to learn and master the core security methodologies including applying the NIST Cybersecurity Framework, building SecOps integrated software architectures, auditing network architectures, managing access controls in Linux, and leveraging SQL and Python for threat investigations. I am also completing this to prepare for the CompTIA Security+ certification exam.

<p align="center">
  <span style="pointer-events: none;">
    <img src="assets/images/Google Cybersecurity Professional Certificate.png" alt="Google Cybersecurity Professional Certificate" width="700"/>
  </span>
</p>

<div align="center" style="line-height: -1.0;">
  <sub>📜 <em><a href="https://www.coursera.org/professional-certificates/google-cybersecurity">Google Cybersecurity Professional Certificate</a></em> 🔒</sub><br />
  <sub><em>(Ctrl + click or scroll-click to open link in a new tab)</em></sub>
</div>

<p align="center"><br /></p>

<p align="center">
  <span style="pointer-events: none;">
    <img src="assets/images/CompTIA Security.webp" alt="CompTIA Security+ Certificate" width="200"/>
  </span>
</p>

<div align="center" style="line-height: -1.0;">
  <sub>📜 <em><a href="https://www.comptia.org/en-us/certifications/security">CompTIA Security+ Certificate</a></em> 🔒</sub><br />
  <sub><em>(Ctrl + click or scroll-click to open link in a new tab)</em></sub>
</div>

---

### 2. Conducting a Security Audit

#### 2.1 Project Title
**Internal Security Audit & Controls Assessment (Botium Toys) - Lab 2**

#### 2.2 Project Introduction
I conducted an internal security audit for Botium Toys, a retail business expanding into international e-commerce. The audit identified critical security gaps such as unrestricted data access, missing data backups, unencrypted payment data, and nominal password policies that expose the company to operational disruptions, asset loss, and regulatory/compliance fines.

#### 2.3 Modeling and Evaluation
I evaluated the company's security posture using the **National Institute of Standards and Technology Cybersecurity Framework (NIST CSF)** and audited operations against key industry compliance standards:

* **NIST CSF & Internal Controls:** * **Access Controls:** Identified significant gaps, including lack of least privilege enforcement, missing Multi-Factor Authentication (MFA), and unbacked nominal password policies.
  * **Technical Controls:** Perimeter firewalls and antivirus software are active, but an Intrusion Detection System (IDS), data encryption, and centralized log management are missing.
  * **Administrative Controls:** Found no formal Disaster Recovery Plan (DRP), data backup schedule, or regular legacy maintenance framework.
  * **Physical Controls:** On-premises facilities are well secured with sufficient physical locks, CCTV surveillance, and fire detection/prevention systems.
* **Compliance Assessment:**
  * **Payment Card Industry Data Security Standard (PCI DSS) [Not Compliant]:** Credit card transactions are processed, transmitted, and stored internally without encryption, access restriction, or secure password policies.
  * **General Data Protection Regulation (GDPR) [Not Compliant]:** While a 72 hour breach notification plan exists, E.U. customer PII/SPII is unencrypted and accessible to all staff without asset classification controls.
  * **System and Organization Controls (SOC 1 / SOC 2) [Not Compliant]:** User access policies, separation of duties, and privacy controls are absent, despite active data availability and integrity mechanisms.

#### 2.4 Business & Legal Risks Identified
1. **Regulatory/Compliance Fines:** Failing to encrypt cardholder and PII/SPII data violates PCI DSS and GDPR mandates, exposing the business to financial penalties and class action lawsuit risks.
2. **Operational Interruption & Downtime:** The absence of a formalized DRP and data backups leaves the company vulnerable to unrecoverable data loss during security incidents.
3. **Insider Threat & Unchecked Data Exposure:** Allowing all employees broad access to sensitive records significantly elevates internal data leakage risks.
4. **Contractual & Audit Vulnerability:** Inadequate access logging and missing SOC 1 / SOC 2 standards limit operational transparency.

#### 2.5 Conclusion & Recommendations
**Key Recommendations:**
  1. **Enforce RBAC & Least Privilege:** Restrict user access based on job roles to protect customer PII/SPII and cardholder data.
  2. **Deploy End-to-End Encryption:** Encrypt cardholder data at rest and in transit to align with PCI DSS requirements.
  3. **Establish Backup & DRP Protocols:** Implement routine data backups and draft a formal Disaster Recovery Plan.
  4. **Enforce Central Password Management & MFA:** Standardize complexity rules and require MFA across all accounts.
  5. **Deploy IDS & SIEM Monitoring:** Install an Intrusion Detection System and centralized log aggregation (e.g., Splunk, Microsoft Sentinel) for continuous monitoring.
  6. **Formalize Legacy & Asset Workflows:** Establish regular patching schedules, middleware integrations, and complete a full asset classification inventory under NIST CSF.

**Next Steps:** 
Initiate immediate remediation on high risk access control and encryption gaps, followed by deploying SIEM logging and routine security audit schedules.

<p align="center">
  <a href="assets/documents/Final%20-%20Lab%202%20Conducting%20a%20Security%20Audit%20-%20Kraus.pdf">
    <img src="assets/images/Lab%202%20-%20Thumbnail.png" alt="Lab 2 - Conducting a Security Audit Preview" width="300"/>
  </a>
</p>

<p align="center">
  <sub>📄 <em><a href="assets/documents/Final - Lab 2 Conducting a Security Audit - Kraus.pdf">Full Audit Report (PDF)</a></em> 📄</sub><br />
  <sub><em>(Ctrl + click or scroll-click to open link in a new tab)</em></sub>
</p>

---

### 3. Security Incident Evaluation using NIST Cybersecurity Framework (CSF)

* **Project Title:** Using the NIST Cybersecurity Framework (CSF) to respond to a security incident
* **Project Introduction:** This project analyzes a two-hour Denial of Service (DoS) attack on the internal network of a multimedia company. An external threat actor sent an incoming flood of ICMP ping packets through an unconfigured firewall, causing network services to stop responding until incoming ICMP traffic was blocked, non-critical services were taken offline, and critical services were restored. Using the NIST Cybersecurity Framework (Identify, Protect, Detect, Respond, and Recover), the incident report documents the root cause, immediate mitigations, and ongoing security improvements.
* **Modeling and Evaluation:** Focused on ICMP ping packet traffic flooding the internal network and overwhelming network services, alongside TCP/IP and UDP networking concepts. Addressed taking non-critical network services offline while restoring critical network services during the outage, and separating critical services from non-critical workloads as a protection and recovery improvement. Blocked incoming ICMP packets, adding firewall ICMP rate limiting and source IP address verification for spoofed IP addresses, filtering suspicious ICMP traffic with an IDS/IPS, and using network monitoring software, SIEM alerting, service health tracking, and user account/access monitoring.
* **Conclusion:** Securing the network against future ICMP flood DoS attacks involves maintaining properly configured firewall rules with ICMP rate limiting and source IP verification, keeping critical services prioritized and configurations/backups ready for recovery, and updating security procedures and staff awareness. Next steps for intrusion detection include using network monitoring software, IDS/IPS filtering, and SIEM alerting to spot abnormal traffic and unauthorized account activity early, while refining response and recovery plans for future incidents

<p align="center">
  <a href="assets/documents/Lab3_NIST_CSF_Incident_Report_Analysis.pdf">
    <img src="assets/images/Incident%20Report%20Analysis%20using%20NIST%20CSF.png" alt="Incident Report Analysis using NIST CSF Preview" width="300"/>
  </a>
</p>

<p align="center">
  <sub>📄 <em><a href="assets/documents/Lab3_NIST_CSF_Incident_Report_Analysis.pdf">Full Incident Report Analysis (PDF)</a></em> 📄</sub><br />
  <sub><em>(Ctrl + click or scroll-click to open link in a new tab)</em></sub>
</p>

---

### 4. Using Linux Commands to Manage File Permissions

* **Project Title:** Linux File System Authorization & Permission Management
* **Project Introduction:** Two to three sentences stating the access control issue solved, the file/directory structure modified, and the security outcome achieved.
* **Methodology & Execution:** Name and describe the command-line utilities used (`chmod`, `chown`, `ls -la`) and permission evaluation criteria (read, write, execute for user/group/other).
* **Conclusion:** Best practices for Principle of Least Privilege (PoLP) and planned automated access control scripts.

<p align="center">
  <img src="assets/images/linux_permissions_terminal.png" alt="Linux Permissions Verification" width="700"/>
</p>

---

### 5. Applying Filters to SQL Queries

* **Project Title:** Security Log Analysis via SQL Filtering
* **Project Introduction:** Two to three sentences stating the database investigative problem, the log dataset queried, and the filter results isolating suspicious activity.
* **Methodology & Querying:** Describe the relational database structure, SQL operators (`WHERE`, `AND`, `OR`, `LIKE`), and metrics used to filter unauthorized login attempts or system events.
* **Conclusion:** Recommendations for automated threat query templates and future database auditing enhancements.

<p align="center">
  <img src="assets/images/sql_queries_output.png" alt="SQL Query Results" width="700"/>
</p>

---

### 6. Identifying Vulnerabilities for a Small Business

* **Project Title:** Small Business Threat Profile & Vulnerability Assessment
* **Project Introduction:** Two to three sentences stating the operational context, business assets/data at risk, and vulnerability assessment findings.
* **Modeling and Evaluation:** Name and describe threat modeling techniques (e.g., STRIDE), vulnerability scoring, and asset criticality evaluations used.
* **Conclusion:** Prioritized security recommendations tailored to small business resources and long-term risk management steps.

<p align="center">
  <img src="assets/images/vulnerability_assessment.png" alt="Vulnerability Assessment Table" width="700"/>
</p>

---

### 7. Documenting Incidents with an Incident Handler’s Journal

* **Project Title:** Incident Response Handler's Log & Event Timeline
* **Project Introduction:** Two to three sentences stating the security incident scenario analyzed, event log data processed, and response tracking results.
* **Methodology & Incident Lifecycle:** Describe the incident response phases applied (NIST SP 800-61), log categorization methods, and severity metrics.
* **Conclusion:** Root cause analysis findings, post-incident recommendations, and future playbook updates.

<p align="center">
  <img src="assets/images/incident_journal_entry.png" alt="Incident Handler Journal Entry" width="700"/>
</p>

---

### 8. Importing and Parsing a Text File in Python

* **Project Title:** Automated Security Log Parsing Algorithm in Python
* **Project Introduction:** Two to three sentences stating the manual file auditing bottleneck solved, the log/allow-list data parsed, and the automation output.
* **Methodology & Code Logic:** Name and describe the Python methods/functions used (`open()`, `.read()`, `.split()`), conditional logic, and string parsing evaluation metrics.
* **Conclusion:** Time saved through automation and planned features for real-time alert integration.

<p align="center">
  <img src="assets/images/python_parser_output.png" alt="Python Script Execution" width="700"/>
</p>
