# ansible
Yet-an-other ansible

ansible-playbook -i hosts workstation.yml --tags=show_output  -vvv 

Tags list and definitions:
always
configure_host
configure_host-set_hostname
first_run
flatpak
install_archive_packages
install_base
install_base_packages
install_codecs_packages
install_flathub
install_flatpak_app
install_fonts_packages
install_hardware_packages
install_kde_packages
install_rpmfusion
never
packages_install
repositories
rpmfusion
show_output : be more verbose
update
upgrade_system

Tasks lists and summary:


List to TODO:
Tags cleanup and standardisation
Allow show_output on every tasks
roles/packages/task/install_base.yml TODO: Allow installation depending on distribution and distribution family
roles/packages/task/install_base.yml TODO: COMBINE ALL LISTS TO DO A SINGLE INSTALL !! 
roles/packages/tasks/cleanup.yml TODO: Remove cache and remove unwanted packages
workstation.yml TODO: Write a logfile


List of FIXME:
roles/flatpak/tasks/main.yml FIXME: Upgrade fail with error when run as root "Failed to download missing issuer certificate from Authority"


Notes to self :

Network :

Try guessing main IP of target host : 
> ansible_default_ipv4.address|default(ansible_all_ipv4_addresses[0])


> hostvars[inventory_hostname]['ansible_default_ipv4']['address']


Run scripts and only once
https://blog.programster.org/ansible-run-a-local-script-on-remote-server


Check if need restarting Fedora:
https://www.thegeekdiary.com/how-to-check-if-a-service-restart-or-server-reboot-is-required-after-rpm-package-update-centos-rhel-fedora/
