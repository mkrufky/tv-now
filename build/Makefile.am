AM_CXXFLAGS  = -I../libdvbtee/usr/include -I../libdvbtee/libdvbtee -I../libdvbtee/libdvbtee_server
AM_CFLAGS    = -I../libdvbtee/usr/include -I../libdvbtee/libdvbtee -I../libdvbtee/libdvbtee_server
AM_CXXFLAGS += -D_POSIX -D_GNU_SOURCE -D__USE_LARGEFILE64 -D__STDC_FORMAT_MACROS -D_FILE_OFFSET_BITS=64
AM_CFLAGS   += -D_POSIX -D_GNU_SOURCE -D__USE_LARGEFILE64 -D__STDC_FORMAT_MACROS -D_FILE_OFFSET_BITS=64

AM_CFLAGS   += -O2 -Wall -pthread -I./libIWeb
AM_CXXFLAGS += -Wno-deprecated -Wno-deprecated-declarations -pthread -fPIC

AM_CXXFLAGS += -D_DEBUG -D_VERBOSE -g -ggdb
AM_CFLAGS   += -D_DEBUG -D_VERBOSE -g -ggdb
# Compiler flags applied to all files
# Optional flags: -D_VERBOSE -D_DEBUG -DSPAWN_BROWSE_THREAD -D_TEMPDEBUG
# -g puts debug symbols
# -DSPAWN_BROWSE_THREAD makes it so each browse thread spawns a thread (recommended only if browse request takes a long time)
#

bin_PROGRAMS = tv-now

AM_CXXFLAGS += -I.. -I../libIWeb
AM_CFLAGS   += -I.. -I../libIWeb

tv_now_SOURCES = \
  ../CdsMediaClass.c \
  ../CdsMediaObject.c \
  ../CdsObjectToDidl.c \
  ../MicroMediaServer.c \
  ../UpnpMicroStack.c \
  ../MyString.c \
  ../MimeTypes.c \
  ../PortingFunctions.c \
  ../tv-now.c

tv_now_LDADD = -L../libdvbtee/usr/lib -ldvbtee -ldvbtee_server -ldvbpsi -lstdc++

#DVBTEE_LIBS_STATIC = ./libdvbtee/usr/lib/libdvbtee.a ./libdvbtee/usr/lib/libdvbtee_server.a ./libdvbtee/usr/lib/libdvbpsi.a -lstdc++

tv_now_SOURCES += ../dvbteeserver.cpp

tv_now_LDADD += -L./libIWeb -lIWeb
