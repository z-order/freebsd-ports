PORTNAME=	sheerdns
PORTVERSION=	1.04
PORTREVISION=	1
CATEGORIES=	dns
MASTER_SITES=	https://BSDforge.com/projects/source/dns/sheerdns/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Lightweight, simple, and fast master DNS server
WWW=		https://BSDforge.com/projects/dns/sheerdns/

LICENSE=	BSD2CLAUSE
LICENSE_FILE=	${WRKSRC}/LICENSE

DEPRECATED=	Abandonware, upstream dead and last update over 10 years ago
EXPIRATION_DATE=2024-02-29

USES=		gmake tar:xz

WRKSRC=		${WRKDIR}/${PORTNAME}

PLIST_FILES=	share/man/man8/sheerdns.8.gz sbin/sheerdns sbin/sheerdnshash
PORTDOCS=	sheerdns.html sheerdns.ps

OPTIONS_DEFINE=	DOCS

post-install:
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/sbin/sheerdns
	@${STRIP_CMD} ${STAGEDIR}${PREFIX}/sbin/sheerdnshash

post-install-DOCS-on:
	@${MKDIR} ${STAGEDIR}${DOCSDIR}
	(cd ${WRKSRC} && ${INSTALL_DATA} ${PORTDOCS} ${STAGEDIR}${DOCSDIR})

.include <bsd.port.mk>
