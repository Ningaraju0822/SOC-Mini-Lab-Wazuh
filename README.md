# Mini SOC Lab

## Overview
This Mini SOC Lab demonstrates a simple Security Operations Center environment using open-source tools. The lab includes:

- **Attacker:** Kali Linux VM  
- **Victim:** Ubuntu Linux VM  
- **SIEM & Monitoring:** Wazuh (Manager + ELK Stack) on Ubuntu  

The setup enables practicing attack simulation, detection, and incident response.

## Lab Architecture

Kali Linux (Attacker) --> Ubuntu Linux (Victim with Wazuh Manager & Agent)
|
--> Wazuh Manager + ELK Stack for centralized logging & alerting


## Components
| Component     | Description                         |
|---------------|-----------------------------------|
| Kali Linux    | Attacker machine for pentesting   |
| Ubuntu Linux  | Victim machine with Wazuh Agent   |
| Wazuh Manager | Centralized detection & monitoring|
| ELK Stack     | Log storage, processing, and UI   |

## Setup Instructions

### 1. Environment Preparation
- Install VirtualBox on your host system  
- Create Kali Linux and Ubuntu VMs with 2GB+ RAM and 20GB disk each  
- Install respective OS using official ISOs

### 2. Install and Configure Wazuh
- On Ubuntu VM, install Wazuh Manager and ELK Stack  
- Install Wazuh Agent on Ubuntu and configure it to communicate with Wazuh Manager  
- Install Wazuh Agent on Kali Linux and configure similarly

### 3. Testing and Monitoring
- Verify agents are connected to Wazuh Manager  
- From Kali Linux, run pentesting tools (nmap, hydra, etc.) targeting Ubuntu  
- Monitor alerts and logs in Kibana dashboards  
- Practice alert triage and incident response

## Benefits
- Hands-on SOC monitoring experience  
- Understand attack detection and alert management  
- Prepare for real-world cybersecurity operations

## References
- [Wazuh Documentation](https://documentation.wazuh.com/)  
- [Kali Linux](https://www.kali.org/)  
- [Ubuntu](https://ubuntu.com/)  
- [VirtualBox](https://www.virtualbox.org/)

---

Feel free to customize and expand this README for your GitHub repo! Need help generating the PDF too?
