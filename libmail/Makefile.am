#
# Copyright 2002-2009, Double Precision Inc.
#
# See COPYING for distribution information.
#

CONFIG_STATUS_DEPENDENCIES=../tcpd/couriertls.config

noinst_LTLIBRARIES=libmail.la
noinst_PROGRAMS=mailtool testsuite

AM_CFLAGS = $(LIBIDN_CFLAGS)

libmail_la_SOURCES=misc.H mail.H mail.C \
			addmessage.C addmessage.H \
			addmessageimport.C \
			addmessageremoveattachments.C \
			addressbook.H addressbook.C \
			addressbookadd.H addressbookadd.C \
			addressbookget.H addressbookget.C \
			addressbookopen.H addressbookopen.C \
			addressbooksearch.H addressbooksearch.C \
			attachments.C attachments.H \
			autodecoder.C autodecoder.H \
			envelope.C envelope.H \
			base64.C base64.H \
			copymessage.C copymessage.H \
			decoder.C decoder.H \
			driver.C driver.H \
			expungelist.C expungelist.H \
			fd.C fd.H \
			fdtls.C fdtls.H \
			file.C file.H \
			generic.C generic.H \
			genericdecode.C genericdecode.H \
			headers.C headers.H \
			imap.C imap.H \
			imapacl.C imapacl.H \
			imapidle.C imapidle.H \
			imaplogin.C imaplogin.H \
			imaplogout.C \
			imapfetchhandler.C imapfetchhandler.H \
			imaphandler.C imaphandler.H \
			imaphmac.C imaphmac.H \
			imapfolder.C imapfolder.H \
			imapfolders.C imapfolders.H \
			imaplisthandler.C imaplisthandler.H \
			imapparsefmt.C imapparsefmt.H \
			imapstatushandler.C imapstatushandler.H \
			logininfo.C logininfo.H \
			maildir.C maildir.H \
			maildiradd.C maildiradd.H \
			maildirfolder.C maildirfolder.H \
			mbox.C mbox.H \
			mboxadd.C mboxadd.H \
			mboxexpunge.C mboxexpunge.H \
			mboxfolder.C \
			mboxgetmessage.C mboxgetmessage.H \
			mboxlock.C mboxlock.H \
			mboxmagictag.C mboxmagictag.H \
			mboxmultilock.C mboxmultilock.H \
			mboxopen.C mboxopen.H \
			mboxread.C mboxread.H \
			mboxsighandler.C mboxsighandler.H \
			mimetypes.C mimetypes.H \
			namespace.H \
			nntp.C nntp.H \
			nntpadd.C nntpadd.H \
			nntpcache.C nntpcache.H \
			nntpchecknew.C nntpchecknew.H \
			nntpfetch.C nntpfetch.H \
			nntpfolder.C nntpfolder.H \
			nntpgroup.C nntpgroup.H \
			nntpgroupinfo.C nntpgroupinfo.H \
			nntpgroupopen.C nntpgroupopen.H \
			nntplistactive.C nntplistactive.H \
			nntplogin.C nntplogin.H \
			nntplogin2.C nntplogin2.H \
			nntplogout.C nntplogout.H \
			nntpnewsrc.C nntpnewsrc.H \
			nntppost.C nntppost.H \
			nntpxover.C nntpxover.H \
			nntpxpat.C nntpxpat.H \
			objectmonitor.C objectmonitor.H \
			poll.C \
			pop3.C pop3.H \
			pop3folder.C \
			pop3maildrop.C pop3maildrop.H \
			qp.C qp.H \
			rfc2047decode.C rfc2047decode.H \
			rfc2047encode.C rfc2047encode.H \
			rfcaddr.C rfcaddr.H \
			runlater.C runlater.H \
			search.C search.H \
			smap.C smap.H \
			smapacl.C smapacl.H \
			smapadd.C smapadd.H \
			smapaddmessage.C smapaddmessage.H \
			smapcopy.C smapcopy.H \
			smapcreate.C smapcreate.H \
			smapdelete.C smapdelete.H \
			smapfetch.C smapfetch.H \
			smapfetchattr.C smapfetchattr.H \
			smapidle.C smapidle.H \
			smaplist.C smaplist.H \
			smapmsgrange.C smapmsgrange.H \
			smapnewmail.C smapnewmail.H \
			smapnoopexpunge.C smapnoopexpunge.H \
			smapopen.C smapopen.H \
			smapsearch.C smapsearch.H \
			smapsendfolder.C smapsendfolder.H \
			smapstatus.C smapstatus.H \
			smapstore.C smapstore.H \
			smtp.C smtp.H \
			smtpfolder.H smtpfolder.C \
			smtpinfo.H \
			snapshot.C snapshot.H \
			sortfolders.C \
			structure.C structure.H \
			sync.C sync.H \
			tmpaccount.C tmpaccount.H \
			tmpaccountadd.C tmpaccountfolder.C
libmail_la_LIBADD = $(LIBIDN_LIBS)

mailtool_SOURCES=mailtool.C
mailtool_DEPENDENCIES=libmail.la \
	../rfc2045/librfc2045.la \
	../rfc822/librfc822.la ../rfc822/libencode.la \
	../maildir/libmaildir.la \
	@LIBCOURIERTLS@ \
	../liblock/liblock.la ../unicode/libunicode.la \
	../libhmac/libhmac.la ../md5/libmd5.la ../sha1/libsha1.la \
	../numlib/libnumlib.la ../tcpd/libspipe.la ../soxwrap/libsoxwrap.a \
	../soxwrap/soxlibs.dep

mailtool_LDADD=libmail.la ../rfc2045/librfc2045.la \
	../rfc822/librfc822.la ../rfc822/libencode.la \
	../maildir/libmaildir.la \
	@LIBCOURIERTLS@ \
	../liblock/liblock.la ../unicode/libunicode.la \
	../libhmac/libhmac.la ../md5/libmd5.la ../sha1/libsha1.la \
	../numlib/libnumlib.la ../tcpd/libspipe.la ../soxwrap/libsoxwrap.a \
	`cat ../maildir/maildir.libdeps ../soxwrap/soxlibs.dep`
mailtool_LDFLAGS=-static

testsuite_SOURCES=testsuite.C
testsuite_DEPENDENCIES=$(mailtool_DEPENDENCIES)
testsuite_LDADD=$(mailtool_LDADD)
testsuite_LDFLAGS=-static

EXTRA_DIST=autodeps.C testsuite.txt

check-am:
	./testsuite | cmp -s - $(srcdir)/testsuite.txt

install-data-hook: @INSTINCLUDES@

uninstall-local: @UNINSTINCLUDES@

install-includes:
	set -x ; \
	source=autodeps.C object=autodeps.o libtool=no \
	depfile=autodeps.P tmpdepfile=autodeps.tP \
	$(CXXDEPMODE) $(depcomp) \
	$(CXXCOMPILE) -c -o autodeps.o `test -f 'autodeps.C' || echo '$(srcdir)/'`autodeps.C
	rm -f autodeps.o
	$(mkinstalldirs) $(DESTDIR)$(includedir)/libmail
	for f in `sed 's/.*://' <autodeps.P | tr -d '\\\\' | tr ' ' '\\012' | sed '/^\//d;/autodeps.C/d' | sort | uniq` ; do \
	    $(INSTALL_DATA) $$f $(DESTDIR)$(includedir)/libmail ; case $$f in \
		*/*) \
			n=`echo $$f | sed 's:.*/::'` ; \
			f=`echo $$f | sed 's:/[^/]*$$::'` ;\
			f=`echo $$f | sed 's:.*/::'` ;\
			$(mkinstalldirs) $(DESTDIR)$(includedir)/libmail/$$f ;\
			mv -f $(DESTDIR)$(includedir)/libmail/$$n $(DESTDIR)$(includedir)/libmail/$$f ;\
			;; \
		esac ; done
	rm -f autodeps.P

uninstall-includes:
	rm -rf $(DESTDIR)$(includedir)/libmail

BUILT_SOURCES=libcouriertls.h
DISTCLEANFILES=libcouriertls.h mimetypefiles.h

libcouriertls.h: ../tcpd/couriertls.config
	cp /dev/null libcouriertls.h ; . ../tcpd/couriertls.config ; \
		test "$$couriertls" != "" || exit 0 ; \
		echo '#define HAVE_LIBCOURIERTLS 1' >libcouriertls.h
