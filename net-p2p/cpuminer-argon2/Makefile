# Created by: Christopher Hall
# $FreeBSD$

PORTNAME=	cpuminer-argon2
PORTVERSION=	20160413
CATEGORIES=	net-p2p

MAINTAINER=	hsw@bitmark.com
COMMENT=	CPU Miner using Argon2 password hash

LICENSE=	GPLv2

BUILD_DEPENDS=	${LOCALBASE}/include/curl/curl.h:ftp/curl
LIB_DEPENDS=	libcurl.so:ftp/curl \
		libjansson.so:devel/jansson

USE_GITHUB=	yes
GH_ACCOUNT=	Miouyouyou
GH_PROJECT=	cpuminer-argon2
GH_TAGNAME=	8dc2572

USES=		gmake autoreconf libtool pkgconfig
USE_GCC=	yes
GNU_CONFIGURE=	yes
CONFIGURE_ARGS=	--with-curl=${LOCALBASE}
INSTALL_TARGET=	install-strip

PLIST_FILES=	bin/cpuminer man/man1/cpuminer.1.gz
PORTDOCS=	NEWS README.md

OPTIONS_DEFINE=	DOCS

post-install:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	${INSTALL_DATA} ${PORTDOCS:S,^,${WRKSRC}/,} ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
