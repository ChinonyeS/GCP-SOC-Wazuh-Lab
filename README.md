# GCP-SOC-Wazuh-Lab
A cloud-based SOC lab, featuring Wazuh for threat detection and Fail2ban for automated incident response
# Cloud-Native SOC & IAM Monitoring Lab (GCP)

## Project Overview
This project demonstrates the deployment of a Security Operations Center (SOC) using **Wazuh** in Google Cloud Platform. The lab monitors for unauthorized access attempts and uses **Fail2ban** for automated threat mitigation.

### Technologies Used
* **Cloud:** Google Cloud Platform (Compute Engine, VPC Firewalls)
* **SIEM/XDR:** Wazuh (Manager & Agent)
* **Security Tools:** Fail2ban, SSHD
* **OS:** Ubuntu 22.04 LTS

### Key Features
1. **IAM Security:** Implemented a custom Service Account to ensure the VM followed the **Principle of Least Privilege**.
2. **Threat Detection:** Configured Wazuh to monitor real-time logs for brute force attacks.
3. **Automated Response:** Integrated Fail2ban to automatically block malicious IPs after 3 failed login attempts.

### Incident Simulation
* **Scenario:** An unauthorized user attempted to access the server via SSH using the username `hacker_test`.
* **Result:** Wazuh triggered a Level 12 alert. Fail2ban detected the repeated failures and added the attacker's IP to the ban list.

---
### Lab Evidence

#### 1. Wazuh Security Dashboard
![Wazuh Dashboard](Wazuh%20visuals.png)
![Wazuh Dashboard](Wazuh%20visuals%201.png)
*Figure 1: High-level overview of security events and agent status.*

#### 2. Brute Force Detection
![Brute Force Alert](Security%20monitoring%20logs%20with%20wazuh%20.png)
![Brute Force Alert](Reading%20security%20logs%201%20.png)
![Brute Force Alert](Reading%20security%20logs%202%20.png)
![Brute Force Alert](Reading%20security%20logs%203%20.png)
*Figures 2, 3, 4 and 5: Level 12 alert triggered by unauthorized 'hacker_test' login attempt.*

#### 3. Automated Mitigation (Fail2ban)
![Fail2ban Status](Fail2ban%20security%20log.png)
*Figure 6: Fail2ban service successfully identifying and banning the malicious IP.*

Added technical evidence screenshots
