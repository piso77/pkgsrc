# $NetBSD: Makefile,v 1.8 2020/09/01 09:14:54 fcambus Exp $

DISTNAME=	dbip-country-lite-2020-09.mmdb
PKGNAME=	dbip-country-lite-2020.09
CATEGORIES=	net
MASTER_SITES=	https://download.db-ip.com/free/
EXTRACT_SUFX=	.gz

MAINTAINER=	fcambus@NetBSD.org
HOMEPAGE=	https://db-ip.com/db/download/ip-to-country-lite
COMMENT=	DB-IP IP to Country Lite: IPv4/v6 address to country
LICENSE=	cc-by-v4.0

NO_BUILD=	yes

INSTALLATION_DIRS+=	share/dbip

do-install:
	${RUN}${INSTALL_DATA} ${WRKDIR}/${DISTNAME} \
		${DESTDIR}${PREFIX}/share/dbip/dbip-country-lite.mmdb

.include "../../mk/bsd.pkg.mk"
