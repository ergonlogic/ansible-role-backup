# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.hostname = 'restic.local'
  config.vm.network 'private_network', ip: '10.55.55.56'

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 2
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.provisioning_path = "/vagrant/tests"
    ansible.playbook = "playbook.yml"
    ansible.inventory_path = "inventory"
    ansible.limit = "all"
  end

end
