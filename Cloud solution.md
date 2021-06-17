# Phase 2 - Cloud solution for Ansible & Vagrant on Google Cloud

![Image diagram](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/Cloud%20images/cloud.png)

I may use: 
- Datadog,cloud monitoring as a service
- A Bastion host (A strengthened computer) [Article](https://annaken.github.io/building-a-secure-bastion/)

Installing the Google cloud SDK into my Ubuntu OS I created a GCP project ![Project Creation](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/Cloud%20images/project-create.png)

## Creating a GCP Project

![Project-Creation](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/Cloud%20images/project-create.png)

### Project list

└──╼ $ gloud projects list

![project-list](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/Cloud%20images/project-list.png)

## Create 2 VM instaces on GCP

![VM instances](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/Cloud%20images/vm-instances.png)


## Configure both of them using Ansible

![Vagrant file](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/Cloud%20images/vagrant-file.png)

## SSH into Instances

Problems can arise when you try to SSH into the ubuntu instances,make the below changes

└──╼ $ sudo nano /etc/ssh/sshd_config
PermitRootLogin prohibit-password to PermitRootLogin yes 
PasswordAuthentication no to PasswordAuthentication yes

└──╼ $ sudo service ssh restart

### Also changing the default password can help

└──╼ $ sudo passwd
New password:
Retype new password:
passwd: password updated successfully

![SSH into Instances]()


