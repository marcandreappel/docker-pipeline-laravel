FROM php:fpm-alpine

LABEL org.label-schema.schema-version="1.0" \
    org.label-schema.vendor="Marc-André Appel <marc-andre@appel.fun>" \
    org.label-schema.name="marcandreappel/docker-pipeline-laravel" \
    org.label-schema.description="A Bitbucket Pipeline PHP Docker Image" \
    org.label-schema.url="https://hub.docker.com/r/marcandreappel/docker-pipeline-laravel" \
    org.label-schema.build-date=$DATE \
    org.label-schema.version="$VERSION" \
    org.label-schema.vcs-url="$URL" \
    org.label-schema.vcs-branch="$BRANCH" \
    org.label-schema.vcs-ref="$COMMIT"

RUN apk update \
	&& apk add git curl libmcrypt-dev mariadb-client libzip-dev zstd-dev autoconf libc-dev gcc make \
	&& docker-php-ext-install pdo_mysql pcntl bcmath zip \
	&& pecl update-channels \
	&& yes | pecl install mcrypt igbinary redis

EXPOSE 9000
CMD ["php-fpm"]
