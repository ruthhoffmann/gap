## Process this file with automake to generate Makefile.in

# Copyright 2001, 2002 Free Software Foundation, Inc.
#
# This file is part of the GNU MP Library test suite.
#
# The GNU MP Library test suite is free software; you can redistribute it
# and/or modify it under the terms of the GNU General Public License as
# published by the Free Software Foundation; either version 3 of the License,
# or (at your option) any later version.
#
# The GNU MP Library test suite is distributed in the hope that it will be
# useful, but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General
# Public License for more details.
#
# You should have received a copy of the GNU General Public License along with
# the GNU MP Library test suite.  If not, see https://www.gnu.org/licenses/.


AM_CPPFLAGS = -I$(top_srcdir) -I$(top_srcdir)/tests
AM_LDFLAGS = -no-install
LDADD = $(top_builddir)/tests/libtests.la $(top_builddir)/libgmp.la

check_PROGRAMS = t-printf t-scanf t-locale
TESTS = $(check_PROGRAMS)

# Temporary files used by the tests.  Removed automatically if the tests
# pass, but ensure they're cleaned if they fail.
#
CLEANFILES = *.tmp

$(top_builddir)/tests/libtests.la:
	cd $(top_builddir)/tests; $(MAKE) $(AM_MAKEFLAGS) libtests.la
