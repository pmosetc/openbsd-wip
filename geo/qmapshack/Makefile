# $OpenBSD: Makefile.template,v 1.73 2016/01/11 09:17:22 sthen Exp $

COMMENT =	map management tool

GH_ACCOUNT = 	Maproom
GH_PROJECT = 	qmapshack
GH_TAGNAME = 	V_1.14.1

CATEGORIES =	geo

HOMEPAGE =	https://github.com/Maproom/qmapshack/wiki

#MAINTAINER =	

# GPLv3
PERMIT_PACKAGE =	Yes

WANTLIB += ${COMPILER_LIBCXX} GL Qt5Core Qt5DBus Qt5Gui Qt5Help
WANTLIB += Qt5Network Qt5Positioning Qt5PrintSupport Qt5Qml Qt5Quick
WANTLIB += Qt5Sql Qt5WebChannel Qt5WebEngineCore Qt5WebEngineWidgets
WANTLIB += Qt5Widgets Qt5Xml c gdal jpeg m proj quazip5 routino

MODULES =		devel/cmake x11/qt5

RUN_DEPENDS =		devel/desktop-file-utils \
			x11/gtk+3,-guic
LIB_DEPENDS =		archivers/quazip \
			devel/proj \
			geo/gdal,-main \
			geo/routino \
			x11/qt5/qtwebengine

CONFIGURE_ARGS = 	-DCMAKE_CXX_FLAGS=-DACCEPT_USE_OF_DEPRECATED_PROJ_API_H=1

NO_TEST = 		Yes

.include <bsd.port.mk>
