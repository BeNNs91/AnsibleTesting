# AnsibleTesting
Testing of Ansible code for switch deployment

# Prerequisites
1. Ansible
2. sshpass
3. sudo apt install python3-pip


# Configuration
Ensure you have an `ansible.cfg` file in the root directory with the following content:

refrences:
https://developer.arubanetworks.com/hpe-aruba-networking-aoscx/docs/getting-started-with-ansible-and-aos-cx
https://galaxy.ansible.com/ui/repo/published/arubanetworks/aoscx/docs/


Command Notes:
Test API connection : 
curl -k -u admin:P@ssw0rd123 -X GET "https://<switch-ip>/v1/rest/system"
ansible -i hosts.yml all -m ping -vvv




ini
[defaults]
host_key_checking = False

[ssh_connection]
remote_tmp = /tmp/.ansible/tmp


Switch Configuration 
https-server rest access-mode read-write
