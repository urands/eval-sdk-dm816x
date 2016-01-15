#$L$
# Copyright (C) 2011 Ridgerun (http://www.ridgerun.com). 
##$L$

include ../../../bsp/classes/rrsdk.defs
include $(CLASSES)/autotools.class

PKG_URL=http://ftp.gnu.org/pub/gnu/gettext/
PKG_TARBALL=gettext-0.19.7.tar.gz
PKG_SHA1SUM=4b2574b76d14c98270bf607a2a62f033524d8e8c

AUTOTOOLS_PARAMS=--disable-openmp --disable-java --disable-native-java --without-emacs

ifneq ($(CONFIG_FS_APPS_GETTEXT_NLS),y)
    AUTOTOOLS_PARAMS=--disable-nls
endif

LIBRARIES_OPTIONAL= /usr/lib/libasprintf.so.0.0.0 
	    

LIBRARIES=  /usr/lib/libgettextlib-0.19.7.so
