ACLOCAL_AMFLAGS = -I m4

if OS_WINDOWS_CROSSCOMPILE
# for leveldb
AM_MAKEFLAGS = TARGET_OS=OS_WINDOWS_CROSSCOMPILE
endif

export CC CXX AR LD
SUBDIRS = tor db4.8/build_unix leveldb src

Spectre.app: all-am
	mkdir -p Spectre.app/Contents/{MacOS,Resources}
	cp Info.plist Spectre.app/Contents
	cp spectre.icns Spectre.app/Contents/Resources
	cp src/spectre Spectre.app/Contents/MacOS/Spectre
	echo "APPL????" > Spectre.app/Contents/PkgInfo
	@MACDEPLOYQT@ Spectre.app @MACDEPLOYQT_LIBPATH@ 

.PHONY: Spectre.app
