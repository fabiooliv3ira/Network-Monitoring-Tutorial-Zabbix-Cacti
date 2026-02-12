# Network Management: Zabbix vs. Cacti Implementation

![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Zabbix](https://img.shields.io/badge/Zabbix-v7.2.1-CC0000?style=for-the-badge&logo=zabbix&logoColor=white)
![Cacti](https://img.shields.io/badge/Cacti-v1.2.28-669933?style=for-the-badge&logo=cacti&logoColor=white)
![SNMP](https://img.shields.io/badge/Protocol-SNMP-blue?style=for-the-badge)

**Course:** Network Management (Gestão de Redes)  
**Institution:** ISEC - Instituto Superior de Engenharia de Coimbra  
**Year:** 2024/2025  
**Authors:** 
- [Fábio Oliveira](https://github.com/fabiooliv3ira)
- Carlos Emanuel Silva

This repository serves as a **practical manual** for deploying and configuring two of the most popular open-source network monitoring solutions: **Zabbix** and **Cacti**. 

Originally developed as a project for the **Network Management** course at ISEC, it provides a full walkthrough from fresh OS installation to real-time data visualization.

---

## Lab Environment

To follow this guide, we used the following environment:
*   **Hypervisor:** Oracle VM VirtualBox.
*   **Network Simulator:** GNS3 (for virtual Cisco Routers).
*   **Operating Systems:** 
    *   **Ubuntu 22.04 Noble** (Recommended for Zabbix).
    *   **Debian 12** (Used for Cacti automated setup).

---

## What this Tutorial Covers

### 1. Zabbix 7.2.1 Deployment
*   **Manual Installation:** Step-by-step commands for setting up the Zabbix Server, Frontend, and Agent.
*   **Database Setup:** Detailed SQL commands to initialize the MySQL/MariaDB backend.
*   **SNMP Integration:** How to configure a Cisco Router (IOU) to send data to Zabbix via SNMP v2c.
*   **Dashboarding:** How to create custom graphs and monitor interface traffic.

### 2. Cacti 1.2.28 Deployment
*   **Automated Installation:** Using a **Shell Script** to install the entire LAMP stack (Linux, Apache, MariaDB, PHP) and Cacti.
*   **RRDtool Configuration:** Setting up high-performance data logging and graphing.
*   **Host Monitoring:** How to monitor local server metrics like CPU Load, Memory, and Processes.

---

## Getting Started

### Installation & Configuration
1.  **Follow the Manual:** For a complete walkthrough with every terminal command and configuration detail, open the [Report & Step By Step Configuration Guide](Report%20%26%20Step%20By%20Step%20Configuration.pdf).
2.  **Automated Cacti Setup:** You can use the provided [ScriptCacti](ScriptCacti.sh) shell script to automate the installation process on a Debian 12 environment.
3.  **Project Context:** The original academic requirements can be found in the [Objectives](Objectives.pdf) file.

### Network Topology
The lab uses a central Cisco router connecting multiple subnets. You can find the GNS3 topology diagrams in the Report file.

---

## Results Showcase

The guide demonstrates how to capture:
*   **Network Traffic:** Bits received/sent per interface.
*   **Device Status:** Uptime tracking and operational alerts.
*   **System Health:** Memory usage and process monitoring via Cacti graphs.
