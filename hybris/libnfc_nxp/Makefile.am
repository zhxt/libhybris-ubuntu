lib_LTLIBRARIES = \
	libnfc_nxp.la

libnfc_nxp_la_SOURCES = libnfc_nxp.c
libnfc_nxp_la_CFLAGS = \
	-I$(top_srcdir)/include \
	$(ANDROID_HEADERS_CFLAGS) \
	-Wno-error=unused-function

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libnfc_nxp.pc

if WANT_TRACE
libnfc_nxp_la_CFLAGS += -DDEBUG
endif

if WANT_DEBUG
libnfc_nxp_la_CFLAGS += -ggdb -O0
endif

libnfc_nxp_la_LDFLAGS = \
	$(top_builddir)/common/libhybris-common.la \
	-version-info "1":"0":"0"
