# $NetBSD: Makefile,v 1.4 2017/07/23 18:52:03 adam Exp $

DISTNAME=	Unidecode-0.04.21
PKGNAME=	${PYPKGPREFIX}-${DISTNAME}
CATEGORIES=	textproc
MASTER_SITES=	${MASTER_SITE_PYPI:=U/Unidecode/}

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	http://pypi.python.org/pypi/Unidecode/
COMMENT=	ASCII transliterations of Unicode text
LICENSE=	gnu-gpl-v2 # or newer

USE_LANGUAGES=	# none
EGG_NAME=	${DISTNAME:S/0.04/0.4/}

post-install:
	cd ${DESTDIR}${PREFIX}/bin && ${MV} unidecode unidecode${PYVERSSUFFIX} || ${TRUE}

.include "../../lang/python/egg.mk"
.include "../../mk/bsd.pkg.mk"
