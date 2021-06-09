# net-dev-bavkup
ansible playbooks to backup network devices

for small business cisco series on device side: ip ssh password-auth

look to catalog paths in playbooks



Backups:

  1. cd ~/net-dev-backup
  2. ansible-vault create cisco-credential.yml (or something else)
  3. launch your playbook use --ask-vault-pass
     or --vault-password-file=.ansible_vault_pass
     
     
     
     CRON:
     
     0 */5 * * *    if ! out=`ansible-playbook -i ПУТЬ/net-dev-backup/hosts.yml -l cisco ПУТЬ/net-dev-backup/stats.yml --vault-password-file=ПУТЬ/net-dev-backup/.ansible_vault_pass`; then echo $out; fi
     
     0 */5 * * *    if ! out=`ansible-playbook -i ПУТЬ/net-dev-backup/hosts.yml -l cisco ПУТЬ/net-dev-backup/backup.yml --vault-password-file=ПУТЬ/net-dev-backup/.ansible_vault_pass`; then echo $out; fi
