# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "cbednarski/ubuntu-1604"

  config.vm.boot_timeout = 600

  config.vm.hostname = "elgg"
  config.vm.network :private_network, ip: "192.168.33.34"

  config.vm.synced_folder ".", "/home/vagrant/"

  config.vm.provision :shell, path: "provisioning/provision.sh"

end
