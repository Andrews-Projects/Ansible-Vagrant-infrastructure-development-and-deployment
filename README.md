# Ansible & Vagrant infrastructure development and deployment


# Introduction

![Vagrant + Ansible + virtual box](https://github.com/House-Of-Research/Ansible-Vagrant-local-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/Vagrant-Ansible3.png)

## Vagrant 

- This is a great tool for managing local virtual machines to mimic real world infrastructure locally or in the cloud.

## Ansible

- Ansible is an open-source software provisioning, configuration management, and application-deployment tool enabling infrastructure as code.

- It runs on many Unix-like systems, and can configure both Unix-like systems as well as Microsoft Windows.

- Ansible provisions servers managing their configurations & deploying applications either locally or in the cloud.It works by pushing changes
  to all servers(by default)


My plan is to develop this project in 2 phases.

**Phase 1:** Deploying Ansible & Vagrant locally.

**Phase 2:** Deploying Ansible & Vagrant to Google Cloud. -----> [Cloud Solution](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Cloud%20solution.md)

# PHASE 1:

## Tools used:

1. GitKraken - a Git GUI tool.

2. Debian based O.S (Parrot O.S).

3. VMWare Workstation.

4. Ubuntu Server.

## [Initial setup explained here:](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Initial-setup.md)

### Ubuntu server installation

I'm impressed as to the array of tools listed by the ubuntu server including the Google Cloud SDK.

![List of tools](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/tools.png)

### Installation complete

Apparently 2 ubuntu servers can run simultaneously using the same network card but in different windowes,it was a success.

## ![The 2 servers](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/ubuntu_servers.png)

### Here is a simple chart as to how everything has been set up

![chart](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/chart.png)

 
### Create a inventory file

└──╼ $ sudo mkdir /etc/ansible

└──╼ $ sudo touch /etc/ansible/hosts

- The hosts file should contain the server(s) details,In my case:

[servers]

192.168.x.x 

OR (i.e if you dont want to keep typing the SSH password)

192.168.x.x ansible_ssh_pass=xxxx ansible_ssh_user=user

### Running an Ad-Hoc command

└──╼ $ansible all -m ping

![result](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/1stcmd.png)

**See memory usage**

└──╼ $ ansible servers -a "free -m" -u [ubuntu_server_1]

![memory usage](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/memory%20usage.png)

### Other fun ansible commands

└──╼ $ansible all -m setup   ---> Gathering facts.

└──╼ $ ansible abc -m copy -a "src = /etc/yum.conf dest = /tmp/yum.conf" ---> Copying a file

![](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/the_end.jpeg)
