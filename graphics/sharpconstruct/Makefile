# Created by: Dmitry Marakasov <amdmi3@amdmi3.ru>
# $FreeBSD$

PORTNAME=	sharpconstruct
PORTVERSION=	0.11
PORTREVISION=	10
CATEGORIES=	graphics
MASTER_SITES=	SF/sharp3d/SharpConstruct/${PORTVERSION}

MAINTAINER=	amdmi3@FreeBSD.org
COMMENT=	3D modeller for organic shapes

LIB_DEPENDS=	libgtkglextmm-x11-1.2.so:${PORTSDIR}/x11-toolkits/gtkglextmm \
		libglademm-2.4.so:${PORTSDIR}/devel/libglademm24

USES=		tar:bzip2 gmake pkgconfig
USE_GL=		yes
GNU_CONFIGURE=	yes

ONLY_FOR_ARCHS=	i386 amd64
ONLY_FOR_ARCHS_REASON=	uses SSE

PLIST_FILES=	bin/${PORTNAME} \
		man/man1/${PORTNAME}.1.gz
PORTDATA=	*

post-patch:
	@${REINPLACE_CMD} -e 's|malloc.h|stdlib.h|' ${WRKSRC}/include/Align.hh
	@${REINPLACE_CMD} -e 's|"/sharpconstruct|"|' ${WRKSRC}/src/MainWindow.cc
	@${REINPLACE_CMD} -e 's|/usr/share/sharpconstruct|${DATADIR}|' ${WRKSRC}/src/MainWindow.cc
	@${REINPLACE_CMD} -e '/FileDialog/,/}/ d' ${WRKSRC}/src/MainWindow.cc
	@${REINPLACE_CMD} -e 's|memalign(b,c)|malloc(c)|' ${WRKSRC}/include/Align.hh
	@${FIND} ${WRKSRC} -name Makefile.in -print0 | ${XARGS} -0 \
		${REINPLACE_CMD} -e '/^DEFS / s|$$| -DDATADIR=\\"${DATADIR}\\"|'

.include <bsd.port.mk>
