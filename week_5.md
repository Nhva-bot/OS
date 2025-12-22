Week Five (Advanced Security and Monitoring)

* Implement Access Control using AppArmor with documentation.
* Configure automatic security updates with evidence of implementation
* Configure fail2ban for enhanced intrusion detection
* Create a security baseline verification script
* Create a remote monitoring script

In this week we look at implementing advanced security control and develop monitoring capabilities. As we are using Ubuntu we will focus on AppArmor as that is the default.

First we need to confirm AppArmor is running on the server and find out what services are protected and which profiles are enforcing or complaiiin mode with the following: 
sudo aa-status and sudo aa-status --verbose

<img width="1271" height="900" alt="Screenshot 2025-12-22 084652" src="https://github.com/user-attachments/assets/d96bcc10-daeb-4555-9148-eacf6f9f2d0f" />

<img width="1276" height="899" alt="Screenshot 2025-12-22 084729" src="https://github.com/user-attachments/assets/6f3b3c51-e179-4b64-8c2d-003a84155f7f" />

From this we can see AppArmor is installed. MAC is enabled and the kernel module is active.
We can also see 24 profiles are in enfore mode. AppArmor is actually enforcing security.

Next we configure automatic security updates. The evidence follows:

<img width="1271" height="899" alt="Screenshot 2025-12-22 085411" src="https://github.com/user-attachments/assets/e89af63d-1d3f-4df8-913b-b49939d696be" />

<img width="1271" height="902" alt="Screenshot 2025-12-22 085533" src="https://github.com/user-attachments/assets/bd551d73-8c08-42d7-a746-0e7fe4837904" />

<img width="1271" height="896" alt="Screenshot 2025-12-22 085637" src="https://github.com/user-attachments/assets/24785d8f-006e-4f45-8335-8cf2a3d7e33a" />

<img width="1276" height="897" alt="Screenshot 2025-12-22 085824" src="https://github.com/user-attachments/assets/51185381-7bc4-4981-b755-4dbb493b1a43" />

Security updates were configured using unattended-upgrades to ensure critical security patches are installed without manual intervention. Next we install fail2ban. This protects the server by monitoring log files, detect repeated failed login attempts. Blocking the attackers IP using firewalls 

<img width="1273" height="900" alt="Screenshot 2025-12-22 090738" src="https://github.com/user-attachments/assets/dde2cf60-4b45-498b-b71b-c0771b5b7256" />

<img width="1272" height="898" alt="Screenshot 2025-12-22 090846" src="https://github.com/user-attachments/assets/abe40042-cf10-4e0d-b7b9-b9934b9dffee" />

<img width="1272" height="903" alt="Screenshot 2025-12-22 090952" src="https://github.com/user-attachments/assets/972b7dac-1db4-45d9-b486-f5ab68140702" />

fail2ban is deployed to enhance intrusion detection by monitoring SSH authentication logs.

Next we create a script that runs on the serveer and is executed via SSH and it automatically verifies that all required security controls are still enabled. The script created and excuted on the server validates SSH hardening, firewall configuration, AppArmor enforcement, automatic security updates and fail2ban operation.

<img width="1275" height="897" alt="Screenshot 2025-12-22 092244" src="https://github.com/user-attachments/assets/1036f727-23e4-4a5a-91b9-ec50585b479e" />

The following shows the script created for remote server moitoring

<img width="1273" height="898" alt="Screenshot 2025-12-22 093637" src="https://github.com/user-attachments/assets/b2965b21-ebaa-4b28-bbd3-b20ee3e22f6a" />

<img width="1278" height="893" alt="Screenshot 2025-12-22 093029" src="https://github.com/user-attachments/assets/7ae5bee8-7d7b-4647-a13c-d55c14aed5d0" />

<img width="1272" height="901" alt="Screenshot 2025-12-22 094142" src="https://github.com/user-attachments/assets/06f289d1-f136-435b-ad3f-bf6a7aaffb86" />

<img width="1274" height="897" alt="Screenshot 2025-12-22 094040" src="https://github.com/user-attachments/assets/60545d66-2c3d-4809-9ee1-5cef5aef0f98" />



[Week Four](week_4.md) | [Home](index.md) | [Week Six](week_6.md)



