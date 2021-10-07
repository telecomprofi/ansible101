# ansible101
Ansible examples for beginners
# First ansible playbok to deploy LAMP stack
* [Link to video](https://www.youtube.com/watch?v=Bl1Iab8B1L8)
* [Link to playbook](https://github.com/telecomprofi/ansible101/blob/main/ansible_LAMP.md)

### Provision AWS EC2 instance with Ansible Playbok keeping secrets secure with Ansible vault
* [Link to article](https://medium.datadriveninvestor.com/devops-using-ansible-to-provision-aws-ec2-instances-3d70a1cb155f)
* [Link to playbook](tba)
* 
#### update cache & upgrade all packages on CentOS Linux <update.md> <update.yml>
* update systemctl limits on number of file descriptors (ulimit -n) & similiar (CentOS7 tuning)

### Updating system/user limits.conf/ulimit with ansible

#### 1. with pam_limits module <systemctl.yml> and (1st variant)


### 2. without it <systemctl2.yml> with reload (2nd variant)
* copy files to remote host

#### 3. Ad-hoc ansible cli examples <ad-hoc with ssh key, become, and run comands from specific linux user>

#### 4. Ansible playbook to modify ulimit system limits for specific user with pam_limits module - untested (3rd variant) 
* [Link to playbook](https://github.com/telecomprofi/ansible101/blob/main/modify_ulimit%20using%20pam_limits%20module_untested.yml)


#### 5.  Ansible playbook example of changing Linux system/user limits with pam_limits 
* [Link to article](https://github.com/telecomprofi/ansible101/blob/main/limits.conf%20with%20Ansible.md)

  


