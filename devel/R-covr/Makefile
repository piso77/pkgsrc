# $NetBSD: Makefile,v 1.3 2020/08/01 13:40:43 mef Exp $

R_PKGNAME=	covr
R_PKGVER=	3.5.0
CATEGORIES=	devel

MAINTAINER=	pkgsrc-users@NetBSD.org
COMMENT=	Test Coverage for Packages
LICENSE=	gnu-gpl-v3

#Packages suggested but not available:
#  'rmarkdown', 'htmltools', 'DT', 'rstudioapi', 'xml2', 'memoise',
#  'mockery'

DEPENDS+=	R-crayon>=1.3.4:../../devel/R-crayon
DEPENDS+=	R-withr>=1.0.2:../../devel/R-withr
DEPENDS+=	R-digest>=0.6.20:../../security/R-digest
DEPENDS+=	R-jsonlite>=1.6:../../textproc/R-jsonlite
DEPENDS+=	R-yaml>=2.2.0:../../textproc/R-yaml
DEPENDS+=	R-httr>=1.4.1:../../www/R-httr
DEPENDS+=	R-rex>=0:../../devel/R-rex

TEST_DEPENDS+=	R-memoise-[0-9]*:../../devel/R-memoise
TEST_DEPENDS+=	R-mockery-[0-9]*:../../devel/R-mockery
TEST_DEPENDS+=	R-rstudioapi-[0-9]*:../../math/R-rstudioapi
TEST_DEPENDS+=	R-htmltools-[0-9]*:../../textproc/R-htmltools
TEST_DEPENDS+=	R-rmarkdown-[0-9]*:../../textproc/R-rmarkdown
TEST_DEPENDS+=	R-DT-[0-9]*:../../textproc/R-DT
TEST_DEPENDS+=	R-xml2-[0-9]*:../../textproc/R-xml2

.include "../../math/R/Makefile.extension"
.include "../../mk/bsd.pkg.mk"
