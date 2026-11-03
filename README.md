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
| Lab                               | Focus                                 | Key Tools                                 | Status            |
|-----------------------------------|---------------------------------------|-------------------------------------------|-------------------|
| User & Group Management           | Access control, sudo policies         | `useradd`, `visudo`                       | In Progress       |
| File System & Permissions         | ACLs, ownership, hardening            | `chmod`, `chown`, `setfacl`               | In Progress       |
| Process & Service Management      | Systemd, resource monitoring          | `systemctl`, `top`, `journalctl`          | In Progress       |
| Storage & LVM                     | Disk partitioning, logic volumes      | `fdisk`, `lvm`, `mount`                   | Planned           |
| Networking Fundamentals           | Ip config, DNS, firewall basics       | `ip`, `ss`, `ufw`                         | Planned           |
| Backup & Restore Drill            | incremental syncs, full archives      | `rsync`, `tar`, `cron`                    | Planned           |
| Web Service hosting               | Web services, reverse-proxy, ssl/tls  | `Apache/Nginx`, `certbot`                 | Planned           |
| Database Server Administration    | MariaDB/PostgreSQL, hardening         | `mysql_secure_installation`,`mysqldump`   | Planned           |
| Patch Management & Kernel Rollback| Security patches, rollback drill      | `dnf`, `grubby`                           | Planned           |

### Devops & Automation
| Lab                               | Focus                             | Key Tools                         | Status            |
|-----------------------------------|-----------------------------------|-----------------------------------|-------------------|
| Bash Automation                   | Idepotent scripts, cron jobs     | Bash, `cron`                      | Planned           |
| Infrastructure as Code            | Server Provisioning               | Ansible / Terraform               | Planned           |
| Containerization                  | Dockerized services               | Docker, `docker-compose`          | Planned           |
| CI/CD Pipeline                    | Automated builds & deployments    | GitHub Actions / Jenkins          | Planned           |
| Monitoring Stack                  | Metrics, dashboards, alerting     | Prometheus, Grafana               | Planned           |
| Log Aggregation & Alerting         | Centralized logging               | `syslog`, `auth.log`, `ELK stack` | Planned           |
| Configuration Management at Scale | applying hardening baseline       |  ansible playbook                 | Planned           |

### Security & Hardening
| Lab                                           | Focus                                 | Key Tools                             | Status            |
|-----------------------------------------------|---------------------------------------|---------------------------------------|-------------------|
| SSH-Hardening                                 | Key-based auth, non-standard ports    | `sshd_config`, `fail2ban`             | Planned           |
| Firewall Configuration                        | Least-privilege network rules         | `ufw`, `iptables`                     | Planned           |
| System Auditing                               | Log analysis, intrusion detection     | `auditd`, `rsyslog`                   | Planned           |
| Vulnerability Scanning                        | Local security assessment             | `Lynis`, `OpenVAS`                    | Planned           |
| Centralized Logging                           | Security event correlation            | `rsyslog`,    Splunk                  | Planned           |
| Red Team vs. Blue Team Simulation             | bruteforcing, hardening               | `nmap`, `hydra`, `fail2ban`, `ufw`    | Planned           |
| Mandatory Access Control (SELinux/AppArmor)   | MAC frameworks                        | `auditd`, AppArmor profiles, `nginx`  | Planned           |
| File Integrity Monitoring (FIM)               | Detecting changes                     | wazuh                                 | Planned           |

##  Skills Demonstrated

### Linux System Administration
- **Enterprise Linux distributions** — Ubuntu, Debian, RHEL, Rocky Linux, AlmaLinux
- **Package & patch management** — `dnf`, `yum`, `apt`, security updates, kernel rollback with `grubby`
- **Storage & filesystems** — LVM, partitioning, ACLs, `fstab`, mount options
- **Service management** — systemd units, timers, `journalctl`, resource monitoring
- **Networking** — TCP/IP, DNS (BIND9), DHCP, firewalls (`ufw`, `iptables`, `nftables`)
- **Web & database services** — Nginx/Apache virtual hosts, reverse proxy, TLS with `certbot`, MariaDB/PostgreSQL hardening and backup

### DevOps & Automation
- **Configuration management** — Ansible roles, idempotent playbooks, CIS baseline enforcement
- **Infrastructure as Code** — Terraform provisioning, state management, teardown
- **Containers** — Docker, Docker Compose, container healthchecks, basic orchestration awareness
- **CI/CD** — GitHub Actions / Jenkins pipelines, security gates, build-test-deploy flows, rollback strategies
- **Observability** — Prometheus metrics, Grafana dashboards, centralized logging (Loki/ELK), alerting

### Security & Hardening
- **SSH & access control** — key-based authentication, `fail2ban`, PAM, MFA/TOTP
- **Mandatory Access Control** — SELinux policy modules, AppArmor profiles, denial analysis with `ausearch`
- **Auditing & integrity** — `auditd` rules, AIDE/Wazuh file integrity monitoring, log analysis
- **Vulnerability management** — `Lynis`, OpenVAS, patch validation, CVE remediation workflows
- **Defensive operations** — red team vs. blue team drills, incident detection, runbook and postmortem authoring

### Operational & SRE Competencies
- **Incident response** — diagnosis and recovery from disk-full, inode exhaustion, OOM kills, systemd crashloops
- **Backup & disaster recovery** — `rsync`, `tar`, database dumps, live restore validation
- **Documentation** — runbooks, postmortems, reproducible lab narratives
- **Scripting** — Bash automation, Python for tooling and integration

## Repository Structure
```text
Linux-Server-LAB/
├── 01-system-administration/
│   ├── user-management/
│   ├── file-permissions-acls/
│   ├── process-service-management/
│   ├── storage-lvm/
│   ├── networking-fundamentals/
│   ├── backup-restore-drill/
│   ├── web-service-hosting-tls/
│   ├── database-administration/
│   ├── patch-management-kernel-rollback/   ← from the expanded list
│   └── incident-response-drills/           ← disk-full, inode, OOM, systemd
│
├── 02-devops-automation/
│   ├── bash-automation/
│   ├── ansible-provisioning/
│   ├── docker-services/
│   ├── ci-cd-pipeline-security-gates/
│   ├── monitoring-stack/
│   ├── centralized-logging-alerting/
│   └── idempotent-cis-hardening/           ← Ansible run twice, changed=0
│
├── 03-security-hardening/
│   ├── ssh-hardening/
│   ├── firewall-configuration/
│   ├── system-auditing-auditd/
│   ├── vulnerability-scanning/
│   ├── selinux-apparmor-confinement/
│   ├── file-integrity-monitoring/
│   └── red-team-blue-team-drill/
│
├── docs/
│   ├── architecture-diagrams/
│   ├── runbook-template.md
│   ├── postmortem-template.md
│   └── lab-readme-template.md
│
├── .github/
│   └── workflows/                          ← optional, for CI later
│
├── SECURITY.md
├── LICENSE
├── .gitignore
└── README.md```

## Getting Started
Each lab folder contains its own `README.md` with specific prerequisites and steps. General requirements:
- A Linux VM or bare-metal server (Ubuntu Server, RHEL-based, or Debian).
- SSH access and sudo privileges.
- Git for cloning the repository.

## Security & Ethics
All security labs are performed in isolated, personally owned environments (local VMs or dedicated lab servers). No techniques are documented against systems without explicit authorization.


