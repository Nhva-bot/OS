Week Four ( Initial System Configuration & Security Implementation)

The server was deployed and secured by implementing foundational security controls. All configuration tasks were performed remotely via SSH from the workstation.

* Configure SSH with key-based authentication
* Configure a firewall permitting SSH from one specific workstation only
* Manage users and implement privilege management, creating a non-root administrative user.

In the following screenshots I replace the password with cryptographic keys. This is is generated with ssh-kegen -t ed25519. What is generated will be a pirvate key which will be kept on the workstation and a public key which will be sent to the server, ssh-copy-id t@192.168.56.101.


<img width="1271" height="897" alt="Screenshot 2025-12-21 203022" src="https://github.com/user-attachments/assets/6b8ab077-75ea-4911-ba61-5e42bda1c382" />

<img width="1272" height="891" alt="Screenshot 2025-12-21 203326" src="https://github.com/user-attachments/assets/635c57a7-ca78-4025-9a8f-5415bce71a99" />

<img width="1279" height="896" alt="Screenshot 2025-12-21 203921" src="https://github.com/user-attachments/assets/a6ffc7ad-db5e-4952-a3e1-723579c320d1" />

Next we access the server without having to enter a password like before.

<img width="1280" height="902" alt="Screenshot 2025-12-21 204426" src="https://github.com/user-attachments/assets/a5e09751-b5cd-40c6-a25b-0da8d28eabc0" />

<img width="1279" height="895" alt="Screenshot 2025-12-21 204608" src="https://github.com/user-attachments/assets/7ef4cdd2-9127-4cd6-9905-074f3e9fe620" />

SSH is futher hardened by disabling direct root login and password-based authentication, enforcing key based access only. This helps use reduce surface attacks and ensure secure remote administration. By disabling password login, root login we ensure security. The following show the changes made to sshd_config

<img width="1275" height="898" alt="Screenshot 2025-12-21 205630" src="https://github.com/user-attachments/assets/2db94d61-a6a9-44e2-b952-fc190d95768d" />


<img width="1280" height="894" alt="Screenshot 2025-12-21 205407" src="https://github.com/user-attachments/assets/e162b5fd-b4e5-4329-ac09-4cc6c5b9f916" />

<img width="1280" height="891" alt="Screenshot 2025-12-21 205436" src="https://github.com/user-attachments/assets/9ae7893c-9999-45da-8104-993a418f8dbc" />

The firewall configuration

* SSH is allowed only from ypur workstation's IP address
* No other system can connect to the server
* All other connections are blocked

By using UFW we are able to configure a host based firewall to restrict incoming connections. Only SSH access is permitted only from the allowed workstation IP address. Everything else is denied by default. The following screenshots show this.

1. We give access to said workstation

<img width="1272" height="896" alt="Screenshot 2025-12-21 212606" src="https://github.com/user-attachments/assets/e0fbc740-090a-4769-b54b-246dcb5301a1" />

2. Next we set the default to deny incoming, and set the default to allow outgoing. Futhermore we then make sure the firewall is then enabled 

<img width="1278" height="896" alt="Screenshot 2025-12-21 212905" src="https://github.com/user-attachments/assets/f35f1a0b-a730-4503-a101-907c9da876c1" />

3. We make sure the settings are set correctly.

<img width="1274" height="891" alt="Screenshot 2025-12-21 213040" src="https://github.com/user-attachments/assets/d40ac8ff-8f13-4667-b085-cd3ea1c2335b" />

User Management and Privilege Control

Next we create a non-root user. This allows administrative tasks to be performed without enabling direct root access. This way by ensuring not everyone has root access privileges in line with least privileges. We can confirm that the user can login in on the same workstation with thier own account.

<img width="1279" height="894" alt="Screenshot 2025-12-21 221219" src="https://github.com/user-attachments/assets/d904538a-ed4c-4d62-974b-743ff616a907" />

<img width="1276" height="899" alt="Screenshot 2025-12-21 221700" src="https://github.com/user-attachments/assets/98251cb9-1ef8-49d7-94b3-7f7957d9d1ec" />

The following shows SSH access evidence for the new user. Keep in the mind the user already has the key added so they do not need to enter a password.

<img width="1276" height="896" alt="Screenshot 2025-12-21 224800" src="https://github.com/user-attachments/assets/d4e00bda-1bec-4419-a2fd-bac1d8ac588c" />

<img width="1281" height="893" alt="Screenshot 2025-12-21 224427" src="https://github.com/user-attachments/assets/37b4480c-10c6-4f49-8e48-b1b00a1e1f54" />

<img width="1275" height="894" alt="Screenshot 2025-12-21 223439" src="https://github.com/user-attachments/assets/e6bfadc6-b03d-4559-ba90-984a459c10fe" />



[Week Three](Week_3.md) | [Home](index.md) | [Week Five](Week_5.md)
