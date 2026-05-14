# Personal SOC Home Lab - Wazuh SIEM

A practical **Security Operations Center (SOC)** home lab built with **Wazuh** to simulate real-world threat detection, monitoring, and incident response.

## 🎯 Project Objective
To deploy a functional SIEM environment, simulate common cyberattacks, detect and analyze alerts, and gain hands-on experience in blue team operations.

## 🛠️ Technologies Used
- **Wazuh 4.14** (All-in-One deployment)
- Ubuntu 24.04 LTS (Manager + Linux Agent)
- VirtualBox
- Hydra (brute force simulation tool)

## 🏗️ Lab Architecture

Host Machine (Windows PC)
└── VirtualBox
├── Wazuh Manager (Ubuntu 24.04)
│     ├── Wazuh Server
│     ├── Dashboard (Web UI)
│     └── Indexer (OpenSearch)
│
└── Linux Agent (Ubuntu 24.04)
└── Sends logs, FIM data & security events to Manager


## 🔧 Key Features Configured
- Centralized log collection
- File Integrity Monitoring (FIM)
- Real-time alerting and dashboard visualization
- MITRE ATT&CK technique mapping

## 🚀 Attack Simulations Performed

**1. Brute Force Attack**
- Simulated SSH brute force attacks using Hydra
- Wazuh successfully detected repeated authentication failures
- **MITRE ATT&CK**: T1110 (Brute Force) → Credential Access

**2. File Integrity Monitoring (FIM)**
- Simulated unauthorized file creation, modification of `/etc/passwd`, and deletion
- Triggered clear File Integrity alerts in Wazuh

## 📸 Screenshots

- Wazuh Dashboard Overview
- Active Linux Agent
- Brute Force / SSH Alerts (with MITRE ATT&CK tags)
- File Integrity Monitoring Alerts

*https://github.com/jamesbradfield476/wazuh-siem-homelab/blob/main/Wazuh_Documentation.pdf*

## 📚 Key Learnings
- Deployed and managed a full Wazuh SIEM stack in a virtual environment
- Configured agent registration and troubleshooting (dynamic IP issues, service management)
- Gained practical experience with File Integrity Monitoring and alert triage
- Learned how to simulate and detect brute force attacks
- Understood **MITRE ATT&CK** framework mapping in real alerts
- Improved documentation and project presentation skills

## 🔮 Future Enhancements
- Add Windows Agent
- Implement Active Response (automatic blocking)
- Create custom detection rules
- Set static IPs for all VMs

---

### Goals & Objectives

- Built a functional **Wazuh SIEM** home lab using VirtualBox, deploying a central Manager on Ubuntu 24.04 and Linux Agent for endpoint monitoring
- Simulated real-world threats including SSH brute-force attacks (Hydra) and unauthorized file modifications; successfully detected and analyzed alerts with MITRE ATT&CK mapping (T1110)
- Configured File Integrity Monitoring (FIM) and gained hands-on experience in security event detection and triage
- Demonstrated troubleshooting skills by resolving agent disconnections and network communication issues in a SIEM environment
- Developed practical SOC analyst skills through alert investigation, log analysis, and blue team operations

---

