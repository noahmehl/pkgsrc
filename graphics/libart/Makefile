# $NetBSD: Makefile,v 1.7 2014/10/09 14:06:36 wiz Exp $

DISTNAME=		libart_lgpl-2.3.21
PKGNAME=		${DISTNAME:S/_lgpl//}
CATEGORIES=		graphics
MASTER_SITES=		${MASTER_SITE_GNOME:=sources/libart_lgpl/2.3/}
EXTRACT_SUFX=		.tar.bz2

MAINTAINER=		pkgsrc-users@NetBSD.org
HOMEPAGE=		http://www.levien.com/libart/
COMMENT=		High-performance 2D graphics library

GNU_CONFIGURE=		YES
USE_LIBTOOL=		YES
PKGCONFIG_OVERRIDE=	libart-2.0.pc.in
# bmake cannot handle the self-made libtool logic in Makefile.am.
USE_TOOLS+=		gmake
CONFLICTS+=		libart2-[0-9]*

.include "../../mk/bsd.pkg.mk"
