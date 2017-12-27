# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.hostname = "elgg"
  config.vm.network :private_network, ip: "192.168.33.34"

  config.vm.synced_folder "./Elgg", "/home/vagrant/Elgg"

  # Ansible provisioner.
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/develop.yml"
    ansible.sudo = true
  end

end
