# Created by: Steve Wills <swills@FreeBSD.org>
# $FreeBSD$

PORTNAME=	rack-openid
PORTVERSION=	1.4.2
PORTREVISION=	2
CATEGORIES=	www rubygems
MASTER_SITES=	RG

MAINTAINER=	ruby@FreeBSD.org
COMMENT=	Provides a more HTTPish API around the ruby-openid library

LICENSE=	MIT

RUN_DEPENDS=	rubygem-rack16>=1.1.0:${PORTSDIR}/www/rubygem-rack16 \
		rubygem-ruby-openid>=2.1.8:${PORTSDIR}/net/rubygem-ruby-openid

NO_ARCH=	yes
USE_RUBY=	yes
USE_RUBYGEMS=	yes
RUBYGEM_AUTOPLIST=	yes

.include <bsd.port.mk>
