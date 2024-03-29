COMMENT=		GNOME desktop sharing server

GNOME_PROJECT=		vino
GNOME_VERSION=		3.22.0
REVISION=		4

CATEGORIES=		net

SITES.p=		http://nerd.hu/distfiles/

DISTFILES+=		${GNOME_PROJECT}-${GNOME_VERSION}${EXTRACT_SUFX}
DISTFILES.p+= 		vino-preferences-20200330.tar.gz

MAINTAINER=		Robert Nagy <robert@openbsd.org>

# GPLv2
PERMIT_PACKAGE=		Yes

WANTLIB += ICE SM X11 Xcomposite Xcursor Xdamage Xext Xfixes Xi
WANTLIB += Xinerama Xrandr Xrender Xtst atk-1.0 atk-bridge-2.0
WANTLIB += avahi-client avahi-common avahi-glib c cairo
WANTLIB += cairo-gobject dbus-1 dbus-glib-1 epoxy expat ffi fontconfig
WANTLIB += freetype gcrypt gdk-3 gdk_pixbuf-2.0 gio-2.0 glib-2.0
WANTLIB += gmodule-2.0 gmp gnutls gobject-2.0 gpg-error graphite2
WANTLIB += gtk-3 harfbuzz hogweed iconv intl jpeg
WANTLIB += m nettle notify p11-kit pango-1.0 pangocairo-1.0 pangoft2-1.0
WANTLIB += pcre2-8 pixman-1 png pthread secret-1 tasn1
WANTLIB += telepathy-glib xcb xcb-render xcb-shm z
WANTLIB += fribidi idn2 unistring ${COMPILER_LIBCXX} execinfo
WANTLIB += Xau Xdmcp brotlidec brotlienc zstd

MODULES=		devel/dconf \
			x11/gnome

MODGNOME_TOOLS=		desktop-file-utils

LIB_DEPENDS=		devel/libnotify \
			net/avahi,-glib \
			net/telepathy/telepathy-glib \
			security/gnutls \
			x11/gnome/libsecret \
			x11/gtk+3

CONFIGURE_STYLE=	gnu

MODGNOME_CPPFLAGS=	-I${X11BASE}/include

FAKE_FLAGS=		sysconfdir=${PREFIX}/share/examples/vino

post-build:
	cd ${WRKDIR}/vino-preferences && ${MAKE}

post-install:
	cd ${WRKDIR}/vino-preferences && \
		${MAKE} PREFIX=${TRUEPREFIX} install

.include <bsd.port.mk>
