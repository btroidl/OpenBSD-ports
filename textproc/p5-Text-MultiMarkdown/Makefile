COMMENT =	convert MultiMarkdown syntax to (X)HTML

DISTNAME =	Text-MultiMarkdown-1.000035
CATEGORIES =	textproc www
MODULES =	cpan
PKG_ARCH =	*
REVISION =	0

MAINTAINER =	Okan Demirmen <okan@openbsd.org>

# BSD
PERMIT_PACKAGE =	Yes

RUN_DEPENDS =	textproc/p5-Text-Markdown \
		www/p5-HTML-Parser

MAKE_ENV =	TEST_POD=Yes \
		TEST_SPELLING=Yes

TEST_DEPENDS =	devel/p5-Test-Spelling \
		devel/p5-Test-Differences \
		www/p5-HTML-Tidy

.include <bsd.port.mk>
