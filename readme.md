Vagrant + Cheff + LEMP Stack Environment
========================================

Setup the Local Development Environment (LDE)
---------------------------------------------

This environment makes use of [Vagrant](http://www.vagrantup.com/). Follow the instructions to have the LDE up and running.

These instructions has been tested on a Ubuntu 16.04.5 LTS (Xenial Xerus) 64bit OS.


### 1. Install [VirtualBox](https://www.virtualbox.org)

VirtualBox is an x86 virtualization software package and distributed under either the GNU GPL or a proprietary license with additional features.

Download and install **Virtualbox** and the **Extension Pack** from the [Virtualbox Downloads Page](https://www.virtualbox.org/wiki/Downloads).


### 2. Install Vagrant and plugins

Go to the [download](https://www.vagrantup.com/downloads.html) page, choose the correct package for your OS and install it. This instruction was written with the version [2.1.5].

    wget -c 'https://releases.hashicorp.com/vagrant/2.1.5/vagrant_2.1.5_x86_64.deb'
    sudo dpkg -i vagrant_2.1.5_x86_64.deb

Now install Vagrant plugins
	
	# Berkshelf handle chef cookbooks dependencies
	vagrant plugin install vagrant-berkshelf
	# Keep your VirtualBox Guest Additions up to date
	vagrant plugin install vagrant-vbguest

	
### 3. Start (init) the VM with Vagrant

    vagrant up

	
### 4. Start browsing

Once the VM is loaded, enter on http://192.168.33.199 to check if the services are woking fine. 


Tips for work on this setup
---------------------------

### Update files on the shared folder to start working

The shared folder points to "/var/www/html/" folder, that makes easier to edit 
