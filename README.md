# 🛡️ Web Application Security Assessment & SIEM Monitoring

**Author:** Mani Kandan
**Domain:** Cyber Security
**Organization:** Aenexz Tech

![Status](https://img.shields.io/badge/status-completed-brightgreen)
![Domain](https://img.shields.io/badge/domain-Cyber%20Security-blue)
![SIEM](https://img.shields.io/badge/SIEM-Wazuh-orange)

---

## 📝 Project Overview

This project simulates a **full-cycle penetration test** followed by a **Blue Team incident investigation** for a fictional client, *SecureCorp*. The engagement involved actively exploiting a vulnerable web application (DVWA) and a Linux host, then investigating those exact attacks using the **Wazuh SIEM** platform to formulate actionable security recommendations — covering the complete offense-to-defense lifecycle.

---

## 🏗️ Architecture & Topology

| Component | Details |
|---|---|
| **Target Environment** | Ubuntu Linux VM hosting Apache2, PHP, and MariaDB |
| **Vulnerable Application** | Damn Vulnerable Web Application (DVWA) |
| **Attacker Machine** | Kali Linux / WSL2 |
| **SIEM / SOC** | Wazuh Open Source Security Platform |

<!-- Optional: upload your image `8.png` to the repo and reference it below to show the DVWA network/application mapping -->
<!-- ![DVWA Application Mapping](./8.png) -->

---

## ⚔️ Phase 1 — Red Team Operations (Attack Simulation)

Simulated real-world threat vectors against the target infrastructure, documenting payloads, methods, and execution timelines.

- **Vulnerability Probing** — Executed SQL Injection (SQLi) for database exfiltration, Reflected & Stored XSS for client-side execution, and Command Injection for OS-level access.
- **Credential Harvesting** — Automated dictionary brute-force attacks against the SSH daemon and HTTP-GET web login forms using `Hydra`.

---

## 🛡️ Phase 2 — Blue Team Operations (Detection & Investigation)

Transitioned to a SOC Analyst role to verify telemetry and investigate the attacks within the Wazuh SIEM.

- **Log Analysis** — Audited `/var/log/auth.log` and `/var/log/apache2/access.log`.
- **SIEM Triage** — Differentiated between auto-alerted events (e.g., SSH brute force triggering Wazuh Rule 5720) and web-layer attacks (SQLi, XSS) that required manual threat hunting and log correlation.
- **Incident Reporting** — Drafted a comprehensive incident timeline and evidence-based report.

---

## 🚀 Phase 3 — Remediation & Consulting

Translated technical findings into a strategic remediation roadmap for client leadership.

- Recommended enforcement of **cryptographic keys over SSH passwords** and **MFA** for web portals.
- Advised implementation of **Parameterized Data Objects (PDOs)** for SQLi mitigation and strict input validation.
- Proposed **SIEM rule tuning** and **Web Application Firewall (WAF)** deployment to catch application-layer attacks.

---

## 📁 Repository Contents

```
├── 1_Reports_and_Presentations/   # Final debrief presentation and recommendation tables
├── 2_Red_Team_Attack_Logs/        # Payload documentation and terminal outputs
├── 3_Blue_Team_Evidence/          # Wazuh dashboard screenshots and queried logs
└── 4_Evidence_Screenshots/        # Full uncropped visual evidence of exploits and alerts
```

---

## 🎯 Key Takeaways

- Demonstrated the complete attacker-to-defender lifecycle, from exploitation to detection to remediation.
- Bridged Red Team execution with Blue Team log correlation and SIEM rule interpretation.
- Delivered client-ready, prioritized security recommendations grounded in real attack evidence.

---

## 📬 Contact

For questions about this assessment or collaboration opportunities, feel free to reach out via GitHub.
