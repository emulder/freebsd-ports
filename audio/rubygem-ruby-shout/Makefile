# Created by: Steve Wills <swills@FreeBSD.org>
# $FreeBSD$

PORTNAME=	ruby-shout
PORTVERSION=	2.2.1
PORTREVISION=	1
CATEGORIES=	audio rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Ruby binding to the libshout library

LICENSE=	BSD3CLAUSE

LIB_DEPENDS=	libshout.so:${PORTSDIR}/audio/libshout

CONFIGURE_ARGS=	--with-opt-include="${LOCALBASE}/include"
USE_RUBY=	yes
USE_RUBYGEMS=	yes
RUBYGEM_AUTOPLIST=	yes

.include <bsd.port.mk>
