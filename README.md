# 🛡️Automated-DoS-Mitigation-Log-Management-System
This project demonstrates how to defend a Linux server against Denial of Service (DoS) SYN Flood attacks using a layered defense strategy.By integrating UFW (Uncomplicated Firewall) as a sensor and Fail2Ban as an automated response engine, the system detects high-velocity attack patterns and dynamically updates kernel-level firewall rules to drop malicious traffic.

# 🛠️ Technology Stack
- Operating System: Ubuntu 22.04 LTS (Victim)
- Attack Tool: Kali Linux (hping3)
- Firewall: UFW (Uncomplicated Firewall)
- Automation: Fail2Ban
- Log Management: Logrotate

🚀 Implementation Steps
1. UFW Configuration
First, the firewall was configured to block unauthorized traffic and, crucially, to log these events.
```
sudo ufw enable
sudo ufw logging medium  # Ensures SRC IP data is captured for Fail2Ban
```
