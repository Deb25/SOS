# -*- Makefile -*-
#
# Copyright 2011 Sandia Corporation. Under the terms of Contract
# DE-AC04-94AL85000 with Sandia Corporation, the U.S.  Government
# retains certain rights in this software.
#
# Copyright (c) 2016 Los Alamos National Security, LLC. All rights reserved.
#
# This file is part of the Sandia OpenSHMEM software package. For license
# information, see the LICENSE file in the top level directory of the
# distribution.
#

NPROCS ?= 2
LOG_COMPILER = $(TEST_RUNNER)

AM_CPPFLAGS = -I$(top_srcdir)/mpp
AM_LDFLAGS = $(LIBTOOL_WRAPPER_LDFLAGS)

TESTS = binary-search

check_PROGRAMS = $(TESTS)

if ENABLE_LENGTHY_TESTS
TESTS += gups
else
check_PROGRAMS += gups
endif

gups_SOURCES = gups.c
gups_LDADD = $(top_builddir)/src/libsma.la

binary_search_SOURCES = binary-search.c
binary_search_LDADD = $(top_builddir)/src/libsma.la
