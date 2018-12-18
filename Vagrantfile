# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos/7"
  config.vm.synced_folder '.', '/vagrant', type: "virtualbox"


  config.vm.define "centos", primary: true do |centos|
    centos.vm.hostname = "centos"
    centos.vm.network "private_network", ip: "10.0.0.2"
    config.vm.provider "virtualbox" do |vb|
      vb.cpus = "1"
      vb.memory = "4096"
    end
  end

end
