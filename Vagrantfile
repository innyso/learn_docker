# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  
	config.vm.provider :virtualbox do |vb,override|
		config.vm.hostname="docker-vagrant"
		config.vm.box = "ubuntu/trusty64"
    config.vm.network "private_network", ip: "192.168.50.4"
  end
  
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
