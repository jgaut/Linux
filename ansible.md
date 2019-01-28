# Ansible

ansible-playbook test.yml --extra-vars "variable_host=all" -k

ansible splunk -m ping -u root --private-key=./.ssh/id_rsa
