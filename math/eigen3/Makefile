# $NetBSD: Makefile,v 1.8 2016/09/13 14:57:39 prlw1 Exp $

DISTNAME=	3.2.9
PKGNAME=	eigen3-${DISTNAME}
CATEGORIES=	math
MASTER_SITES=   http://bitbucket.org/eigen/eigen/get/
DIST_SUBDIR=	eigen3
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://eigen.tuxfamily.org/
COMMENT=	C++ template library for linear algebra
LICENSE=	mpl-2.0

USE_LANGUAGES+= c c++
USE_CMAKE= yes
CMAKE_ARG_PATH= ..
CONFIGURE_DIRS= _build
WRKSRC=		${WRKDIR}/eigen-eigen-dc6cfdf9bcec

PKGCONFIG_OVERRIDE+=    eigen.pc.in

pre-configure:
	${MKDIR} ${WRKSRC}/_build

.include "../../mk/bsd.pkg.mk"
