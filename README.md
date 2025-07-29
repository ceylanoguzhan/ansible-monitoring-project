# Ansible Monitoring Project

This project automates the installation and configuration of **Prometheus**, **Grafana**, and **Node/Windows Exporters** using **a single Ansible playbook**.  
It demonstrates how to implement **Infrastructure as Code (IaC)** for centralized monitoring in a professional, scalable way.

---

## 🚀 Features

- Fully automated deployment of:
  - **Prometheus** (Monitoring & Metrics storage)
  - **Grafana** (Visualization & Dashboards)
  - **Node Exporter** (Linux metrics)
- Centralized configuration using a single `install_monitoring.yaml` playbook
- Ready-to-use dashboards for both Linux and Windows environments
- No manual steps required: everything is handled by Ansible

---

## 📂 Project Structure

```bash
ansible-monitoring-project/
├── install_monitoring.yaml    # Ansible playbook for full monitoring stack
└── inventory.ini               # Inventory file (hosts & groups)
```

---

## ⚙️ Requirements

- **Ansible Control Node** (Ansible 2.9+)
- At least **2 target servers**:
  - One Linux server for **Prometheus & Grafana**
  - One or more Linux/Windows servers with **Exporters**
- SSH keys configured (for Linux) and WinRM (for Windows)

---

## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/ceylanoguzhan/ansible-project.git
   cd ansible-project
   ```

2. Update your **inventory.ini** with the correct IPs:
   ```ini
   [prometheus]
   192.168.x.x ansible_user=root

   [grafana]
   192.168.x.x ansible_user=root

   [exporters]
   192.168.x.x ansible_user=root
   ```

3. Run the Ansible playbook:
   ```bash
   ansible-playbook -i inventory.ini install_monitoring.yaml
   ```

---


---

## 💡 Why This Project?

- Shows **best practices** for Infrastructure as Code
- Builds a **production-ready monitoring stack**
- Useful for **DevOps engineers**, **system admins**, and **automation enthusiasts**

---

## ✨ Future Improvements

- Add **Alertmanager** integration
- Implement **role-based Ansible structure**
- Add **TLS & authentication** for Grafana and Prometheus

