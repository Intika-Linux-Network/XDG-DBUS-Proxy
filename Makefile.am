include $(top_srcdir)/build-aux/glib-tap.mk

AM_CFLAGS = \
	$(GLIB_CFLAGS) \
	$(CODE_COVERAGE_CFLAGS) \
	$(NULL)
COMMON_LIBS = \
	$(CODE_COVERAGE_LIBS) \
	$(GLIB_LIBS) \
	$(NULL)

bin_PROGRAMS=xdg-dbus-proxy

xdg_dbus_proxy_SOURCES = \
	flatpak-proxy.c	\
	flatpak-proxy.h	\
	dbus-proxy.c	\
	backport-autoptr.h \
	$(NULL)
xdg_dbus_proxy_LDADD = $(COMMON_LIBS)

include Makefile-docs.am
include tests/Makefile.am.inc

EXTRA_DIST += build-aux/glib-tap.mk
EXTRA_DIST += build-aux/tap-test

# Add rules for code-coverage testing, as defined by AX_CODE_COVERAGE
@CODE_COVERAGE_RULES@
