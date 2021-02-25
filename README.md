# ansible
Yet-an-other ansible

ansible-playbook -i hosts workstation.yml --tags=show_output  -vvv 

Notes to self :

Network :

Try guessing main IP of target host : 
> ansible_default_ipv4.address|default(ansible_all_ipv4_addresses[0])
or 
> hostvars[inventory_hostname]['ansible_default_ipv4']['address']
