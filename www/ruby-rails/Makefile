# $OpenBSD: Makefile,v 1.32 2012/09/23 16:57:36 jeremy Exp $

COMMENT=	ruby MVC web application framework

VERSION=	3.2.13
DISTNAME=	rails-${VERSION}
CATEGORIES=	www

# MIT License
PERMIT_PACKAGE_CDROM=	Yes

MODULES=	lang/ruby

BUILD_DEPENDS=	${RUN_DEPENDS}
RUN_DEPENDS=	www/ruby-railties,${MODRUBY_FLAVOR}=${VERSION} \
		devel/ruby-activesupport,${MODRUBY_FLAVOR}=${VERSION} \
		databases/ruby-activerecord,${MODRUBY_FLAVOR}=${VERSION} \
		devel/ruby-actionpack,${MODRUBY_FLAVOR}=${VERSION} \
		mail/ruby-actionmailer,${MODRUBY_FLAVOR}=${VERSION} \
		www/ruby-activeresource,${MODRUBY_FLAVOR}=${VERSION} \
		devel/ruby-bundler,${MODRUBY_FLAVOR}>=1.0,<2.0

CONFIGURE_STYLE=ruby gem

post-extract:
	rm -f ${_GEM_DATAFILE}

.include <bsd.port.mk>
