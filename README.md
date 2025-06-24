# 📘 Ansible Assignments

This repository contains two Ansible assignments:

```
ansible_assignments/
├── assignment2/
│   ├── inventory.ini
│   ├── site.yml
│   └── roles/
│       └── compliance/
│           ├── tasks/
│           ├── vars/
│           └── templates/
└── assignment3/
    ├── inventory.ini
    ├── site.yml
    └── roles/
        └── backup/
            ├── tasks/
            └── vars/
```

---

## ✅ Assignment 2: System Compliance

### 🔍 Objective

Automate system compliance checks by:

- ✅ Installing required packages (e.g., `git`, `htop`, `curl`)
- ❌ Removing forbidden packages (e.g., `telnet`, `vsftpd`)
- 🚀 Enabling and starting required services (e.g., `sshd`, `cron`)
- ⛔ Disabling and stopping forbidden services
- 🧾 Generating a detailed compliance report

### ▶️ How to Run

```bash
cd assignment2
ansible-playbook -i inventory.ini site.yml
```

### 📄 Output

A compliance report will be generated at:

```
/tmp/compliance_report.txt
```

---

## 💾 Assignment 3: Backup and Restore

### 🔍 Objective

Automate the backup and restoration of directories using Ansible:

- 📦 Compress a source directory into a timestamped `.tar.gz` archive
- 💾 Store it in a configurable backup directory
- 🔁 Restore the latest backup when needed

### ⚙️ Configuration

Edit the `site.yml` file to set the backup action:

```yaml
action: backup   # Options: 'backup' or 'restore'
```

You can also customize variables in `group_vars` or `vars` files:

- `source_dir` – directory to back up (default: `/etc`)
- `backup_dir` – where to store backups (default: `/tmp/backups`)

### ▶️ How to Run

```bash
cd assignment3
ansible-playbook -i inventory.ini site.yml
```

---

## 🛠 Requirements

- Ansible
- Python 3
- (Optional) Docker — if using Molecule for role testing

To install Ansible:

```bash
pip install ansible
```

---

## 📬 Contact
zalhabibi@pros.com
