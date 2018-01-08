# Proxmox - Templates

## Requirements

  * vagrant 2.0.1+
  * virtualbox 5.2.0+

> Note: The `$` stands for your machine CLI, while the `⇒` stands for the VM CLI

## Build

```
  $ vagrant up
  $ vagrant ssh
  ⇒ cp -a /srv/* /tmp
  ⇒ cd /tmp/debian-[7|8|9].0-manala
  ⇒ sudo make
  ⇒ mv debian-[7|8|9].0-manala_*_amd64.tar.gz /srv/debian-[7|8|9].0-manala/dist/
```
