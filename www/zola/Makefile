PORTNAME=	zola
DISTVERSIONPREFIX=	v
DISTVERSION=	0.18.0
PORTREVISION=	1
CATEGORIES=	www

MAINTAINER=	mikael@FreeBSD.org
COMMENT=	Fast static site generator
WWW=		https://www.getzola.org/

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

LIB_DEPENDS=	libonig.so:devel/oniguruma \
		libsass.so:textproc/libsass

USES=		cargo ssl
USE_GITHUB=	yes
GH_ACCOUNT=	getzola

MAKE_ENV=	CARGO_PROFILE_RELEASE_LTO=off

PLIST_FILES=	bin/zola \
		etc/bash_completion.d/zola.bash \
		share/fish/completions/zola.fish \
		share/zsh/site-functions/_zola
PORTDOCS=	*

OPTIONS_DEFINE=	DOCS

post-install:
	${STRIP_CMD} ${STAGEDIR}${PREFIX}/bin/zola
	@${MKDIR} ${STAGEDIR}${PREFIX}/etc/bash_completion.d \
		${STAGEDIR}${PREFIX}/share/fish/completions \
		${STAGEDIR}${PREFIX}/share/zsh/site-functions
	${STAGEDIR}${PREFIX}/bin/zola completion bash > \
		${STAGEDIR}${PREFIX}/etc/bash_completion.d/zola.bash
	${STAGEDIR}${PREFIX}/bin/zola completion fish > \
		${STAGEDIR}${PREFIX}/share/fish/completions/zola.fish
	${STAGEDIR}${PREFIX}/bin/zola completion zsh > \
		${STAGEDIR}${PREFIX}/share/zsh/site-functions/_zola

post-install-DOCS-on:
	@cd ${WRKSRC}/docs && \
		${COPYTREE_SHARE} . ${STAGEDIR}${DOCSDIR}

.include <bsd.port.mk>
