# ansible
Yet-an-other ansible

ansible-playbook -i hosts workstation.yml --tags=show_output  -vvv 

Tags list and definitions:
```
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
```

Tasks lists and summary:


List to TODO:
- Passwords
- Configure users !!
- Install VLC and all codecs
- Install copr 
- Cleanup after packages install
- Filesystem : snapshot root
- Tags cleanup and standardisation
- Steam : add external library
- Steam : icon fix? 
- Allow show_output on every tasks
- roles/flatpak/tasks/main.yml TODO: Install per user repository and application
- roles/packages/task/install_base.yml TODO: Allow installation depending on distribution and distribution family
- roles/packages/task/install_base.yml TODO: COMBINE ALL LISTS TO DO A SINGLE INSTALL !! 
- roles/packages/tasks/cleanup.yml TODO: Remove cache and remove unwanted packages
- roles/packages/vars/main.yml TODO: combine into a single package list to install
- roles/packages/vars/main.yml TODO: missing packages workstation.yml
- Write a logfile


List of FIXME:
- roles/flatpak/tasks/main.yml FIXME: Upgrade fail with error when run as root "Failed to download missing issuer certificate from Authority"
- Install steam flatpak as --user under the desired users

Notes to self :

Network :

Try guessing main IP of target host : 
> ansible_default_ipv4.address|default(ansible_all_ipv4_addresses[0])


> hostvars[inventory_hostname]['ansible_default_ipv4']['address']


Run scripts and only once
https://blog.programster.org/ansible-run-a-local-script-on-remote-server


Check if need restarting Fedora:
https://www.thegeekdiary.com/how-to-check-if-a-service-restart-or-server-reboot-is-required-after-rpm-package-update-centos-rhel-fedora/
