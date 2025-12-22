Week Seven (Security Audit)

* Conduct a security audit and evaluate overall system configuration

In order to understand how well the system is doing I will need to install Lynis. In doing this I can get a score of how well the system is. Then through that I can correct and improve anythinig that falls below that.

<img width="1271" height="898" alt="Screenshot 2025-12-22 130422" src="https://github.com/user-attachments/assets/fdeb134b-8de8-4d51-a12b-18ef216378e5" />

<img width="1272" height="903" alt="Screenshot 2025-12-22 130641" src="https://github.com/user-attachments/assets/996d7eb5-0f32-48b9-8b75-07d87495525a" />

Above we can see that I install Lynis and I then run it to get a score of the system. As you can see below is the Hardeniing Index and a Warning.

<img width="1272" height="903" alt="Screenshot 2025-12-22 130641" src="https://github.com/user-attachments/assets/084f765d-4855-429d-8024-fe2b97341c63" />

<img width="1274" height="902" alt="Screenshot 2025-12-22 131329" src="https://github.com/user-attachments/assets/528996a2-66f4-4eec-bf87-d24209b8966c" />

I carry out updates and updrages as this should help improve the system

<img width="1269" height="898" alt="Screenshot 2025-12-22 131922" src="https://github.com/user-attachments/assets/85238c89-a216-410e-b38e-633c0ee61c22" />

<img width="1268" height="900" alt="Screenshot 2025-12-22 131955" src="https://github.com/user-attachments/assets/b29b0d16-9e8f-4bbf-a94d-87e36b387f8c" />

By carring out the changes I can help improve the system. As we can see the hardening had improve to 65

<img width="1276" height="898" alt="Screenshot 2025-12-22 133428" src="https://github.com/user-attachments/assets/2027c1b5-b821-4832-9b8c-f8f1e36486fe" />

As we move to nmap, we first try to connect to it by namap but this fails and says the host is down due to the filtering by the firewall. However when we -Pn option we can confirm that the server was reachable and that only authorised services were exposed. This ensure the firewall configuration is working.

<img width="1278" height="895" alt="Screenshot 2025-12-22 133904" src="https://github.com/user-attachments/assets/1256169d-ffeb-4be1-8afc-dda777cf0d56" />

We also confirm access control has only been given correctly: getent group sudo

<img width="1276" height="898" alt="Screenshot 2025-12-22 134422" src="https://github.com/user-attachments/assets/29696823-c51c-40f2-a71f-f8b4150d8f8b" />

We can also confirm the nessarcy services are running on the: ssh, ufw, fail2ban, unattended-upgrades and systemd-journald. The services running are all needed for remote administration, logging, firewall, intrusion prevention and auto updates. They are reuired for secure serve access, system loggin, network security, protecting SSH and for path management.

<img width="1276" height="899" alt="Screenshot 2025-12-22 134746" src="https://github.com/user-attachments/assets/452b20ce-3461-4b53-8010-b61784483688" />

[Week Three](Week_6.md) | [Home](index.md)
