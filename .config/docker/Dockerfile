FROM julia:1.10.4-bookworm

#RUN apk add --virtual .package-build-deps --no-cache \
#        git
        

# RUN apk add --virtual .julia-deps-deps --no-cache \
#        aom \
#        binutils \
#        cairo \
#        fdk-aac \
#        fontconfig \
#        freetype \
#        freetype-dev \
#        fribidi \
#        gdk-pixbuf-dev \
#        gnu-libiconv \
#        glib \
#        glib-dev \
#        graphite2 \
#        harfbuzz \
#        lame-libs \
#        libass \
#        libbz2 \
#        libffi \
#        libjpeg \
#        libmount \
#        libogg \
#       libvorbis \
#        libx11 \
#       libxau \
#       libxcb \
#        libxext \
#       libxml2 \
#       libxrender \
#       lzo \
#       pixman \
#       opus \
#       opus-dev \
#       x264-dev \
#       x264-libs \
#       x265-dev \
#        x265-libs 

# Hacks
# RUN ln -s /usr/lib/libffi.so /usr/lib/libffi.so.6
# RUN ln -s /usr/lib/libbz2.so /usr/lib/libbz2.so.1.0
# RUN ln -s /usr/lib/libx264.so /usr/lib/libx264.so.163
# RUN ln -s /usr/lib/libx265.so /usr/lib/libx265.so.199

RUN mkdir /wd

WORKDIR /wd

COPY . /wd

RUN julia /wd/.config/julia/docker-env-setup.jl

