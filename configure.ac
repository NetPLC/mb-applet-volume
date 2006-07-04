AC_PREREQ(2.53)
AC_INIT([mb-applet-volume], 0.2, [mallum@handhelds.org])
AC_CONFIG_SRCDIR([volume-applet.c])

AM_INIT_AUTOMAKE()
AM_MAINTAINER_MODE
AM_CONFIG_HEADER(config.h)

# Checks for programs.
AC_PROG_CC

PKG_CHECK_MODULES(APPLET, [gtk+-2.0 libmb])

if test "x$GCC" = "xyes"; then
        GCC_WARNINGS="-Wall -fno-strict-aliasing"
        XLIBS_CFLAGS="$GCC_WARNINGS"
fi

AC_SUBST(APPLET_CFLAGS)
AC_SUBST(APPLET_LIBS)

# Checks for header files.

AC_HEADER_STDC

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_TYPE_PID_T

MIXER_LIBS=""
P_MIXER=""
AC_CHECK_HEADERS(linux/soundcard.h, [ P_MIXER=yes ], [
AC_CHECK_HEADERS(soundcard.h, [MIXER_LIBS="-lossaudio"], [ P_MIXER=no ]) ] )
if test "$P_MIXER" != "yes"; then
  AC_MSG_ERROR([Could not find suitable Soundcard libs.])
fi

AC_SUBST(MIXER_LIBS)

# Checks for library functions.
 
AC_OUTPUT([Makefile])
