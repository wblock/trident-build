# $FreeBSD$

PORTNAME=	lumina-mediaplayer
PORTVERSION=	1.4.2
PORTREVISION=	201810080934
CATEGORIES=	deskutils

MAINTAINER=	jt@ixsystems.com
COMMENT=	Streaming media player from the Lumina Desktop

LICENSE=	BSD3CLAUSE

RUN_DEPENDS=	gstreamer1-qt5>=0:multimedia/gstreamer1-qt@qt5 \
		gstreamer1-plugins-gl>=0:graphics/gstreamer1-plugins-gl

OPTIONS_DEFINE=	I18N
OPTIONS_SUB=		yes
OPTIONS_DEFAULT=	I18N
I18N_DESC= Install localization files

.include <bsd.port.options.mk>

MAKE_JOBS_UNSAFE=yes

USES=		qmake qt:5
USE_QT=		core gui widgets network svg \
		buildtools_build x11extras multimedia concurrent
USE_GITHUB=	yes
GH_ACCOUNT=	trueos
GH_PROJECT=	lumina
GH_TAGNAME=	151b24609cb3ff3e3fcdce8aaf3de35c91b6a6c6
WRKSRC_SUBDIR=	src-qt5/desktop-utils/${PORTNAME}

.if${PORT_OPTIONS:MI18N}
USE_QT+= linguist_build
QMAKE_ARGS+=CONFIG+=WITH_I18N
.endif

.include <bsd.port.mk>
