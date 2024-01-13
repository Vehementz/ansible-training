

#### Install apache
ansible-playbook -i inventaire.ini --become --ask-become-pass install-apache.yml

#### Install mediawiki
ansible-playbook -i inventaire.ini --become --ask-become-pass --ask-vault-pass install-mediawiki.yml 


