# Created by: Christopher Hall
# $FreeBSD$

PORTNAME=	libargon2
PORTVERSION=	20160413
CATEGORIES=	security devel

MAINTAINER=	hsw@bitmark.com
COMMENT=	Password hash Argon2

LICENSE=	CC0-1.0

USE_GITHUB=	yes
GH_ACCOUNT=	P-H-C
GH_PROJECT=	phc-winner-argon2
GH_TAGNAME=	26c2724

USES=		gmake
#USES=		autoreconf libtool
#GNU_CONFIGURE=	yes
USE_LDCONFIG=	yes
#INSTALL_TARGET=	install-strip

do-install:
	${INSTALL_DATA} ${WRKSRC}/include/argon2.h ${STAGEDIR}${PREFIX}/include
	${INSTALL_LIB} ${WRKSRC}/libargon2.a ${STAGEDIR}${PREFIX}/lib
	${INSTALL_LIB} ${WRKSRC}/libargon2.so ${STAGEDIR}${PREFIX}/lib
	${INSTALL_PROGRAM} ${WRKSRC}/argon2 ${STAGEDIR}${PREFIX}/bin

.include <bsd.port.mk>
