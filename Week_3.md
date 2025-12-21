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

1. Logging into the server from the workstation. ssh t@192.168.56.101

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

The resource usage is based on the primary function of each selected application. Each application was chosen to represent a specific workload type. As a result, the expected CPU, memory, disk I/O, and network usage can be identified based on which resource is most heavily utilised by the application being tested. 

<img width="1274" height="520" alt="Screenshot 2025-12-21 191156" src="https://github.com/user-attachments/assets/a75a31db-7712-4918-a213-bd63bbfde1c5" />

Monitoring Strategy

CPU was intensive as we stress-ng was running. The command top is used to monitor real-time CPU usage and identify stree-ng process while running uptime to observe load averages. This gives us an over view of the load affected over the system behaviour.

As memtester ran we looked at the memory usage. free -h command was used to track memory consumption and the available memory. By using vmstat and free-h we are snabled to identify memory pressure and system reponsiveness during the test.

Both iostat and vmstat were used for disk performance as fio was running to evaluate read and write activity. iostat is used to measure disk throughput wait times and vmstat provided addtional context on system performancce.

iperf3 was used to generate traffic between Ubuntu workstation and the server. This gives use network performance through the use of iperf3 output. While ss command is used to monitor active network connections on the server.

Apach2 performance was monitored by looking at the system resources usage and service by using the top command and ss. top for the CPU usage and memory. ss was used for active network connections. journalctl -u apache2 is used for the review of service logs for errors or abnormal behaviour.



[Week Two](Week_2.md) | [Home](index.md) | [Week Four](Week_4.md)
