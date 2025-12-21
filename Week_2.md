Week Two (Security Planning and Testing Methodology)

Objectives:
* Create a performance testing plan describing Remote Monitoring Methodology
* Security Configuration Checklist (SSH hardening, firewall configuration, MAC,  automatic updates, user privilege management, and network security)
* Threat Model identifying

All monitoring and testing activities will be performed using the command-line interface (CLI). Performance data will be collected remotely from the Ubuntu Desktop workstation by connecting to the Ubuntu Server system via SSH. The things we will look at are as follow:

* CPU utilisation
* Memory usage
* Disk space utilisation
* Network activity

Remote Monitoring Methodology tools:
As we carrying this out remotely using SSH the following tools will be used:
* top/htop - CPU and memory usage
* vmstat - memory and process
* iostat - disk I/O performance
* free -h - memory usage
* ss - network connections
* iperf3 - network throughput and latency
* journalctl - system and service logs

By applying the above tools we will be able to get performance monitoring information, security hardening, and and potential operational issues.

Security Configuration will focus on verfying and security conttrols. This would be secure remote access, firewall enforcement, access control and system update polices. This will be carried out through CLI monitoring tools.

Identified Threats

Unauthorized Access - Unauthorised SSH login attempts : Harden SSH, disable root login, enforce secure                                                             authentication, restricting access with firewall rules.



[Week One](Week_1.md) | [Home](index.md) | [Week Three](Week_3.md)
