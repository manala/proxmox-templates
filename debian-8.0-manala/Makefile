 BASEDIR:=$(shell dab basedir)

all: info/init_ok
	dab bootstrap --minimal
	dab exec apt-get purge -y isc-dhcp-client isc-dhcp-common
	dab exec apt-get purge -y postfix
	dab exec apt-get purge -y iptables libxtables10
	dab install udev
	dab install systemd systemd-sysv dbus
	dab install python
	sed -i 's/^PermitRootLogin without-password/PermitRootLogin yes/' -i ${BASEDIR}/etc/ssh/sshd_config
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
