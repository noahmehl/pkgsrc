# $NetBSD: Makefile,v 1.6 2017/07/25 16:12:56 joerg Exp $

DISTNAME=	danielj7-hg-fastimport-d41a42894dfa
PKGNAME=	${PYPKGPREFIX}-hg-fastimport-20170211
PKGREVISION=	1
CATEGORIES=	devel
MASTER_SITES=	-https://bitbucket.org/danielj7/hg-fastimport/get/v20170211.tar.bz2
EXTRACT_SUFX=	.tar.bz2

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://mercurial.selenic.com/wiki/FastImportExtension
COMMENT=	Mercurial extension for importing from a git fast-import stream
LICENSE=	gnu-gpl-v2

DEPENDS+=	${PYPKGPREFIX}-fastimport>=0.9.6nb1:../../devel/py-fastimport
DEPENDS+=	${PYPKGPREFIX}-mercurial-[0-9]*:../../devel/py-mercurial

USE_LANGUAGES=	# none

INSTALLATION_DIRS+=	${PYSITELIB}/hgfastimport share/doc/py-hg-fastimport

PYTHON_VERSIONS_INCOMPATIBLE=	34 35 36 # py-mercurial
PY_PATCHPLIST=			yes

do-build:

do-install:
	${INSTALL_SCRIPT} ${WRKSRC}/hgfastimport/*.py ${DESTDIR}${PREFIX}/${PYSITELIB}/hgfastimport
	${INSTALL_DATA} ${WRKSRC}/README.txt ${DESTDIR}${PREFIX}/share/doc/py-hg-fastimport
	${PY_COMPILE_ALL} ${DESTDIR}${PREFIX}/${PYSITELIB}/hgfastimport

.include "../../lang/python/extension.mk"
.include "../../mk/bsd.pkg.mk"
