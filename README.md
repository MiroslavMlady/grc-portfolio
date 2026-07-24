# GRC Portfolio — Miroslav Mladý

Hands-on governance, risk and compliance projects built around a fictional Slovak SME (SLOVPACK s.r.o., a packaging manufacturer with 45 employees). The three projects are deliberately connected: the ISMS identifies the risks, the incident response plan operationalises them, and the DFIR case study shows the technical investigation behind them.

**Certifications:** HTB CDSA · PMP · GRC Mastery · ISO/IEC 27001:2022 · Google Cybersecurity

---

## 1. ISO/IEC 27001:2022 Implementation Lab
📁 `iso27001-implementation-lab/`

A complete ISMS built the way a real engagement works: a simulated client evidence pack (6 interviews, contract extracts, an incident record and a site walkthrough) feeds every ISMS artefact.

- Context analysis and ISMS scope (Clause 4)
- Information security policy and RACI roles (Clause 5)
- Risk methodology, 18-asset register, 20-risk register and treatment plan (Clause 6)
- Statement of Applicability — all 93 Annex A controls (Clause 6)
- 6 security policies (Clause 8)
- Internal audit with 2 nonconformities (Clause 9)
- Management review and closed corrective-action loop — full PDCA cycle (Clauses 9–10)
- Customer security questionnaire response (proof of value)

*The ISMS Manager role in this lab represents my perspective as the implementing consultant.*

## 2. Cyber Incident Response Plan
📁 `incident-response-plan/`

An operational plan built on the ISMS above. Where the Incident Management Policy (SLP-POL-005) defines *what* must happen, the CIRP defines *how* — scaled to a 45-employee manufacturer with a single IT administrator and an outsourced MSP.

- Virtual Incident Response Team with named roles, deputies and pre-approved containment actions
- Three-level severity classification and the full NIST SP 800-61 lifecycle
- Notification matrix: contractual 24-hour customer obligation, GDPR 72-hour notification, voluntary national CSIRT reporting
- Three playbooks mapped to the risk register: phishing/account compromise (RSK-001), ransomware (RSK-002), MSP privileged access compromise (RSK-009)
- Honest handling of the known logging gap (RSK-016) — the plan states what evidence will *not* be available, instead of pretending otherwise

## 3. DFIR — Phishing / Malware Analysis
📁 `dfir-investigation-report/`

Investigation of a simulated phishing email delivering the Agent Tesla information-stealing Trojan: email forensics, SPF/spoofing detection, malware triage (VirusTotal, Tria.ge), MITRE ATT&CK mapping and IOCs.

This closes the loop with the two projects above. Email is the entry point behind two of SLOVPACK's highest risks — RSK-001 (phishing to account compromise, driven by a documented incident in the evidence pack) and RSK-002 (ransomware, which most often arrives the same way). The ISMS defines the controls (A.6.3 awareness, A.8.7 anti-malware, A.5.17 MFA), the CIRP defines the response (Playbook A for account compromise, Playbook B for a malware payload), and this case study is the technical layer underneath both: what an analyst actually does when the email lands and the attachment turns out to be an infostealer.

---

⚠️ SLOVPACK s.r.o. is a fictional company. All persons, data and events are invented for portfolio purposes.




