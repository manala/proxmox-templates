BASEDIR:=$(shell dab basedir)

all: info/init_ok
	dab bootstrap --minimal
	dab exec apt-get purge -y isc-dhcp-client isc-dhcp-common
	dab exec apt-get purge -y postfix postfix-sqlite
	dab exec apt-get purge -y iptables libxtables12 libnfnetlink0 libiptc0 libip6tc0
	dab install dbus libpam-systemd
	dab install python
	sed -i 's/^#PermitRootLogin prohibit-password/PermitRootLogin yes/' -i ${BASEDIR}/etc/ssh/sshd_config
	dab finalize

info/init_ok: dab.conf
	dab init
	touch $@

.PHONY: clean
clean:
	dab clean
	rm -f *~

.PHONY: dist-clean
dist-clean:
	dab dist-clean
	rm -f *~
