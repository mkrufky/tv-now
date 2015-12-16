#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.50])
AC_INIT([TV-NOW], [0.0.3], [brad@nextdimension.cc])

AM_INIT_AUTOMAKE([subdir-objects])

AC_CONFIG_SRCDIR([MicroMediaServer.h])
AC_CONFIG_HEADERS([config.h])

# Checks for programs.
AC_PROG_CXX
AC_PROG_AWK
AC_PROG_CC
AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AC_PROG_RANLIB

# libtool...
LT_INIT
AC_CONFIG_MACRO_DIR([m4])

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lIWeb':
AC_CHECK_LIB([IWeb], [main])
# FIXME: Replace `main' with a function in `-lcurl':
AC_CHECK_LIB([curl], [main])
# FIXME: Replace `main' with a function in `-ldvbpsi':
AC_CHECK_LIB([dvbpsi], [main])
# FIXME: Replace `main' with a function in `-ldvbtee':
AC_CHECK_LIB([dvbtee], [main])
# FIXME: Replace `main' with a function in `-ldvbtee_server':
AC_CHECK_LIB([dvbtee_server], [main])
# FIXME: Replace `main' with a function in `-lhdhomerun':
AC_CHECK_LIB([hdhomerun], [main])
# FIXME: Replace `main' with a function in `-ln':
AC_CHECK_LIB([n], [main])

# Checks for header files.
AC_CHECK_HEADERS([arpa/inet.h fcntl.h inttypes.h malloc.h memory.h netdb.h netinet/in.h stddef.h stdint.h stdlib.h string.h sys/ioctl.h sys/socket.h sys/time.h unistd.h wchar.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_PID_T
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_FSEEKO
AC_FUNC_MALLOC
AC_FUNC_MKTIME
AC_FUNC_REALLOC
AC_CHECK_FUNCS([gethostname gettimeofday inet_ntoa localtime_r memset pow select socket strcasecmp strdup strncasecmp strstr strtol strtoul])

AC_CONFIG_FILES([Makefile
                 build/Makefile
                 build/libIWeb/Makefile])

AC_CONFIG_SUBDIRS([libdvbtee])
AC_OUTPUT
