# Linux Server Lab Projects

> A hands on collection of system administration, DevOps, and security labs built on Linux servers, documenting real configurations, automations, and hardening practices.

## Table of Contents
- [About the lab](#-about-the-lab)
- [Lab Modules](#-lab-modules)
- [Skills Demonstrated](#-skills-demonstrated)
- [Repository Structure](#-repository-structure)
- [Getting Started](#-getting-started)
- [Security & Ethics](#-security--ethics)

## About the lab
This repository contains practical linux server labs designed to build and document real-world administration, automation, and defensive security skills. Each lab is designed as a self-contained scenario, simulating a real operational task from diagnosis and implementation to validation and documentation (runbooks/postmortems).

## Lab Modules

### System Administration
| Lab                           | Focus                                 | Key Tools                                 |
|-------------------------------|---------------------------------------|-------------------------------------------|
| User & Group Management       | Access control, sudo policies         | `useradd`, `visudo`                       |
| File System & Permissions     | ACLs, ownership, hardening            | `chmod`, `chown`, `setfacl`               |
| Process & Service Management  | Systemd, resource monitoring          | `systemctl`, `top`, `journalctl`          |
| Storage & LVM                 | Disk partitioning, logic volumes      | `fdisk`, `lvm`, `mount`                   |
| Networking Fundamentals       | Ip config, DNS, firewall basics       | `ip`, `ss`, `ufw`                         |
| Backup & Restore Drill        | incremental syscs, full archives      | `rsync`, `tar`, `cron`                    |
| Web Service hosting           | Web services, reverse-proxy, ssl/tls  | `Apache/Nginx`, `certbot`                 |
| Database Server Administration| MariaDB/PostgreSQL, hardening         | `mysql_secure_installation`,`mysqldump`   |

### Devops & Automation
| Lab                       | Focus                             | Key Tools                 |
|---------------------------|-----------------------------------|---------------------------|
| Bash Automation           | Idepondent scripts, cron jobs     | Bash, `cron`              |
| Infrastructure as Code    | Server Provisioning               | Ansible / Terraform       |
| Containerization          | Dockerized services               | Docker, `docker-compose`  |
| CI/CD Pipeline            | Automated builds & deployments    | GitHub Actions / Jenkins  |
| Monitoring Stack          | Metrics, dashboards, alerting     | Prometheus, Grafana       |
| Log Aggregation & Aleting     | Centralized logging                   | `syslog`, `auth.log`, `ELK stack`         |
Configuration Management at Scale | applying hardening baseline | `ansible playbook` |

### Security & Hardening
| Lab                       | Focus                                 | Key Tools                 |
|---------------------------|---------------------------------------|---------------------------|
| SSH-Hardening             | Key-based auth, non-standard ports    | `sshd_config`, `fail2ban` |
| Firewall Configuration    | Least-privilege network rules         | `ufw`, `iptables`         |
| System Auditing           | Log analysis, intrusion detection     | `auditd`, `rsyslog`       |
| Vulnerability Scanning    | Local security assessment             | `Lynis`, `OpenVAS`        |
| Centralized Logging       | Security event correlation            | `rsyslog`, `Splunk`       |
| Red Team vs. Blue Team Simulation | bruteforcing, hardening | `nmap`, `hydra`, `fail2ban`, `ufw` |
| Mandatory Access Control (SELinux/AppArmor) | MAC frameworks | `auditd`, `AppArmor profiles`, `nginx` |
| File Integrity Monitoring (FIM) | Detecting changes | `wazuh` |

## Skills Demonstrated
- **Linux CLI & Shell Scripting** - daily driver for every lab
- **System Hardening** - applying CIS-style baselines to servers
- **Infrastructure Automation** - reducing manual toil with scripts and IaC
- **Security Operations** - log analysis, firewall rules, and audit trails
- **DevOps Toolchain** - containers, CI/CD, and observability

## Repository Structure
```text
linux-server-labs/
|---01-system-administration/
|       |---user-manangement/
|       |---file-permissions/
|       |---production-incident-response-drills/
|       |---backup-&-restore drill/
|       |---web-service-hosting-&-hardening/
|---02-devops-automation/
|       |---bash-scripting/
|       |---ansible-provisioning/
|       |---docker-services/
|---03-security-hardening/
|       |---ssh-hardening/
|       |---firewall-rules/
|       |---log-auditing/
|---docs/
|       |---architecture-diagrams/
|---README.md
```

## Getting Started
Each lab folder contains its own `README.md` with specific prerequisites and steps. General requirements:
- A Linux VM or bare-metal server (Ubuntu Server, RHEL-based, or Debian).
- SSH access and sudo privileges.
- Git for cloning the repository.

## Security & Ethics
All security labs are performed in isolated, personally owned environments (local VMs or dedicated lab servers). No techniques are documented against systems without explicit aythorization.


