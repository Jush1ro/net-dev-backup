# net-dev-bavkup
ansible playbooks to nackup network devices

Backups:
  1. cd ~/net-dev-backup
  2. ansible-vault create cisco-credential.yml (or something else)
  3. launch your playbook use --ask-vault-pass
     or --vault-password-file=.ansible_vault_pass
