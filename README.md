# Proxmox - Templates

## Requirements

  * vagrant 1.8.4+
  * virtualbox 5.0.26+

  * dab 2.0-6+
  * lxc 2.0.4+

> Note: The `$` stands for your machine CLI, while the `⇒` stands for the VM CLI

## Dev

  $ vagrant up
  $ vagrant ssh
  ⇒ sudo su
  ⇒ cd /srv
  ⇒ rm -Rf * && cp -a /vagrant/*/ .
  ⇒ cd debian-[7|8].0-manala
  ⇒ make

## Notes

 * To satisfy requirements, pvetest repository is enabled. See: /etc/apt/sources.list.d/pve-install-repo.list
 * To build virtualbox guest additions, follow https://www.vagrantup.com/docs/virtualbox/boxes.html#virtualbox-guest-additions using "pve-headers" instead of "linux-headers" packages

## Todo

  * Check why the vagrant box is sooooooo big
