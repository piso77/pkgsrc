# $NetBSD: Makefile,v 1.16 2020/08/18 20:12:37 riastradh Exp $

DISTNAME=	nose-1.3.7
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	devel python
MASTER_SITES=	${MASTER_SITE_PYPI:=n/nose/}
EXTRACT_USING=	bsdtar

MAINTAINER=	kamel.derouiche@gmail.com
HOMEPAGE=	https://nose.readthedocs.io/
COMMENT=	Unittest-based testing framework for python
LICENSE=	gnu-lgpl-v2.1

# only needed for a plugin
#DEPENDS+=	${PYPKGPREFIX}-coverage>=3.0:../../devel/py-coverage

USE_LANGUAGES=	# none

SUBST_CLASSES+=		manpath
SUBST_STAGE.manpath=	pre-build
SUBST_FILES.manpath=	setup.py
SUBST_VARS.manpath=	PKGMANDIR

post-extract:
	${MV} ${WRKSRC}/nosetests.1 ${WRKSRC}/nosetests${PYVERSSUFFIX}.1

pre-test:
	${RUN} cd ${WRKSRC} && \
	${PYTHONBIN} setup.py build_tests

do-test:
	${RUN} cd ${WRKSRC}; ${SETENV} ${TEST_ENV} ${PYTHONBIN} selftest.py

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
