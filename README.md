
---

### Outline VPN Server Ansible Playbook

This playbook allows for quick deployment and configuration of an Outline VPN server using Ansible.

#### Requirements:

* Ansible installed on your local machine
* SSH access (IP address and password) to the target host
* Telegram Bot Token and your Telegram Chat ID (to send the access key after setup)

#### Usage:

1. Encrypt sensitive variables using `ansible-vault`:

   ```bash
   ansible-vault encrypt_string 'my_secret_value' --name 'telegram_token' >> vault.yml
   ```

   Repeat for other secrets (e.g., `telegram_chat_id`, `server_password`, etc.).

2. Run the playbook:

   ```bash
   ansible-playbook -i inventory setup-outline.yml --ask-vault-pass
   ```

This will install Outline, configure the server, and send you the access key via Telegram.

---
