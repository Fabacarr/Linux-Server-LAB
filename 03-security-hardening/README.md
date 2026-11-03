# Lab [NN] — [Short Descriptive Title]

# Lab — Patch Management & Kernel Rollback

> **Status:** 🚧 In Progress  
> **Last updated:** 2026-11-03

## 📖 Overview
One paragraph describing the operational scenario. What system, what risk, what outcome?
Example: "A production web server is running an outdated kernel with a known CVE. This lab applies security patches during a maintenance window and validates rollback in case the new kernel breaks the application."

## 🎯 Learning Outcomes
By the end of this lab, you will be able to:
- [ ] [Outcome 1 — e.g., "Perform a kernel update with dnf and verify the running kernel"]
- [ ] [Outcome 2 — e.g., "Roll back to the previous kernel using grubby"]
- [ ] [Outcome 3 — e.g., "Document a maintenance‑window runbook"]

## ✅ Prerequisites
- A Linux VM (Ubuntu Server 24.04 / Rocky Linux 9 / Debian 12)
- SSH access with sudo
- [Tool, e.g., Ansible installed on the control node]
- [Prior lab dependency, if any]

## 🧪 Scenario / Task
Describe the exact task as if it were assigned by a manager:
"Apply all security updates to the server, reboot if required, and confirm the application health endpoint returns HTTP 200. If the kernel update causes a boot failure, restore the previous kernel."

## 🪜 Steps
1. **Snapshot the VM** (record the snapshot name).
2. **Capture baseline evidence:** `uname -r`, `rpm -qa | sort`, `systemctl --failed`.
3. **Apply updates:** `sudo dnf update -y --security` (or `apt upgrade`).
4. **Reboot** if the kernel changed.
5. **Validate:** `uname -r`, `systemctl --failed`, health‑check command.
6. **Rollback drill:** boot the previous kernel, confirm it works, then return to the new kernel.

## 📸 Evidence / Validation
Paste or link:
- Before/after `uname -r` output.
- `systemctl --failed` showing zero failed units.
- Health‑check response.
- Rollback boot log snippet.

## 🧯 Troubleshooting Notes
What went wrong? What did you check? Include the command that revealed the issue and the fix.
Example: "The service failed after reboot because the new kernel removed a legacy module. `journalctl -u <service> -b` showed the missing dependency."

## 🧹 Cleanup
- Revert snapshots.
- Remove temporary files or test users.
- Document any leftover configuration.

## 📚 Lessons Learned
Two or three bullets on what you would do differently in production. This is what turns a command log into a portfolio narrative.

## 🔗 References
- Vendor documentation links.
- CIS benchmark control numbers (if applicable).
- Related runbook or postmortem files.
