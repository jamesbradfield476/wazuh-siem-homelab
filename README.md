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

```mermaid
graph TD
    subgraph "Host Machine (Windows)"
        VB[VirtualBox]
    end

    subgraph "Wazuh SIEM"
        Manager[Wazuh Manager <br> (Ubuntu 24.04)] 
        Manager --- Dashboard[Dashboard + OpenSearch]
    end

    subgraph "Endpoints"
        LinuxAgent[Linux Agent <br> (Ubuntu 24.04)]
    end

    Manager <--> LinuxAgent
