# $NetBSD: Makefile,v 1.13 2020/08/31 18:08:54 wiz Exp $
#

DISTNAME=	Sys-Syscall-0.25
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	6
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Sys/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://metacpan.org/pod/distribution/Sys-Syscall/lib/Sys/Syscall.pm

COMMENT=	Access system calls that Perl doesn't normally provide access to
LICENSE=	${PERL5_LICENSE}

PERL5_PACKLIST=	auto/Sys/Syscall/.packlist
USE_LANGUAGES=	# none

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
