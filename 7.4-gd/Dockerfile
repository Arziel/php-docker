# -------------------------------------------------------------
# @Generated Pá čen 19 11:00:02 CEST 2020
#
# Don't edit this file directly!
# For edit use Docker file in root directory & run ./copy.sh
# to regenerate
# -------------------------------------------------------------

FROM arziel/php:7.4



RUN set -e && \
    apt-get update && apt-get install -yqq \
		git \
		zlib1g-dev \
		libpng-dev \
		libwebp-dev \
		libjpeg-dev


RUN docker-php-ext-configure gd \
    	    --enable-gd-native-ttf \
    	    --with-jpeg-dir=/usr/lib/x86_64-linux-gnu \
    	    --with-png-dir=/usr/lib/x86_64-linux-gnu \
    	    --with-freetype-dir=/usr/lib/x86_64-linux-gnu \
    	    --with-webp-dir=/usr/lib/x86_64-linux-gnu \
    	&& docker-php-ext-install gd


RUN rm -rf /var/lib/apt/lists/*
