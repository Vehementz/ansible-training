

#### Install apache
ansible-playbook -i inventaire.ini --become --ask-become-pass install-apache.yml

#### Install mediawiki
ansible-playbook -i inventaire.ini --become --ask-become-pass --ask-vault-pass install-mediawiki.yml 

##### To crypt 
ansible-vault encrypt_string 'lemotdepass' --vault-password-file ./crypt.txt
############# lemotdepass: 'variable to encrypt' , puis ./crypt comme fichier de clé de cryptage


#### Exemple playbook with variable encrypted in file
ansible-playbook -i hosts.yml --vault-password-file ./crypt.txt -t oki -b playbook.yml

#### Encrypt file in /files/secrets/ directory
ansible-vault encrypt credentials.yml
