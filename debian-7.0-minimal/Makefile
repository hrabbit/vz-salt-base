BASEDIR:=$(shell dab basedir)

all: info/init_ok 
	dab bootstrap --minimal
	dab install salt-minion
	@if [[ -n "$(SALT-MASTER)" ]]; then \
		echo "Setting master: $(SALT-MASTER)"; \
		mkdir -p ${BASEDIR}/etc/salt/minion.d; \
		echo "master: $(SALT-MASTER)" > ${BASEDIR}/etc/salt/minion.d/local.conf; \
	fi;

	echo "" >> ${BASEDIR}/etc/network/interfaces
	echo "auto eth0" >> ${BASEDIR}/etc/network/interfaces
	echo "iface eth0 inet dhcp" >> ${BASEDIR}/etc/network/interfaces
	dab finalize

info/init_ok: dab.conf
	dab init
	touch $@

clean:
	dab clean
	rm -f *~

dist-clean:
	dab dist-clean
	rm -f *~
