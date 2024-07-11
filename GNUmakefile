.POSIX:
.SUFFIXES:
.PHONY: all clean install check
all:
PROJECT=make-scripts
VERSION=1.0.0
PREFIX=/usr/local

all:
clean:
install:
check:
## -- BLOCK:license --
install: install-license
install-license: 
	mkdir -p $(DESTDIR)$(PREFIX)/share/doc/$(PROJECT)
	cp LICENSE $(DESTDIR)$(PREFIX)/share/doc/$(PROJECT)
## -- BLOCK:license --
## -- BLOCK:sh --
install: install-sh
install-sh:
	mkdir -p $(DESTDIR)$(PREFIX)/bin
	cp bin/systemd-h        $(DESTDIR)$(PREFIX)/bin
	cp bin/runit-h          $(DESTDIR)$(PREFIX)/bin
	cp bin/make-h           $(DESTDIR)$(PREFIX)/bin
	cp bin/copy-script      $(DESTDIR)$(PREFIX)/bin
	cp bin/script-h         $(DESTDIR)$(PREFIX)/bin
## -- BLOCK:sh --
