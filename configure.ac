# Initialize Autoconf
AC_PREREQ([2.60])
AC_INIT([xlocale-config], [0.0.0],
        [https://bugs.freedesktop.org/enter_bug.cgi?product=xorg], [xlocale-config])
AC_CONFIG_SRCDIR([Makefile.am])
AC_CONFIG_MACRO_DIR([m4])
AC_CANONICAL_HOST

# Initialize Automake
AM_INIT_AUTOMAKE([foreign dist-bzip2])

m4_ifndef([XORG_MACROS_VERSION],
          [m4_fatal([must install xorg-macros 1.15 or later before running autoconf/autogen])])
XORG_MACROS_VERSION(1.15)
XORG_RELEASE_VERSION
XORG_CHANGELOG
XORG_INSTALL
XORG_PROG_RAWCPP
XORG_WITH_PERL

# arch specific things
WCHAR32="1"
case $host_os in
  os2*) WCHAR32="0" ;;
  *) ;;
esac
AC_SUBST(WCHAR32)

X11_DATADIR="${datadir}/X11"
AX_DEFINE_DIR(X11_DATADIR, X11_DATADIR, [Location of X11 data])
AC_SUBST(X11_DATADIR)

X11_LOCALEDATADIR="${X11_DATADIR}/locale"
AX_DEFINE_DIR(XLOCALEDATADIR, X11_LOCALEDATADIR, [Location of X11 locale data])
AC_SUBST(X11_LOCALEDATADIR)

locales="\
 am_ET.UTF-8  armscii-8   C           cs_CZ.UTF-8  el_GR.UTF-8  en_US.UTF-8 \
 fi_FI.UTF-8  georgian-academy        georgian-ps  ibm-cp1133   iscii-dev \
 isiri-3342   iso8859-1   iso8859-10  iso8859-11   iso8859-13   iso8859-14 \
 iso8859-15   iso8859-2   iso8859-3   iso8859-4    iso8859-5    iso8859-6 \
 iso8859-7    iso8859-8   iso8859-9   iso8859-9e   ja           ja.JIS \
 ja_JP.UTF-8  ja.SJIS     km_KH.UTF-8 ko           koi8-c       koi8-r \
 koi8-u       ko_KR.UTF-8 microsoft-cp1251         microsoft-cp1255 \
 microsoft-cp1256         mulelao-1   nokhchi-1    pt_BR.UTF-8  ru_RU.UTF-8 \
 sr_CS.UTF-8  tatar-cyr   th_TH       th_TH.UTF-8  tscii-0      vi_VN.tcvn \
 vi_VN.viscii zh_CN       zh_CN.gb18030            zh_CN.gbk    zh_CN.UTF-8 \
 zh_HK.big5   zh_HK.big5hkscs         zh_HK.UTF-8  zh_TW        zh_TW.big5 \
 zh_TW.UTF-8"
AC_SUBST(locales)

AC_CONFIG_FILES([Makefile
		nls/Makefile])
AC_OUTPUT
