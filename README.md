# Proxmox - Templates

## Requirements

  * vagrant 2.0.1+
  * virtualbox 5.2.0+

> Note: The `$` stands for your machine CLI, while the `⇒` stands for the VM CLI

## Build

```
  $ vagrant up
  $ vagrant ssh
  ⇒ cp -a /srv/templates /tmp
  ⇒ cd /tmp/templates/debian-[7|8|9].0-manala
  ⇒ sudo make
```
