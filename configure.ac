AC_INIT([Usage],
        [0.0.1],
        [https://github.com/csoriano89/usage/issues/new],
        [usage],
        [https://wiki.gnome.org/Design/Apps/Usage])
AX_IS_RELEASE([git-directory])

AM_INIT_AUTOMAKE([dist-xz no-dist-gzip subdir-objects])
AC_CONFIG_MACRO_DIR([m4])
AM_MAINTAINER_MODE([enable])
m4_ifdef([AM_SILENT_RULES], [AM_SILENT_RULES([yes])])

AM_PATH_PYTHON([3.4])

# GResources
AC_PATH_PROG([GLIB_COMPILE_RESOURCES], [glib-compile-resources])

# Internationalisation
GETTEXT_PACKAGE=usage
AC_SUBST(GETTEXT_PACKAGE)
AC_DEFINE_UNQUOTED([GETTEXT_PACKAGE], ["$GETTEXT_PACKAGE"], [gettext package name])
IT_PROG_INTLTOOL([0.50.2])

# GSettings
AX_REQUIRE_DEFINED([GLIB_GSETTINGS])
GLIB_GSETTINGS

# AppData
AX_REQUIRE_DEFINED([APPSTREAM_XML])
APPSTREAM_XML

AC_CONFIG_FILES([
  VERSION
  Makefile
  data/Makefile
  data/icons/Makefile
  src/Makefile
  po/Makefile.in
])
AC_OUTPUT

