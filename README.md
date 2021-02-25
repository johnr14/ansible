# ansible
Yet-an-other ansible

ansible-playbook -i hosts workstation.yml --tags=show_output  -vvv 

Notes to self :

Network :

Try guessing main IP of target host : 
> ansible_default_ipv4.address|default(ansible_all_ipv4_addresses[0])


> hostvars[inventory_hostname]['ansible_default_ipv4']['address']


Run scripts and only once
https://blog.programster.org/ansible-run-a-local-script-on-remote-server


Check if need restarting Fedora:
https://www.thegeekdiary.com/how-to-check-if-a-service-restart-or-server-reboot-is-required-after-rpm-package-update-centos-rhel-fedora/
