# Created by: Jyun-Yan You <jyyou@cs.nctu.edu.tw>
# $FreeBSD$

PORTNAME=	innate
PORTVERSION=	2013.02.21
CATEGORIES=	www rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Powerful web-framework wrapper for Rack

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/COPYING

RUN_DEPENDS=	rubygem-rack15>=1.5.2:${PORTSDIR}/www/rubygem-rack15

USE_RUBY=	yes
USE_RUBYGEMS=	yes
RUBYGEM_AUTOPLIST=	yes
SHEBANG_FILES=	.load_gemset
USES=		shebangfix

.include <bsd.port.mk>
