AM_CFLAGS  = -Os -Wall -D_POSIX -D_DEBUG -D_VERBOSE -pthread

noinst_LTLIBRARIES = libIWeb.la

AM_CFLAGS += -I../../libIWeb

libIWeb_la_SOURCES = \
  ../../libIWeb/ILibParsers.c \
  ../../libIWeb/ILibAsyncSocket.c \
  ../../libIWeb/ILibAsyncServerSocket.c \
  ../../libIWeb/ILibWebClient.c \
  ../../libIWeb/ILibWebServer.c
