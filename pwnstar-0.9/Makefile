VER=1

CONFDIR = /var/www

BINPROGS = PwnSTAR_0.9
	
HOTSPOT3 = \
	hotspot_3/facebookLogo.jpg \
	hotspot_3/formdata.txt \
	hotspot_3/GmailLogo.png \
	hotspot_3/GoogleWifi.jpg \
	hotspot_3/HotmailLogo.png \
	hotspot_3/index.html \
	hotspot_3/process-form-data.php \
	hotspot_3/yahoo.gif
	
PHOTSPOT = \
	portal_hotspot/facebookLogo.jpg \
	portal_hotspot/formdata.txt \
	portal_hotspot/GmailLogo.png \
	portal_hotspot/GoogleWifi.jpg \
	portal_hotspot/HotmailLogo.png \
	portal_hotspot/index.html \
	portal_hotspot/yahoo.gif
	
	
PPDF = \
	portal_pdf/aup1.pdf \
	portal_pdf/aup2.pdf \
	portal_pdf/aup2.pdf.alternative \
	portal_pdf/aup_virgin.pdf \
	portal_pdf/index.php \
	portal_pdf/sample_payload.exe
	
PSIMPLE = \
	portal_simple/formdata.txt \
	portal_simple/index.php \
	portal_simple/service.php
	

install:
	
	#install  dirs
	install -dm755 $(DESTDIR)/usr/bin
	install -m755 $(BINPROGS) $(DESTDIR)/usr/bin
	
	install -dm755 $(DESTDIR)$(CONFDIR)
	install -dm755 $(DESTDIR)$(CONFDIR)/hotspot_3
	install -m755 $(HOTSPOT3) $(DESTDIR)$(CONFDIR)/hotspot_3
	
	install -dm755 $(DESTDIR)$(CONFDIR)/portal_hotspot
	install -m755 $(PHOTSPOT) $(DESTDIR)$(CONFDIR)/portal_hotspot
	
	install -dm755 $(DESTDIR)$(CONFDIR)/portal_pdf
	install -m755 $(PPDF) $(DESTDIR)$(CONFDIR)/portal_pdf
	
	install -dm755 $(DESTDIR)$(CONFDIR)/portal_simple
	install -m755 $(PSIMPLE) $(DESTDIR)$(CONFDIR)/portal_simple

	

uninstall:
	for f in $(BINPROGS); do $(RM) $(DESTDIR)/usr/bin/$$f; done
	rm -rf $(DESTDIR)$(CONFDIR)/hotspot_3
	rm -rf $(DESTDIR)$(CONFDIR)/portal_hotspot
	rm -rf $(DESTDIR)$(CONFDIR)/portal_pdf
	rm -rf $(DESTDIR)$(CONFDIR)/portal_simple
	

.PHONY: install uninstall
