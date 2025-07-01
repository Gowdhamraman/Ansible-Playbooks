# Ansible Playbook: Fetch User and Group Details Across Cluster

This Ansible playbook fetches user and group information for a specified user across a set of servers.

---

## Features

- Checks if a given user exists on each target host.
- Retrieves user ID (UID), group ID (GID), and group memberships.
- Shows the user's `/etc/passwd` and group entries.
- Gracefully reports hosts where the user does not exist.
- Requires a username input at runtime to avoid accidental runs.

---

## Prerequisites

- Ansible installed on the control machine.
- SSH access with privilege escalation (sudo) to target hosts.
- Inventory file listing your target servers.

---

## Usage

### Run the playbook with a specified username

```bash
ansible-playbook fetch_user_info.yml -i your_inventory_file -e "username=someuser"
