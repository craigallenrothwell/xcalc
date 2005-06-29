# 
#  Copyright 2005  Red Hat, Inc.
# 
#  Permission to use, copy, modify, distribute, and sell this software and its
#  documentation for any purpose is hereby granted without fee, provided that
#  the above copyright notice appear in all copies and that both that
#  copyright notice and this permission notice appear in supporting
#  documentation, and that the name of Red Hat not be used in
#  advertising or publicity pertaining to distribution of the software without
#  specific, written prior permission.  Red Hat makes no
#  representations about the suitability of this software for any purpose.  It
#  is provided "as is" without express or implied warranty.
# 
#  RED HAT DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE,
#  INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS, IN NO
#  EVENT SHALL RED HAT BE LIABLE FOR ANY SPECIAL, INDIRECT OR
#  CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE,
#  DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
#  TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR
#  PERFORMANCE OF THIS SOFTWARE.

bin_PROGRAMS = xcalc

xcalc_CFLAGS = $(DEP_CFLAGS)
xcalc_LDADD = $(DEP_LIBS) -lm

xcalc_SOURCES =	\
        actions.c \
        actions.h \
        math.c \
        xcalc.c \
        xcalc.h

dist_man_MANS = \
        xcalc.man

# App default files  (*.ad)

appdefaultdir = $(sysconfdir)/X11/app-defaults


APPDEFAULTFILES = \
        XCalc \
        XCalc-col


$(APPDEFAULTFILES): %: %.ad
	cp $< $@

appdefault_DATA = $(APPDEFAULTFILES)

EXTRA_DIST = $(foreach FILE, $(APPDEFAULTFILES), $(FILE).ad)

CLEANFILES = $(APPDEFAULTFILES)
