# $NetBSD: Makefile,v 1.10 2017/07/23 19:02:25 nros Exp $

DISTNAME=	zstd-1.3.0
CATEGORIES=	archivers
MASTER_SITES=	${MASTER_SITE_GITHUB:=facebook/}
GITHUB_TAG=	v${PKGVERSION_NOREV}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://www.zstd.net/
COMMENT=	Fast real-time compression algorithm
LICENSE=	modified-bsd

USE_LANGUAGES=		c c++
USE_TOOLS+=		gmake pkg-config
PKGCONFIG_OVERRIDE+=	lib/libzstd.pc.in
MAKE_FLAGS=		MANDIR=${PREFIX}/${PKGMANDIR}/man1
MAKE_FLAGS+=		INSTALL=${INSTALL:Q}

BUILD_TARGET=		allmost
TEST_TARGET=		test

RESTRICTED=		LICENSE-examples does not permit redistribution of the examples
NO_SRC_ON_CDROM=	${RESTRICTED}
NO_SRC_ON_FTP=		${RESTRICTED}

.include "../../archivers/xz/buildlink3.mk"
.include "../../devel/zlib/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
