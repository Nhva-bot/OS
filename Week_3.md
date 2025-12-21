Week Three (Application Selection for Performance Testing)

Objectives:
* Select applications representing different workload types
* Installation Documentation with exact commands for SSH-based installation
* Expected Resource Profiles documenting anticipated resource usage
* Monitoring Strategy explaining measurement approach for each application 

The following applications were selected to represent a range of workload types relevant to the server performance. And they as follow

* stree-ng: Workload type is that is CPU intensive. It will generate a controlled CPU load to evaluate processor utilisation and stability
  
* memtester: Workload type is RAM intensive. This tests memory allocation and stability under high memory usage

* fio: Workload type of I/O. Simulate read and write workloads to assess storage performance

* iperf3: Workload type of network. Measures the network throughput and latency between systems

* Apache2: Server application. Real world server workload handling client requests

The following shows the exact commands for SSH baased installation from the workstation to the server. The pictures show the server as well as the workstation side by side.

1. Logging into the server. ssh t@192.168.56.101

<img width="1278" height="891" alt="Screenshot 2025-12-21 182827" src="https://github.com/user-attachments/assets/c938c93e-4497-43c7-9656-16ef63b62bc8" />

2. Making sure everything is uptodate on the server

<img width="2558" height="902" alt="Screenshot 2025-12-21 172501" src="https://github.com/user-attachments/assets/c70a4ec4-b55a-4072-a393-4fc5b117959e" />

<img width="2559" height="899" alt="Screenshot 2025-12-21 172528" src="https://github.com/user-attachments/assets/49e970dd-6b3e-4f8d-ac0d-5a37729e7209" />

3. Installing stress-ng: sudo apt install stree-ng -y
   
   <img width="2559" height="902" alt="Screenshot 2025-12-21 172700" src="https://github.com/user-attachments/assets/15ae54f1-8d19-4e42-a24b-ffa62e589909" />

4. Installing memtester: sudo apt install memtester -y

   <img width="2559" height="901" alt="Screenshot 2025-12-21 172856" src="https://github.com/user-attachments/assets/7471a828-2669-4053-bce8-76a99453b613" />

5. Installing fio: susdo apt install fio -y

   <img width="2559" height="895" alt="Screenshot 2025-12-21 184155" src="https://github.com/user-attachments/assets/44906a45-974a-4ade-b57b-28c4af338872" />

6. Installing iperf3: sudo apt install iperf3 -y

   <img width="2559" height="900" alt="Screenshot 2025-12-21 173318" src="https://github.com/user-attachments/assets/6f3bebaf-9c16-4d8b-a408-12194130bb8d" />

7. Installing apache2: sudo apt install apache2 -y
   
<img width="2559" height="902" alt="Screenshot 2025-12-21 173749" src="https://github.com/user-attachments/assets/0da0c483-f07b-4e74-84bc-60417e778f67" />

[Week Two](Week_2.md) | [Home](index.md) | [Week Four](Week_4.md)
