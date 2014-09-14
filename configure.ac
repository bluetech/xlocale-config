# Initialize Autoconf
AC_PREREQ([2.60])
AC_INIT([xlocale-config], [0.0.0],
        [https://bugs.freedesktop.org/enter_bug.cgi?product=xorg], [xlocale-config])
AC_CONFIG_SRCDIR([Makefile.am])

# Initialize Automake
AM_INIT_AUTOMAKE([foreign dist-bzip2])

m4_ifndef([XORG_MACROS_VERSION],
          [m4_fatal([must install xorg-macros 1.15 or later before running autoconf/autogen])])
XORG_MACROS_VERSION(1.15)
XORG_RELEASE_VERSION
XORG_CHANGELOG
XORG_INSTALL

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
