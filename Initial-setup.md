## This page explains the basic initial setup of Ansible & Vagrant

## Initial setup ---> Ansible

- Ansible's only dependency is Python,On linux this comes by default.

### Ansible installation

$ sudo pip install ansible

### for Ubuntu:

$ sudo apt-add-repository -y ppa:ansible/ansible

$ sudo apt-get update

$ sudo apt-get install -y ansible

### If you're on RHEL/CentOS 6:

$ rpm -ivh http://dl.fedoraproject.org/pub/epel/6/x86_64/\
epel-release-6-8.noarch.rpm

$ yum install epel-release

### Upgrade ansible with:

$ pip install --upgrade ansible

### test installation success with:

$ ansible --version

### Installation successful
![](https://github.com/Andrews-Projects/Ansible-Vagrant-infrastructure-development-and-deployment/blob/main/Images%20%26%20gifs/ansible-install.png)



## Initial setup ---> Vagrant

Vagrant is a server provisioning tool

Download vagrant from their website,depending on your system type [Vagrant](https://www.vagrantup.com/downloads)

- Create a new folder where youll keep your Vagrant file & provisioning instructions 

┌─[andrew@parrot]─[~/Desktop]
└──╼ $mkdir vagrantfile && cd vagrantfile






