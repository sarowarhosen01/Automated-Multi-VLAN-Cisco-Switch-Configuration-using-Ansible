# Automated Cisco Switch Configuration using Ansible

A complete Ansible automation project for configuring multiple Cisco switches with VLAN segmentation, access ports, and trunking.

![Cisco Network](https://via.placeholder.com/800x400?text=Cisco+Switches+Automation)  
*(Replace with actual topology diagram)*

## 📋 Project Overview

This project automates the initial configuration of 7 Cisco switches (SW1 to SW7) in a multi-department enterprise network. It includes:

- Hostname configuration
- Creation of 9 VLANs (IT, HR, Sales, Finance, Server, CCTV, WiFi, Guest, Management)
- Access port configuration with PortFast
- Trunk port configuration (802.1Q)
- Configuration persistence

## 🛠 Technologies Used

- **Ansible** (Core + Cisco IOS Collection)
- **Cisco IOS** (Layer 2 Switches)
- **YAML** (Playbook & Inventory)
- **Git** (Version Control)
- **Cisco Packet Tracer / EVE-NG / GNS3** (Lab Environment)

## 🌐 Network Design

- **VLANs Configured:**
  | VLAN ID | Name         | Purpose              |
  |---------|--------------|----------------------|
  | 10      | IT           | IT Department        |
  | 20      | HR           | Human Resources      |
  | 30      | SALES        | Sales Team           |
  | 40      | FINANCE      | Finance Department   |
  | 50      | SERVER       | Servers              |
  | 60      | CCTV         | Surveillance         |
  | 70      | WIFI         | Wireless Users       |
  | 80      | GUEST        | Guest Network        |
  | 110     | MANAGEMENT   | Switch Management    |

- **Port Assignments:**
  - Gi0/1 to Gi0/9 → Access ports (different VLANs)
  - Gi0/0 → Trunk port (to Router/Core Switch)

## 📁 Project Structure

```bash
Cisco-Automation-Project/
├── inventory/
│   └── hosts
├── playbooks/
│   └── switch_configuration.yml
└── README.md
