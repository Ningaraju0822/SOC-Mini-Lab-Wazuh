# SOC Mini Lab – Wazuh, ELK Stack, Caldera & Atomic Red Team

## 📌 Project Overview
The **SOC Mini Lab** is a simulated Security Operations Center environment built to detect, analyze, and respond to cyberattacks in real time.  
This lab leverages **open-source tools** to replicate enterprise SOC operations, covering **SIEM**, **log analysis**, **endpoint monitoring**, and **attack simulations**.

It demonstrates **end-to-end SOC workflows** — from attack simulation to detection and incident investigation.

---

## 🎯 Objectives
- Build a functional SOC environment using open-source tools.
- Simulate real-world cyberattacks and collect logs.
- Create detection rules and visualize alerts in a SIEM.
- Demonstrate SOC incident response and threat hunting workflows.
- Document results for portfolio and interview purposes.

---

## 🏗 Architecture Diagram

[ Kali Linux (Attacker) ] → [ Windows 10 VM (Victim) ]
↓ ↓
[ Wazuh Agent ] [ Wazuh Agent ]
↓ ↓
[ Wazuh Server + ELK Stack ]
↓
[ SOC Analyst Dashboard ]


---

## 🛠 Tools & Technologies Used
| Tool | Purpose |
|------|---------|
| **VirtualBox** | Virtualization platform for creating isolated lab environments |
| **Kali Linux** | Attacker machine for penetration testing |
| **Windows 10 VM** | Victim machine for endpoint monitoring |
| **Wazuh** | SIEM & endpoint monitoring |
| **ELK Stack (Elasticsearch, Logstash, Kibana)** | Log storage, processing, and visualization |
| **Caldera** | Automated adversary emulation platform |
| **Atomic Red Team** | MITRE ATT&CK-based attack simulation |

---

## 🔧 Step-by-Step Implementation

### **1. Lab Setup**
- Installed **VirtualBox** and created three virtual machines:
  - Kali Linux (Attacker)
  - Windows 10 (Victim)
  - Ubuntu Server with Wazuh & ELK Stack
- Configured all machines in **Host-Only Adapter** mode for network isolation.

### **2. Wazuh & ELK Installation**
- Installed **Wazuh Manager** on Ubuntu server.
- Deployed **ELK Stack** for log management and dashboards.
- Installed and connected **Wazuh Agents** on Kali Linux and Windows 10 VMs.
- Verified agent connections in the Wazuh dashboard.

### **3. Attack Simulation**
- **Caldera**:
  - Ran phishing simulation and lateral movement scenarios.
- **Atomic Red Team**:
  - Executed MITRE ATT&CK TTPs (Credential Dumping, Brute Force, etc.).
- **Manual Attacks from Kali**:
  - SSH brute force with Hydra.
  - SMB enumeration & exploitation.

### **4. Detection & Analysis**
- Wazuh collected endpoint and network logs from agents.
- Created **custom detection rules** for brute force, privilege escalation, and malicious file execution.
- Visualized incidents and alerts in **Kibana dashboards**.

### **5. Incident Response**
- Investigated triggered alerts in Wazuh.
- Correlated multiple indicators to detect attack patterns.
- Documented incidents in a structured format.

---

## 📊 Detection Results
| Attack Type | Tool Used | Detection Method | Alert Status |
|-------------|-----------|------------------|--------------|
| SSH Brute Force | Hydra | Wazuh rule 5710 | ✅ Detected |
| Credential Dumping | Atomic Red Team | Sysmon + Wazuh | ✅ Detected |
| Phishing Simulation | Caldera | Email log analysis | ✅ Detected |

---

## 📸 Screenshots
*(Replace these placeholders with your own screenshots)*  
- **Wazuh Dashboard** – showing real-time alerts.  
- **Kibana Attack Timeline** – visual representation of incidents.  
- **Caldera Attack Graph** – mapping simulated attack steps.  
- **Atomic Red Team Logs** – execution and detection proof.

---

## 📚 Lessons Learned
- SIEM fine-tuning reduces false positives significantly.
- Attack simulation tools are essential for SOC readiness testing.
- Isolated lab environments prevent accidental real-world impact.

---

## 🚀 Future Improvements
- Integrate **Shuffle SOAR** for automated incident response.
- Add **Threat Intelligence Feeds** to Wazuh.
- Expand the lab with **cloud workload monitoring** capabilities.

---

## 📂 Repository Structure

SOC-Mini-Lab/
│── README.md # Project documentation
│── diagrams/ # Architecture diagrams
│── screenshots/ # Lab screenshots
│── configs/ # Wazuh & ELK configuration files
│── attack-scripts/ # Custom attack scripts


---

## 🏷 GitHub Topics
`soc` `cybersecurity` `siem` `wazuh` `elk-stack` `incident-response` `threat-hunting` `caldera` `atomic-red-team` `red-team` `blue-team` `security-lab`

---

## 📜 License
This project is licensed under the MIT License – feel free to use, modify, and share.


