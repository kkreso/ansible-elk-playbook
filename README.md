Forked and based on https://github.com/DanielBerman/ansible-elk-playbook

# Ansible ELK Playbook
 
This playbook is for setting up version 6.x of the ELK Stack on a remote Debian server. 

## Notes and requirements

 - The playbook was built and tested on Debian 9 VMs, for ELK versions 6.x 
 - You will need Ansible installed and running
 - Playbook is currently configured to set up the ELK stack together with Metricbeat for server perf monitoring. There is a role for Filebeat as well. You just need to add the Filebeat role to your [site.yml] file.
 
 ## Instructions
 
 1. Edit your Ansible hosts file ('/etc/ansible/hosts') and add an 'elkservers' entry for the server you wish to install ELK on. You can of course name the host any way you want, this is just an example. 
 2. Verify connectivity to the ELK server.
 3. In the terminal on the machine hosting Ansible, clone this repo.
 4. Cd into the directory, and run:
 `ansible-playbook site.yml`
 
 The plays in the playbook will run on the target server, installing ELK and the specified beats shippers. 
 