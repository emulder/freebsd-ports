# Created by: Hung-Yi Chen <gaod@hychen.org>
# $FreeBSD$

PORTNAME=	liblbfgs
PORTVERSION=	1.10
PORTREVISION=	1
CATEGORIES=	math
MASTER_SITES=	http://cloud.github.com/downloads/chokkan/liblbfgs/

MAINTAINER=	gaod@hychen.org
COMMENT=	Library of Limited-memory Broyden-Fletcher-Goldfarb-Shanno

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

USES=		libtool
GNU_CONFIGURE=	yes
USE_AUTOTOOLS=	autoconf:env

OPTIONS_DEFINE=	OPTIMIZED DOCS
OPTIMIZED_DESC=	SSE2 optimization routines

.include <bsd.port.options.mk>

# Enable/disable compilation optimizations.
.if ${PORT_OPTIONS:MOPTIMIZED}
CONFIGURE_ARGS+=	--enable-sse2
.endif

PLIST_FILES=	lib/liblbfgs-1.10.so lib/liblbfgs.a \
		lib/liblbfgs.so include/lbfgs.h

PORTDOCS=	README INSTALL COPYING AUTHORS ChangeLog NEWS

post-patch:
.if !${PORT_OPTIONS:MDOCS}
	@${REINPLACE_CMD} -e 's/install-data-am$$//' ${WRKSRC}/Makefile.in
.endif

.include <bsd.port.mk>
