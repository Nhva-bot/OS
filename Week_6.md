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


<img width="1200" height="410" alt="Screenshot 2025-12-22 102853" src="https://github.com/user-attachments/assets/00190f33-1fca-4f02-88b3-f59933f5dd6e" />


<img width="697" height="474" alt="Screenshot 2025-12-22 104626" src="https://github.com/user-attachments/assets/f1a25bf4-f657-4ec6-8071-f195ece8073e" />

Next we look at the memory. We start by getting the base before loading. When we starting the loading we can see an increase in memory. And the results as follow.

<img width="1272" height="897" alt="Screenshot 2025-12-22 105213" src="https://github.com/user-attachments/assets/71f9a1be-bcc2-403a-bad7-c884d61ed8b4" />

<img width="1268" height="897" alt="Screenshot 2025-12-22 105611" src="https://github.com/user-attachments/assets/07d4e7ce-c68d-458d-bbcb-b678084b9304" />

<img width="1269" height="899" alt="Screenshot 2025-12-22 105634" src="https://github.com/user-attachments/assets/c0fb999c-7b6b-4a1e-a079-a3a096360b28" />

<img width="1269" height="897" alt="Screenshot 2025-12-22 105755" src="https://github.com/user-attachments/assets/039e6fe4-dfca-45bf-8fb1-6e30c0664bad" />

<img width="976" height="366" alt="Screenshot 2025-12-22 110540" src="https://github.com/user-attachments/assets/74a0cc23-a96e-488d-936a-649f746d884f" />

Next we have the disk I/O running the fio application. Using fio to generate a mixed read and write workload test we can see active disk increase with sustained read and write.

<img width="1275" height="895" alt="Screenshot 2025-12-22 110928" src="https://github.com/user-attachments/assets/599b31a3-9bb1-4eeb-8b00-e07fe5e2ea01" />

<img width="1275" height="895" alt="Screenshot 2025-12-22 110928" src="https://github.com/user-attachments/assets/cf9a49d7-d849-4085-bded-3a3e4f8b39fc" />

<img width="1262" height="900" alt="Screenshot 2025-12-22 111320" src="https://github.com/user-attachments/assets/be389feb-7b59-4a55-8dbb-59c60765d2ab" />

<img width="1275" height="899" alt="Screenshot 2025-12-22 111408" src="https://github.com/user-attachments/assets/8902a1bd-54ee-4d80-b94c-12f9d83dea64" />

<img width="1067" height="307" alt="Screenshot 2025-12-22 111804" src="https://github.com/user-attachments/assets/89143046-86c7-496c-98d3-8603a901d6e4" />



[Week Five](Week_5.md) | [Home](index.md) | [Week Seven](Week_7.md)
