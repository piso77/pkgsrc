# $NetBSD: Makefile,v 1.94 2020/08/19 12:40:59 riastradh Exp $

DISTNAME=	pytest-6.0.1
PKGNAME=	${PYPKGPREFIX}-${DISTNAME:S/py//}
CATEGORIES=	devel python
MASTER_SITES=	${MASTER_SITE_PYPI:=p/pytest/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://pytest.org/
COMMENT=	Python testing tool
LICENSE=	mit

DEPENDS+=	${PYPKGPREFIX}-attrs>=17.4.0:../../devel/py-attrs
DEPENDS+=	${PYPKGPREFIX}-expat-[0-9]*:../../textproc/py-expat
DEPENDS+=	${PYPKGPREFIX}-iniconfig-[0-9]*:../../devel/py-iniconfig
DEPENDS+=	${PYPKGPREFIX}-more-itertools>=4.0.0:../../devel/py-more-itertools
DEPENDS+=	${PYPKGPREFIX}-packaging-[0-9]*:../../devel/py-packaging
DEPENDS+=	${PYPKGPREFIX}-pluggy>=0.12:../../devel/py-pluggy
DEPENDS+=	${PYPKGPREFIX}-py>=1.8.2:../../devel/py-py
DEPENDS+=	${PYPKGPREFIX}-toml-[0-9]*:../../textproc/py-toml
BUILD_DEPENDS+=	${PYPKGPREFIX}-setuptools_scm-[0-9]*:../../devel/py-setuptools_scm
TEST_DEPENDS+=	${PYPKGPREFIX}-argcomplete-[0-9]*:../../devel/py-argcomplete
TEST_DEPENDS+=	${PYPKGPREFIX}-hypothesis>=3.56:../../devel/py-hypothesis
TEST_DEPENDS+=	${PYPKGPREFIX}-mock-[0-9]*:../../devel/py-mock
TEST_DEPENDS+=	${PYPKGPREFIX}-nose-[0-9]*:../../devel/py-nose
TEST_DEPENDS+=	${PYPKGPREFIX}-requests-[0-9]*:../../devel/py-requests
TEST_DEPENDS+=	${PYPKGPREFIX}-xmlschema-[0-9]*:../../textproc/py-xmlschema

PYTHON_VERSIONS_INCOMPATIBLE=	27 # since 5.0.0

.include "../../lang/python/pyversion.mk"
.if ${_PYTHON_VERSION:S/none/0/} < 38
DEPENDS+=	${PYPKGPREFIX}-importlib-metadata>=0.12:../../devel/py-importlib-metadata
.endif

USE_LANGUAGES=	# none
USE_TOOLS+=	bash:build

post-install:
	cd ${DESTDIR}${PREFIX}/bin && \
	${MV} py.test py.test-${PYVERSSUFFIX} && \
	${MV} pytest pytest-${PYVERSSUFFIX} || ${TRUE}

do-test:
	cd ${WRKSRC}/testing && pytest-${PYVERSSUFFIX}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
