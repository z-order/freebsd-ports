PORTNAME=	IO-Tty
PORTVERSION=	1.18
CATEGORIES=	devel perl5
MASTER_SITES=	CPAN
PKGNAMEPREFIX=	p5-

MAINTAINER=	perl@FreeBSD.org
COMMENT=	Flexible I/O Perl5 module that allows manipulation of pseudo-TTYs
WWW=		https://metacpan.org/release/IO-Tty

LICENSE=	ART10 GPLv1+
LICENSE_COMB=	dual

USES=		perl5
USE_PERL5=	configure

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/${SITE_ARCH_REL}/auto/IO/Tty/Tty.so

.include <bsd.port.mk>
