Week Six (Performance Evaluation and Analysis)

* Execute detailed performance testing and analyse operating system behaviour under different workloads.

In this week we look at the performance following the testing plan we had made in the pervious week. We will apply our testing methodology on the applications we chose. To be able to see the information, we also made a script to show the performance of the system before loading any of the application. You can see it below.

<img width="1277" height="896" alt="Screenshot 2025-12-22 100842" src="https://github.com/user-attachments/assets/8b74c58d-9eaa-438b-91f1-03226cb7e7f0" />

The first test we run will look at the CPU performance testing. This will be done by using stress-ng to generate controlled processor load. During testing CPU utilisation and system load increased showing CPU workload behaviour. The results can be seen below.

<img width="1273" height="899" alt="Screenshot 2025-12-22 101524" src="https://github.com/user-attachments/assets/af600bd8-da10-4c55-9165-35b10c60dd65" />

<img width="1275" height="901" alt="Screenshot 2025-12-22 101618" src="https://github.com/user-attachments/assets/2ebb54be-eb6a-4a55-967f-b40878dfc91c" />

<img width="1273" height="900" alt="Screenshot 2025-12-22 101728" src="https://github.com/user-attachments/assets/42b1d265-80d6-4e08-89f2-e56da1b83497" />


<img width="1271" height="905" alt="Screenshot 2025-12-22 101826" src="https://github.com/user-attachments/assets/04b4d5bc-0cf4-4534-8655-8abccac66842" />

<img width="1274" height="897" alt="Screenshot 2025-12-22 102311" src="https://github.com/user-attachments/assets/433f8d35-8a71-4e70-ad94-934e9a1afe79" />


<img width="1010" height="352" alt="Screenshot 2025-12-22 123927" src="https://github.com/user-attachments/assets/12cca16e-a3a6-4354-a782-27facb032591" />


<img width="697" height="474" alt="Screenshot 2025-12-22 104626" src="https://github.com/user-attachments/assets/f1a25bf4-f657-4ec6-8071-f195ece8073e" />

Next we look at the memory. We start by getting the base before loading. When we starting the loading we can see an increase in memory. And the results as follow.

<img width="1272" height="897" alt="Screenshot 2025-12-22 105213" src="https://github.com/user-attachments/assets/71f9a1be-bcc2-403a-bad7-c884d61ed8b4" />

<img width="1268" height="897" alt="Screenshot 2025-12-22 105611" src="https://github.com/user-attachments/assets/07d4e7ce-c68d-458d-bbcb-b678084b9304" />

<img width="1269" height="899" alt="Screenshot 2025-12-22 105634" src="https://github.com/user-attachments/assets/c0fb999c-7b6b-4a1e-a079-a3a096360b28" />

<img width="1269" height="897" alt="Screenshot 2025-12-22 105755" src="https://github.com/user-attachments/assets/039e6fe4-dfca-45bf-8fb1-6e30c0664bad" />

<img width="1059" height="345" alt="Screenshot 2025-12-22 123937" src="https://github.com/user-attachments/assets/80be4dc9-450a-4c31-9669-052e359220bc" />

<img width="717" height="483" alt="Screenshot 2025-12-22 112634" src="https://github.com/user-attachments/assets/aadd608c-375a-4248-944a-29e8c6ac31cb" />

Next we have the disk I/O running the fio application. Using fio to generate a mixed read and write workload test we can see active disk increase with sustained read and write.

<img width="1275" height="895" alt="Screenshot 2025-12-22 110928" src="https://github.com/user-attachments/assets/599b31a3-9bb1-4eeb-8b00-e07fe5e2ea01" />

<img width="1275" height="895" alt="Screenshot 2025-12-22 110928" src="https://github.com/user-attachments/assets/cf9a49d7-d849-4085-bded-3a3e4f8b39fc" />

<img width="1262" height="900" alt="Screenshot 2025-12-22 111320" src="https://github.com/user-attachments/assets/be389feb-7b59-4a55-8dbb-59c60765d2ab" />

<img width="1275" height="899" alt="Screenshot 2025-12-22 111408" src="https://github.com/user-attachments/assets/8902a1bd-54ee-4d80-b94c-12f9d83dea64" />

<img width="1153" height="356" alt="Screenshot 2025-12-22 123947" src="https://github.com/user-attachments/assets/68ec41a1-598e-4875-8746-06bf8d5fdbee" />

<img width="795" height="500" alt="Screenshot 2025-12-22 112425" src="https://github.com/user-attachments/assets/72378a2a-6a44-43d0-b06a-e02a433af28b" />

Now we look at the network. From the first picture we can see that the server is actively accepting network traffic and 5201 is in use. Next we can confirm that we can connect to the server and we show throughput measurement in the following picture. 

<img width="1274" height="899" alt="Screenshot 2025-12-22 113950" src="https://github.com/user-attachments/assets/5df91fe3-b6c1-4938-95c8-8f809227db26" />

<img width="1279" height="896" alt="Screenshot 2025-12-22 122531" src="https://github.com/user-attachments/assets/c9b3656a-2862-487b-a30e-db84c719c224" />

<img width="1274" height="895" alt="Screenshot 2025-12-22 122752" src="https://github.com/user-attachments/assets/7a9b1b72-48b1-476a-9f46-299ed55f8ad8" />

<img width="1271" height="902" alt="Screenshot 2025-12-22 123047" src="https://github.com/user-attachments/assets/971adb1c-5c44-42f1-a9c2-ffd6852cc0c6" />

<img width="1020" height="379" alt="Screenshot 2025-12-22 123832" src="https://github.com/user-attachments/assets/ce9ad586-40b1-49d6-a530-c009fed2fee2" />

Bottleneck Identification

From the tests carried out we can see where the bottlenecks come into during stress testing as expected. This was very clear on the CPU. Memory capacity was enough and did not limit performance.

Optimisation

The two optimisation done was SSH hardening and was Firewall configuration. By restricting SSH access to a single workstation and enforcing key based authentication we make sure unnecessary network exposure and reduce impact performance

* sudo nano /etc/ssh/sshd_config
* sudo ufw default deny incoming
* sudo ufw default allow outgoing
* sudo ufw enable



[Week Five](Week_5.md) | [Home](index.md) | [Week Seven](Week_7.md)
