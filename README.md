# ansible101
Ansible examples for beginners

* Provision EC2 instance with Ansible Playbok keeping secrets secure with Ansible vault <https://medium.datadriveninvestor.com/devops-using-ansible-to-provision-aws-ec2-instances-3d70a1cb155f>
* update cache & upgrade all packages on CentOS Linux <update.md> <update.yml>
* update systemctl limits on number of file descriptors (ulimit -n) & similiar (CentOS7 tuning)
1. with pam_limits module <systemctl.yml> and (1st variant)
2. without it <systemctl2.yml> with reload (2nd variant)
* copy files to remote host
* Ad-hoc examples <ad-hoc with ssh key, become, and run comands from specific linux user>
* Ansible playbook to modify ulimit system limits for specific user with pam_limits module - untested (3rd variant) <https://github.com/telecomprofi/ansible101/blob/main/modify_ulimit%20using%20pam_limits%20module_untested.yml>

