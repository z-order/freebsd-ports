PORTNAME=	smssend
PORTVERSION=	3.6
CATEGORIES=	misc
MASTER_SITES=	https://BSDforge.com/projects/source/misc/smssend/

MAINTAINER=	ports@FreeBSD.org
COMMENT=	Tool to send an SMS to any GSM
WWW=		https://BSDforge.com/projects/misc/smssend/
LICENSE=	GPLv2

DEPRECATED=	Depends on legacy websites / pages to send SMS
EXPIRATION_DATE=2024-02-29

LIB_DEPENDS=	libskyutils.so:misc/skyutils

USES=		libtool shebangfix tar:txz
SHEBANG_FILES=	bestsms.sh email2smssend
GNU_CONFIGURE=	yes

.include <bsd.port.mk>
