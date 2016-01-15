#$L$
# Copyright (C) 2011 Ridgerun (http://www.ridgerun.com). 
##$L$
PKG_URL=http://ftp.gnu.org/pub/gnu/ncurses/
PKG_TARBALL=ncurses-6.0.tar.gz
PKG_SHA1SUM=acd606135a5124905da770803c05f1f20dd3b21c

# We need to use prefix=/usr to avoid ncurses from looking for terminfos in the build dir
AUTOTOOLS_PARAMS=--with-shared --prefix=/usr --with-abi-version=5
DESTDIR=$(FSDEVROOT)

LIBRARIES=  /usr/lib/{libncurses.so.5.9,libform.so.5.9,libmenu.so.5.9,libpanel.so.5.9}
OTHERS= /usr/share/terminfo/v/vt100 \
	/usr/share/terminfo/v/vt102

include ../../../bsp/classes/rrsdk.class
include $(CLASSES)/autotools.class

# Extra install steps, need to be defined after including autotools.class
# to have the right order
install::
	$(V)sed -i 's?prefix="/usr"?prefix="$(FSDEVROOT)/usr"?' $(FSDEVROOT)/usr/bin/ncurses5-config
	$(V) cp $(FSDEVROOT)/usr/bin/ncurses5-config $(LOCALDIR)/bin
