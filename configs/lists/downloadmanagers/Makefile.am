MAINTAINERCLEANFILES = Makefile.in

DGDATADIR = $(DGCONFDIR)/lists/downloadmanagers

SUBDIRS = .

WLISTS = managedmimetypelist managedextensionlist

EXTRA_DIST = $(WLISTS)

install-data-local: 
	$(mkinstalldirs) $(DESTDIR)$(DGDATADIR) && \
	for l in $(WLISTS) ; do \
		echo "$(INSTALL_DATA) $$l $(DESTDIR)$(DGDATADIR)/$$l"; \
		$(INSTALL_DATA) $$l $(DESTDIR)$(DGDATADIR)/$$l; \
	done


uninstall-local:
	for l in $(WLISTS) ; do \
		rm -f $(DESTDIR)$(DGDATADIR)/$$l ; \
	done
