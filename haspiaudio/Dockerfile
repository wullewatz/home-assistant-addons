
ARG BUILD_FROM
FROM $BUILD_FROM

# Copy data
COPY upnp_renderer.c /

# Setup base
RUN \ 
    set -x \ 
    && addgroup root audio \
    && apk add -uU --no-cache \
        alsa-utils \
        alsa-utils-doc \
        alsa-lib \
        alsaconf \
        alsa-ucm-conf \
        alsa-plugins-pulse \
        libupnp-dev \
        libnice-gstreamer \
        gst-plugins-base \
        gst-plugins-ugly \
        gst-plugins-good \
        gst-plugins-bad \
        gst-plugins-good-gtk \
        gst-libav \
        git \
        gstreamer-dev \
        gstreamer-tools \
	 \
	 && apk add -uU --no-cache --purge minidlna \
     \
	 && apk add -uU --no-cache --purge snapcast \
     \
     && apk add  -uU --no-cache --virtual .build-dependencies \
        autoconf \
        automake \
        libtool \
        pkgconf \  
        gcc \
        g++ \
        make \
     \
     && git clone \
        https://github.com/hzeller/gmrender-resurrect.git \
     \
     && mkdir -p /gmrender-resurrect \
	 && cp upnp_renderer.c /gmrender-resurrect/src \
     && cd /gmrender-resurrect \
     && ./autogen.sh \
     && ./configure \
     && automake \
     && make \
     && make install \
	 \
	 && rm -rf /var/cache/apk/* /tmp/*

# Copy data
COPY rootfs /
