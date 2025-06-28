# UFW_Firewall_Configuration_Kali

 Steps Performed
1. Open Firewall Configuration Tool
UFW was used as the firewall configuration tool via terminal in Kali Linux.

2. List Current Firewall Rules
Initially, the firewall was inactive. After enabling it, current rules were listed using:

bash
Copy
Edit
sudo ufw status numbered
3. Block Inbound Traffic on Port 23 (Telnet)
To block Telnet on port 23:

bash
Copy
Edit
sudo ufw deny in 23
4. Test the Rule
The rule was tested using Telnet to verify if the port was blocked:

bash
Copy
Edit
telnet localhost 23
5. Allow SSH (Port 22)
To ensure SSH access remains available:

bash
Copy
Edit
sudo ufw allow ssh
6. Remove Test Block Rule
To delete the rule and restore original settings:

bash
Copy
Edit
sudo ufw delete 2
🛠 Commands Used
bash
Copy
Edit
sudo apt update
sudo apt install ufw
sudo ufw status numbered
sudo ufw enable
sudo ufw deny in 23
telnet localhost 23
sudo ufw allow ssh
sudo ufw delete 2
🖥️ GUI Support
Although this task focused on CLI-based configuration, GUI tools can also be used for UFW such as gufw if needed.

✅ Outcome
The firewall was successfully configured:

Telnet access was blocked on port 23.

SSH access was preserved.

Firewall rules were managed and cleaned up post-testing.

