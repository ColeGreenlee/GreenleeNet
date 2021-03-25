# :zap: **GreenleeNet Ansible Configuration Notes**

## Helpful Commands I Need To Remember

Run an Ansible playbook:
```bash
ansible-playbook /path/to/playbook.yml -i /path/to/inventory.yml -u user_to_run_as
```

Example of previous command (Initialize all servers in inventory):
```bash
ansible-playbook playbooks/ubuntu_initial_configuration.yml -i hosts.yml -u root
```

Install Ansible collections and roles from requirements.yml:
```bash
ansible-galaxy collection install -r requirements.yml 
```

Ping all servers in inventory (good for ensuring everything is alive):
```bash
ansible -i hosts.yml all -m ping
```