# NIST 800-171 Controls Matrix — CUI Protection Requirements

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC_BY--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)
[![NIST SP 800-171](https://img.shields.io/badge/NIST-SP_800--171_Rev_2-blue.svg)]()
[![Controls](https://img.shields.io/badge/Controls-110-green.svg)]()

A detailed **NIST SP 800-171 controls matrix** mapping all 110 security requirements for protecting Controlled Unclassified Information (CUI) in nonfederal systems. This matrix includes cross-references to NIST SP 800-53, CMMC 2.0, ISO 27001, and CIS Controls, along with implementation guidance and assessment criteria.

> **Maintained by [Petronella Technology Group](https://petronellatech.com)** — A cybersecurity and compliance firm based in Raleigh, NC with 23+ years of experience helping organizations implement NIST frameworks. For professional NIST compliance services, visit our [NIST Compliance page](https://petronellatech.com/compliance/nist-compliance/).

---

## Table of Contents

- [What is NIST SP 800-171?](#what-is-nist-sp-800-171)
- [Who Must Comply with NIST 800-171?](#who-must-comply-with-nist-800-171)
- [NIST 800-171 Control Families](#nist-800-171-control-families)
- [Controls Matrix Overview](#controls-matrix-overview)
- [Control Family Details](#control-family-details)
  - [3.1 Access Control (22 requirements)](#31-access-control-22-requirements)
  - [3.2 Awareness and Training (3 requirements)](#32-awareness-and-training-3-requirements)
  - [3.3 Audit and Accountability (9 requirements)](#33-audit-and-accountability-9-requirements)
  - [3.4 Configuration Management (9 requirements)](#34-configuration-management-9-requirements)
  - [3.5 Identification and Authentication (11 requirements)](#35-identification-and-authentication-11-requirements)
  - [3.6 Incident Response (3 requirements)](#36-incident-response-3-requirements)
  - [3.7 Maintenance (6 requirements)](#37-maintenance-6-requirements)
  - [3.8 Media Protection (9 requirements)](#38-media-protection-9-requirements)
  - [3.9 Personnel Security (2 requirements)](#39-personnel-security-2-requirements)
  - [3.10 Physical Protection (6 requirements)](#310-physical-protection-6-requirements)
  - [3.11 Risk Assessment (3 requirements)](#311-risk-assessment-3-requirements)
  - [3.12 Security Assessment (4 requirements)](#312-security-assessment-4-requirements)
  - [3.13 System and Communications Protection (16 requirements)](#313-system-and-communications-protection-16-requirements)
  - [3.14 System and Information Integrity (7 requirements)](#314-system-and-information-integrity-7-requirements)
- [Cross-Reference Mappings](#cross-reference-mappings)
- [SPRS Scoring Guide](#sprs-scoring-guide)
- [Downloadable Matrix](#downloadable-matrix)
- [Additional Resources](#additional-resources)
- [About](#about)

---

## What is NIST SP 800-171?

**NIST Special Publication 800-171** ("Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations") defines 110 security requirements organized into 14 control families. These requirements are derived from the moderate-impact baseline of NIST SP 800-53 and are specifically tailored for nonfederal organizations that process, store, or transmit CUI.

NIST SP 800-171 is the foundation for:
- **CMMC Level 2** certification for defense contractors
- **DFARS 252.204-7012** compliance requirements
- **Federal contractor** cybersecurity obligations
- **Executive Order 14028** supply chain security initiatives

### NIST 800-171 vs. NIST 800-53

| Aspect | NIST SP 800-171 | NIST SP 800-53 |
|--------|----------------|----------------|
| **Audience** | Nonfederal organizations | Federal agencies |
| **Scope** | CUI protection | All federal information systems |
| **Controls** | 110 requirements | 1,000+ controls |
| **Baselines** | Single set | Low, Moderate, High |
| **Assessment** | NIST SP 800-171A | NIST SP 800-53A |

## Who Must Comply with NIST 800-171?

- **Defense contractors** with DFARS 252.204-7012 clause
- **Federal contractors** handling CUI under FAR 52.204-21 (Level 1) or DFARS (Level 2)
- **Universities and research institutions** with DoD or federal research funding involving CUI
- **Subcontractors** at any tier who receive CUI flow-down
- **State and local government** agencies handling federal CUI
- **IT service providers** (MSPs, MSSPs, cloud providers) supporting covered organizations

## NIST 800-171 Control Families

| Family | ID | Requirements | Description |
|--------|----|-------------|-------------|
| Access Control | AC | 22 | Manage who can access what, and how |
| Awareness and Training | AT | 3 | Security education for workforce |
| Audit and Accountability | AU | 9 | Logging, monitoring, and accountability |
| Configuration Management | CM | 9 | System baseline and change control |
| Identification and Authentication | IA | 11 | Identity verification and MFA |
| Incident Response | IR | 3 | Preparation, detection, and response |
| Maintenance | MA | 6 | System maintenance controls |
| Media Protection | MP | 9 | Digital and physical media safeguards |
| Personnel Security | PS | 2 | Screening and personnel actions |
| Physical Protection | PE | 6 | Physical access and environmental controls |
| Risk Assessment | RA | 3 | Risk identification and vulnerability management |
| Security Assessment | CA | 4 | Control effectiveness and security planning |
| System and Communications Protection | SC | 16 | Boundary protection and encryption |
| System and Information Integrity | SI | 7 | Malware protection and monitoring |
| **Total** | | **110** | |

## Controls Matrix Overview

The full controls matrix is available in CSV format: [`nist-800-171-controls-matrix.csv`](nist-800-171-controls-matrix.csv)

The matrix includes the following fields for each of the 110 requirements:

| Field | Description |
|-------|-------------|
| **Requirement ID** | NIST SP 800-171 requirement number (e.g., 3.1.1) |
| **Control Family** | One of the 14 control families |
| **Requirement Text** | Full requirement description |
| **NIST 800-53 Mapping** | Corresponding NIST SP 800-53 Rev. 5 control(s) |
| **CMMC 2.0 Practice** | Corresponding CMMC Level 2 practice ID |
| **CIS Controls v8** | Corresponding CIS Controls safeguard(s) |
| **SPRS Weight** | Point value for SPRS scoring (1, 3, or 5) |
| **Implementation Guidance** | Practical guidance for implementing the control |
| **Assessment Criteria** | How an assessor evaluates this control |
| **Common Evidence** | Typical evidence artifacts |

---

## Control Family Details

### 3.1 Access Control (22 requirements)

Access Control is the largest control family, accounting for 20% of all NIST 800-171 requirements. These controls govern who can access systems and data, and under what conditions.

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.1.1 | Limit system access to authorized users | AC-2, AC-3, AC-17 | 5 | Active Directory/IAM with documented access policies |
| 3.1.2 | Limit access to authorized transactions and functions | AC-3 | 5 | Role-based access control (RBAC) |
| 3.1.3 | Control CUI flow per approved authorizations | AC-4 | 5 | Data flow diagrams, DLP, network segmentation |
| 3.1.4 | Separate duties to reduce risk | AC-5 | 1 | Segregation of duties matrix |
| 3.1.5 | Employ least privilege | AC-6 | 5 | Minimize admin accounts, JIT access |
| 3.1.6 | Use non-privileged accounts for non-security functions | AC-6(2) | 1 | Separate admin and user accounts |
| 3.1.7 | Prevent non-privileged users from executing privileged functions | AC-6(9), AC-6(10) | 1 | UAC, sudo logging, PAM solutions |
| 3.1.8 | Limit unsuccessful logon attempts | AC-7 | 3 | Account lockout policy (3-5 attempts) |
| 3.1.9 | Provide privacy and security notices | AC-8 | 1 | Login banners on all systems |
| 3.1.10 | Session lock with pattern-hiding | AC-11, AC-11(1) | 1 | Screen lock at 15 minutes |
| 3.1.11 | Terminate sessions after defined conditions | AC-12 | 1 | Session timeout policies |
| 3.1.12 | Monitor and control remote access | AC-17(1), AC-17(2) | 5 | VPN with logging, remote access policy |
| 3.1.13 | Encrypt remote access sessions | AC-17(2) | 5 | FIPS-validated VPN encryption |
| 3.1.14 | Route remote access via managed points | AC-17(3) | 3 | VPN concentrator, no direct RDP |
| 3.1.15 | Authorize remote privileged commands | AC-17(4) | 3 | Documented approval for remote admin |
| 3.1.16 | Authorize wireless access | AC-18 | 1 | Wireless access policy |
| 3.1.17 | Protect wireless access | AC-18(1) | 1 | WPA3/WPA2-Enterprise, 802.1X |
| 3.1.18 | Control mobile devices | AC-19 | 1 | MDM solution, mobile device policy |
| 3.1.19 | Encrypt CUI on mobile devices | AC-19(5) | 3 | Full device encryption (BitLocker, FileVault) |
| 3.1.20 | Control external system connections | AC-20, AC-20(1) | 1 | External system connection agreements |
| 3.1.21 | Limit portable storage on external systems | AC-20(2) | 1 | USB restriction policy |
| 3.1.22 | Control CUI on public systems | AC-22 | 1 | Website content review process |

### 3.2 Awareness and Training (3 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.2.1 | Security awareness for all users | AT-2 | 3 | Annual security awareness training |
| 3.2.2 | Role-based security training | AT-3 | 3 | Training tailored to job functions |
| 3.2.3 | Insider threat awareness | AT-2(2) | 3 | Insider threat training program |

### 3.3 Audit and Accountability (9 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.3.1 | Create and retain audit logs | AU-2, AU-3, AU-3(1), AU-6 | 5 | SIEM deployment, log retention policy |
| 3.3.2 | Trace user actions | AU-2, AU-3, AU-6 | 5 | Unique user IDs, no shared accounts |
| 3.3.3 | Review and update logged events | AU-2(3) | 3 | Annual review of audit log policy |
| 3.3.4 | Alert on audit failure | AU-5 | 3 | SIEM alerting on log collection failures |
| 3.3.5 | Correlate audit records | AU-6(1), AU-6(3) | 3 | SIEM correlation rules |
| 3.3.6 | Audit reduction and reporting | AU-7 | 3 | SIEM dashboards and reports |
| 3.3.7 | Synchronize system clocks | AU-8 | 1 | NTP configuration |
| 3.3.8 | Protect audit information | AU-9 | 3 | Restricted access to log storage |
| 3.3.9 | Limit audit management | AU-9(4) | 1 | Only admins manage log settings |

### 3.4 Configuration Management (9 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.4.1 | Baseline configurations and inventories | CM-2, CM-6, CM-8, CM-8(1) | 5 | CMDB, CIS Benchmarks, DISA STIGs |
| 3.4.2 | Security configuration settings | CM-6 | 5 | GPO, hardening standards |
| 3.4.3 | Change control | CM-3 | 3 | Change management process |
| 3.4.4 | Security impact analysis | CM-4 | 3 | Pre-change security review |
| 3.4.5 | Access restrictions for changes | CM-5 | 3 | Separation of dev/test/prod |
| 3.4.6 | Least functionality | CM-7 | 3 | Disable unnecessary features |
| 3.4.7 | Restrict nonessential services | CM-7(1) | 3 | Port/protocol restrictions |
| 3.4.8 | Application whitelisting/blacklisting | CM-7(4), CM-7(5) | 5 | AppLocker, application control |
| 3.4.9 | Control user-installed software | CM-11 | 1 | Software installation policy |

### 3.5 Identification and Authentication (11 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.5.1 | Identify users and devices | IA-2, IA-5 | 3 | Unique IDs for all users/devices |
| 3.5.2 | Authenticate identities | IA-2, IA-5 | 5 | Strong authentication mechanisms |
| 3.5.3 | Multifactor authentication | IA-2(1), IA-2(2), IA-2(3) | 5 | MFA for all accounts |
| 3.5.4 | Replay-resistant authentication | IA-2(8), IA-2(9) | 1 | Token-based or cert-based auth |
| 3.5.5 | Prevent identifier reuse | IA-4 | 1 | Unique ID lifecycle management |
| 3.5.6 | Disable inactive identifiers | IA-4(4) | 1 | 90-day inactivity disable |
| 3.5.7 | Password complexity | IA-5(1) | 1 | 14+ character minimum |
| 3.5.8 | Prohibit password reuse | IA-5(1) | 1 | Remember 24 passwords |
| 3.5.9 | Temporary passwords | IA-5(1) | 1 | Force change on first login |
| 3.5.10 | Cryptographically protect passwords | IA-5(1) | 1 | Hashing and TLS |
| 3.5.11 | Obscure authentication feedback | IA-6 | 1 | Mask password input |

### 3.6 Incident Response (3 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.6.1 | Establish IR capability | IR-2, IR-4, IR-5, IR-6, IR-7 | 5 | Written IR plan, IR team |
| 3.6.2 | Track and report incidents | IR-6 | 3 | Incident tracking system, DIBNet |
| 3.6.3 | Test IR capability | IR-3, IR-3(2) | 3 | Annual tabletop exercises |

### 3.7 Maintenance (6 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.7.1 | Perform system maintenance | MA-2 | 1 | Maintenance schedule and records |
| 3.7.2 | Control maintenance tools and personnel | MA-3, MA-3(1), MA-3(2) | 3 | Approved tools list |
| 3.7.3 | Sanitize equipment for off-site maintenance | MA-2 | 1 | Data sanitization procedures |
| 3.7.4 | Check media for malicious code | MA-3(2) | 1 | Scan before use |
| 3.7.5 | MFA for nonlocal maintenance | MA-4 | 5 | VPN + MFA for remote maintenance |
| 3.7.6 | Supervise unauthorized maintenance personnel | MA-5 | 1 | Escort procedures |

### 3.8 Media Protection (9 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.8.1 | Protect system media | MP-2, MP-4 | 1 | Locked storage, access logs |
| 3.8.2 | Limit media access | MP-2 | 1 | Need-to-know access |
| 3.8.3 | Sanitize media before disposal | MP-6 | 3 | NIST 800-88 sanitization |
| 3.8.4 | Mark media with CUI markings | MP-3 | 1 | CUI labeling procedures |
| 3.8.5 | Control media during transport | MP-5 | 3 | Chain of custody, encryption |
| 3.8.6 | Encrypt CUI on portable media | MP-5(4) | 3 | BitLocker To Go, LUKS |
| 3.8.7 | Control removable media | MP-7 | 1 | USB policy, GPO restrictions |
| 3.8.8 | Prohibit unowned portable storage | MP-7(1) | 1 | No personal USB devices |
| 3.8.9 | Protect backup confidentiality | CP-9 | 3 | Encrypted backups |

### 3.9 Personnel Security (2 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.9.1 | Screen individuals | PS-3 | 1 | Background checks |
| 3.9.2 | Protect systems during personnel actions | PS-4, PS-5 | 1 | Termination checklist |

### 3.10 Physical Protection (6 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.10.1 | Limit physical access | PE-2, PE-5 | 1 | Badge access, locked rooms |
| 3.10.2 | Monitor physical facility | PE-6 | 1 | Cameras, alarm systems |
| 3.10.3 | Escort visitors | PE-3 | 1 | Visitor sign-in, escort policy |
| 3.10.4 | Physical access audit logs | PE-3 | 1 | Badge system logs |
| 3.10.5 | Control physical access devices | PE-3 | 1 | Key/badge management |
| 3.10.6 | Safeguard CUI at alternate sites | PE-17 | 1 | Remote work security policy |

### 3.11 Risk Assessment (3 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.11.1 | Periodic risk assessment | RA-3 | 5 | Annual risk assessment |
| 3.11.2 | Vulnerability scanning | RA-5, RA-5(5) | 5 | Monthly scans, new vuln scans |
| 3.11.3 | Remediate vulnerabilities | RA-5 | 5 | Patch management program |

### 3.12 Security Assessment (4 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.12.1 | Periodic security assessment | CA-2 | 3 | Annual control assessment |
| 3.12.2 | POA&M development | CA-5 | 5 | Active POA&M tracking |
| 3.12.3 | Ongoing control monitoring | CA-7 | 3 | Continuous monitoring program |
| 3.12.4 | System Security Plan | PL-2 | 5 | Comprehensive SSP |

### 3.13 System and Communications Protection (16 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.13.1 | Boundary protection | SC-7 | 5 | Firewalls, IDS/IPS |
| 3.13.2 | Security architecture | SA-8 | 1 | Defense-in-depth design |
| 3.13.3 | Separate user and admin functions | SC-2 | 1 | Separate admin workstations |
| 3.13.4 | Prevent covert channels | SC-4 | 1 | Shared resource controls |
| 3.13.5 | DMZ for public systems | SC-7 | 5 | Network segmentation |
| 3.13.6 | Deny-all, permit-by-exception | SC-7(5) | 5 | Default-deny firewall rules |
| 3.13.7 | Prevent split tunneling | SC-7(7) | 5 | VPN full tunnel policy |
| 3.13.8 | Encrypt CUI in transit | SC-8, SC-8(1) | 5 | TLS 1.2+, FIPS-validated |
| 3.13.9 | Terminate idle sessions | SC-10 | 1 | Network session timeouts |
| 3.13.10 | Cryptographic key management | SC-12 | 3 | Key management procedures |
| 3.13.11 | FIPS-validated cryptography | SC-13 | 5 | FIPS 140-2/3 validated modules |
| 3.13.12 | Control collaborative devices | SC-15 | 1 | Camera/mic indicators |
| 3.13.13 | Control mobile code | SC-18 | 1 | Script/macro restrictions |
| 3.13.14 | Control VoIP | SC-19 | 1 | VoIP security policy |
| 3.13.15 | Session authenticity | SC-23 | 1 | TLS for all web sessions |
| 3.13.16 | Encrypt CUI at rest | SC-28 | 5 | Full disk encryption |

### 3.14 System and Information Integrity (7 requirements)

| Req ID | Requirement | 800-53 Mapping | SPRS Weight | Key Implementation |
|--------|------------|----------------|-------------|-------------------|
| 3.14.1 | Timely flaw remediation | SI-2 | 5 | Patch management (14/30/90 day SLAs) |
| 3.14.2 | Malicious code protection | SI-3 | 5 | EDR/antimalware on all endpoints |
| 3.14.3 | Monitor security alerts | SI-5 | 1 | CISA, vendor advisories |
| 3.14.4 | Update malware protection | SI-3 | 1 | Auto-update signatures |
| 3.14.5 | Periodic and real-time scans | SI-3 | 3 | Scheduled + on-access scanning |
| 3.14.6 | Monitor inbound/outbound traffic | SI-4 | 5 | IDS/IPS, NDR solutions |
| 3.14.7 | Identify unauthorized use | SI-4 | 3 | SIEM use-case detection |

---

## Cross-Reference Mappings

This matrix provides cross-references to help organizations that are complying with multiple frameworks:

| NIST 800-171 Family | NIST 800-53 Rev. 5 | CMMC 2.0 | ISO 27001:2022 | CIS Controls v8 |
|---------------------|-------------------|----------|----------------|-----------------|
| Access Control | AC family | AC domain | A.5, A.8, A.9 | CIS 3, 4, 5, 6 |
| Awareness & Training | AT family | AT domain | A.6, A.7 | CIS 14 |
| Audit & Accountability | AU family | AU domain | A.8, A.12 | CIS 8 |
| Configuration Mgmt | CM family | CM domain | A.8, A.12 | CIS 4 |
| ID & Authentication | IA family | IA domain | A.5, A.9 | CIS 5, 6 |
| Incident Response | IR family | IR domain | A.5 | CIS 17 |
| Maintenance | MA family | MA domain | A.7, A.11 | CIS 4 |
| Media Protection | MP family | MP domain | A.7, A.8 | CIS 3 |
| Personnel Security | PS family | PS domain | A.6 | CIS 14 |
| Physical Protection | PE family | PE domain | A.7, A.11 | CIS 1 |
| Risk Assessment | RA family | RA domain | A.5, A.8 | CIS 7 |
| Security Assessment | CA family | CA domain | A.5, A.18 | CIS 18 |
| System & Comm Protection | SC family | SC domain | A.5, A.8, A.10 | CIS 3, 12, 13 |
| System & Info Integrity | SI family | SI domain | A.5, A.8 | CIS 7, 10 |

## SPRS Scoring Guide

The **Supplier Performance Risk System (SPRS)** score is calculated using the DoD Assessment Methodology:

- **Maximum score**: 110 points
- **Each requirement** has an assigned value of 1, 3, or 5 points
- **Unmet requirements** deduct their full point value from the maximum
- **POA&Ms** do not change the score — the score reflects current implementation state

### Score Distribution

| SPRS Weight | Count | Total Points | Percentage |
|-------------|-------|-------------|------------|
| 5 points | 25 | 125 (capped at contribution to 110) | High-impact controls |
| 3 points | 38 | 114 (capped) | Medium-impact controls |
| 1 point | 47 | 47 (capped) | Lower-impact controls |

**Note**: The specific scoring values and methodology are defined in the NIST SP 800-171 DoD Assessment Methodology. Consult the latest version for exact point values.

### What Score Do You Need?

- **110** — Full compliance, ideal for contract competitiveness
- **80-109** — Minor gaps, most with active POA&Ms
- **50-79** — Significant gaps requiring remediation
- **Below 50** — Major compliance concerns; may affect contract eligibility

## Downloadable Matrix

- [`nist-800-171-controls-matrix.csv`](nist-800-171-controls-matrix.csv) — Full controls matrix in CSV format

## Additional Resources

### Official Sources
- [NIST SP 800-171 Rev. 2](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) — The source publication
- [NIST SP 800-171A](https://csrc.nist.gov/publications/detail/sp/800-171a/final) — Assessment procedures
- [NIST SP 800-53 Rev. 5](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) — Parent control catalog
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework) — Complementary framework

### Related Open-Source Resources
- [CMMC Compliance Checklist](https://github.com/capetron/cmmc-compliance-checklist) — CMMC Level 2 self-assessment checklist
- [HIPAA Security Risk Assessment Template](https://github.com/capetron/hipaa-security-risk-assessment-template) — HIPAA SRA template
- [Incident Response Plan Template](https://github.com/capetron/incident-response-plan-template) — Free IR plan template

### Professional NIST Compliance Services

For organizations needing expert guidance on NIST compliance, [Petronella Technology Group](https://petronellatech.com/compliance/nist-compliance/) provides:

- **NIST 800-171 gap assessments** with detailed findings and remediation roadmap
- **System Security Plan (SSP)** development and review
- **SPRS score calculation** and improvement strategies
- **Managed security services** for ongoing compliance monitoring
- **CMMC preparation** built on NIST 800-171 foundation
- **Vulnerability management** and remediation support

> Visit [petronellatech.com/compliance/nist-compliance/](https://petronellatech.com/compliance/nist-compliance/) to learn more about our NIST compliance services.

---


---

## ⚠️ The Gap Between Checking Boxes and Passing an Assessment

This matrix maps requirements, but **implementation is where organizations struggle**. The most common issues we find during gap assessments:

- **Partial implementation scored as complete** — "We have antivirus" doesn't satisfy SI-3 if you can't demonstrate centralized management, signature updates, and response procedures
- **Inherited controls not validated** — Cloud provider shared responsibility models are frequently misunderstood
- **SPRS score inflation** — Overestimating your score puts your contracts at risk when DIBCAC validates
- **Missing POA&M milestones** — Accepted POA&Ms need specific remediation dates and resource allocation, not "TBD"

> **Your SPRS score is submitted to the DoD under penalty of the False Claims Act.** An inaccurate self-assessment isn't just a compliance gap — it's a legal liability.

---

## 📞 Get Your NIST 800-171 Score Right

**→ [Schedule a Free SPRS Score Review](https://petronellatech.com/contact-us/schedule-appointment/)** | Call [(919) 422-8500](tel:+19194228500)

[Petronella Technology Group](https://petronellatech.com/compliance/nist-compliance/) helps defense contractors accurately assess, score, and improve their NIST 800-171 implementation. We've helped organizations go from SPRS scores in the negatives to assessment-ready.


## About

This NIST 800-171 controls matrix is maintained by **[Petronella Technology Group](https://petronellatech.com)**, a cybersecurity and IT compliance firm headquartered in Raleigh, North Carolina. Founded in 2002, Petronella Technology Group has over 23 years of experience helping organizations implement NIST frameworks and protect Controlled Unclassified Information.

### Other Compliance Resources
- [CMMC Compliance Checklist](https://github.com/capetron/cmmc-compliance-checklist)
- [HIPAA Security Risk Assessment Template](https://github.com/capetron/hipaa-security-risk-assessment-template)
- [Incident Response Plan Template](https://github.com/capetron/incident-response-plan-template)
- [Cybersecurity Awareness Training Materials](https://github.com/capetron/cybersecurity-awareness-training-materials)

---

*This matrix is provided for informational purposes and should not be considered legal or compliance advice. Organizations should consult with qualified compliance professionals for their specific situation. Based on NIST SP 800-171 Rev. 2 as of 2026.*

*Licensed under [CC-BY-SA-4.0](LICENSE). Contributions welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).*
