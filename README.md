# ansible-CodeIgniter
This repo contains ansible playbook which includes roles for deploying CodeIgniter framework, nginx, php and MySQL.

###ROles include
- common: basic debian package
- Letsencrypt
- CodeIgniter framework base
- Nginx(webserver prefered)
- PHP
- Mysql(DB)
- Iptables(incomplete)
- Swapfile



##Running Ansible deployment as a standalone command

`ansible-playbook -i hosts playbooks/web-playbook.yml`
