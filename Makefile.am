cfgdir		 = $(datadir)/vyatta-cfg/templates
share_perl5dir   = $(datarootdir)/perl5/Vyatta

sbin_SCRIPTS = scripts/system/upnp-interface-config.pl

curverdir = $(sysconfdir)/config-migrate/current
curver_DATA = cfg-version/upnp@0

share_perl5_DATA  = lib/Vyatta/Upnp.pm

cpiop = find  . ! -regex '\(.*~\|.*\.bak\|.*\.swp\|.*\#.*\#\)' -print0 | cpio -0pd

install-exec-hook:
	mkdir -p $(DESTDIR)$(cfgdir)
	cd templates; $(cpiop) $(DESTDIR)$(cfgdir)
