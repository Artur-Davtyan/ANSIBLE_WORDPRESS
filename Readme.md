## SETUP WORDPRESS WITH ANSIBLE
### Description:
In this project we will setup WordPress using Docker containers on the target hosts. We will use Ansible to automate docker installation and WordPress setup process. For that we will use Ansible's models that related to docker images and docker container management. (For more information about Ansible  go to [link](https://docs.ansible.com/) )

### Pre requirepmants:
1. pre installed  Ansible
2. Target host(s) 
   >* You need to create user for Ansible(in our project we use usernam **"ansible"**) 
   >* give privileges to that user to run commansd with "_sudo_" without password 
   >* setup ssh connection useing ssh keys

### Usage:
* Inside working directory
  * Fill the information about target host inside "**_host_**" file
  * chenge the valuses of variables  inseide "**_./group_vars/all_**" file(if you want to use anouther values for that arguments)
  * Run ansible vith docker_wordpress.yml playbook  
```
   #  ansible-playbook -i hosts docker_worpress.yml 
```