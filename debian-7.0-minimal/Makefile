BASEDIR:=$(shell dab basedir)

all: info/init_ok 
	dab bootstrap --minimal
	dab install salt-minion
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
