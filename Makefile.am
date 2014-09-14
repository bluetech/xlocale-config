SUBDIRS=nls specs

ACLOCAL_AMFLAGS = -I m4

pkgconfigdir = $(datadir)/pkgconfig
pkgconfig_DATA = xlocale-config.pc

MAINTAINERCLEANFILES = ChangeLog INSTALL

.PHONY: ChangeLog INSTALL

INSTALL:
	$(INSTALL_CMD)

ChangeLog:
	$(CHANGELOG_CMD)

dist-hook: ChangeLog INSTALL
