# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.guest = 'debian'
  config.vm.box   = 'manala/proxmox-dev-debian'

  # Provider
  config.vm.provider :virtualbox do |virtualbox|
    virtualbox.customize ['modifyvm', :id, '--nicpromisc2', 'allow-vms']
  end
end
