# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

   config.vm.define "fry" do |fry|
    fry.vm.box = "debian/jessie64"
    fry.vm.hostname = "fry.at.futurama"
    fry.vm.network "private_network", ip: "10.0.99.3"
  end

 # config.vm.provision "shell", inline: "apt-get install --yes python-apt"

  config.vm.provision :ansible do |ansible| 
    ansible.playbook ="ansible/provisioning.yml"
  end

#  config.vm.provider "virtualbox" do |v|
#    v.memory = 128
#  end

end
