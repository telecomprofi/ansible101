# ansible101
Ansible examples for beginners

## First ansible playbok to deploy LAMP stack
* [Link to video](https://www.youtube.com/watch?v=Bl1Iab8B1L8)
* [Link to playbook](https://github.com/telecomprofi/ansible101/blob/main/ansible_LAMP.md)

## Provision AWS EC2 instance with Ansible Playbok keeping secrets secure with Ansible vault
* [Link to article](https://medium.datadriveninvestor.com/devops-using-ansible-to-provision-aws-ec2-instances-3d70a1cb155f)
* [Link to playbook](https://github.com/telecomprofi/ansible101/blob/main/ansible_aws_ec2/ansible_aws_ec2_creation.yml)

## Molecule & Podman for devoloping and testing multi-ditro playbooks
* [Link to page](https://github.com/telecomprofi/ansible101/blob/main/molecule.md)


## update cache & upgrade all packages on CentOS Linux <update.md> <update.yml>
* update systemctl limits on number of file descriptors (ulimit -n) & similiar (CentOS7 tuning)

## Updating system/user limits.conf/ulimit with ansible

### 1. with pam_limits module <systemctl.yml> and (1st variant)


### 2. without it <systemctl2.yml> with reload (2nd variant)
* copy files to remote host

### 3. Ad-hoc ansible cli examples <ad-hoc with ssh key, become, and run comands from specific linux user>

### 4. Ansible playbook to modify ulimit system limits for specific user with pam_limits module - untested (3rd variant) 
* [Link to playbook](https://github.com/telecomprofi/ansible101/blob/main/modify_ulimit%20using%20pam_limits%20module_untested.yml)

Yaml & syntax
![image](https://user-images.githubusercontent.com/17558124/137010020-af5281de-c8d6-47d1-b05a-790b8be6f8e4.png)


simple playbook to install and configure Apache httpd
![image](https://user-images.githubusercontent.com/17558124/137010148-f9bb8aa0-e05a-43f3-acea-e18b10b911fa.png)

Simple set of tasks to install nginx
![image](https://user-images.githubusercontent.com/17558124/137010276-8e3d64a5-f9b4-43a4-9238-fadc96e5c411.png)




### 5.  Ansible playbook example of changing Linux system/user limits with pam_limits 
* [Link to article](https://github.com/telecomprofi/ansible101/blob/main/limits.conf%20with%20Ansible.md)




### Ansible galaxy collections
![image](https://user-images.githubusercontent.com/17558124/137009849-e51a06df-2eb1-47ee-8148-731cf3d0fb85.png)


  
### TBA jinja j2 templates in Ansible config management & overriding config settings/vars


### TBA AWX aka Ansible Tower

### TBA how to pair Ansible & Terraform

### Ansible & safe secret management 


