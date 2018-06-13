# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|

  # Ssh
  config.ssh.forward_agent = true

  # Vm
  config.vm.box      = 'manala/dab'
  config.vm.hostname = 'packer.templates'
  config.vm.network    'private_network', type: 'dhcp'

  config.vm.synced_folder '.', '/srv'

end
