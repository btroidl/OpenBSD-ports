COMMENT =		Ethiopic Unicode script

TYPEFACE =		abyssinica
V =			2.100
DISTNAME =		AbyssinicaSIL-$V
CATEGORIES =		fonts

HOMEPAGE =		https://software.sil.org/abyssinica/

MAINTAINER =		George Rosamond <george@nycbug.org>

# SIL OFL 1.1
PERMIT_PACKAGE =	Yes

MODULES =		font

SITES =			https://software.sil.org/downloads/r/abyssinica/

NO_BUILD =		Yes
NO_TEST =		Yes

DOCDIR =		${PREFIX}/share/doc/abyssinica

post-install:
	${INSTALL_DATA_DIR} ${DOCDIR}
	${INSTALL_DATA} ${WRKDIST}/{README.txt,OFL.txt} ${DOCDIR}

.include <bsd.port.mk>
