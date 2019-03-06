# Ansible

#### Blog
https://prefetch.net/blog/2017/08/27/using-ansible-to-verify-remote-file-checksums-with-get_url-lookup-and-stat/

#### Commandes
```
ansible-playbook test.yml --extra-vars "variable_host=all" -k

ansible splunk -m ping -u root --private-key=./.ssh/id_rsa
```

#### Aide
https://www.ansible.com/blog/connecting-to-a-windows-host