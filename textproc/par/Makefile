COMMENT=	paragraph reflow for email

VERSION=	1.52
DISTNAME=	Par${VERSION:S/.//}
PKGNAME=	par-${VERSION}
REVISION=	2
CATEGORIES=	textproc
FIX_EXTRACT_PERMISSIONS=Yes

HOMEPAGE=	http://www.nicemice.net/par/

MAINTAINER=	Gregor Best <gbe@unobtanium.de>

# custom
PERMIT_PACKAGE=	Yes

# uses pledge()
WANTLIB += c

SITES=   	${HOMEPAGE}

PATCHFILES=	par_1.52-i18n.3.diff.gz
PATCH_DIST_STRIP=	-p1

ALL_TARGET=

NO_TEST=	Yes

do-configure:
	cd ${WRKSRC}; cp protoMakefile Makefile

do-install:
	${INSTALL_PROGRAM} ${WRKSRC}/par ${PREFIX}/bin
	${INSTALL_MAN} ${WRKSRC}/par.1 ${PREFIX}/man/man1

.include <bsd.port.mk>
