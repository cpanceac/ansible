# ansible

Make sure your hosts are listed in the inventory file. On Fedora 38 it's located in /etc/ansible/hosts .
Make sure you've uploaded your ($USER) public key to remote ystems. See some examples here: 
https://stackoverflow.com/questions/12392598/how-to-add-rsa-key-to-authorized-keys-file

Test connectivity with:

$ ansible all -m ping

Update one system:

$ ansible-playbook -T 30 -b --ask-become-pass  dnf_update.yaml 

Please note the usage of [fedora] and [debian] sections from /etc/ansible/hosts file.
Also please not that the formatiing is very important, wrong formatting will make your playbook unusable.
