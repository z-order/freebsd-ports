PORTNAME=	libidn2
PORTVERSION=	2.3.4
PORTREVISION=	2
CATEGORIES=	dns
MASTER_SITES=	GNU/libidn

MAINTAINER=	sunpoet@FreeBSD.org
COMMENT=	Implementation of IDNA2008 internationalized domain names
WWW=		https://www.gnu.org/software/libidn/\#libidn2 \
		https://gitlab.com/libidn/libidn2

LICENSE=	GPLv3
LICENSE_FILE=	${WRKSRC}/COPYING

BUILD_DEPENDS=	help2man:misc/help2man
LIB_DEPENDS=	libunistring.so:devel/libunistring

USES=		charsetfix iconv libtool localbase makeinfo pathfix
LDFLAGS+=	-Wl,--undefined-version

CONFIGURE_ARGS=	--disable-nls \
		--with-libunistring-prefix=${LOCALBASE} \
		--enable-ld-version-script \
		ac_cv_prog_RONN=${TRUE}
GNU_CONFIGURE=	yes
GNU_CONFIGURE_MANPREFIX=${PREFIX}/share
INSTALL_TARGET=	install-strip
TEST_TARGET=	check
USE_LDCONFIG=	yes

INFO=		libidn2

.include <bsd.port.mk>
