# $NetBSD: Makefile,v 1.3 2020/05/04 15:36:08 adam Exp $

DISTNAME=	sh-1.13.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	sysutils python
MASTER_SITES=	${MASTER_SITE_PYPI:=s/sh/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://github.com/amoffat/sh
COMMENT=	Python subprocess replacement
LICENSE=	mit

# some test failures, see https://github.com/amoffat/sh/issues/347
TEST_DEPENDS+=	${PYPKGPREFIX}-coverage-[0-9]*:../../devel/py-coverage

USE_LANGUAGES=	# none

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
