# ansible-CodeIgniter
This repo contains ansible playbook which includes roles for deploying CodeIgniter framework, nginx, php and MySQL.

###ROles include
- common: basic debian package
- CodeIgniter framework base
- Nginx(webserver prefered)
- PHP
- Mysql(DB)
- Iptables
- Swapfile



##Running Ansible deployment as a standalone command

`ansible-playbook -i hosts web-playbook.yml`
