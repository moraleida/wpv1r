FROM 10up/wp-php-fpm-dev:7.4

ARG CALLING_USER=www-data
ARG CALLING_UID=33

LABEL "com.10up.wp-local-docker"="user-image"

USER root

RUN useradd ${CALLING_USER} -u ${CALLING_UID}
RUN mkdir -p /run/php-fpm
RUN chown ${CALLING_USER} /run/php-fpm
RUN chown ${CALLING_USER} /var/log/php-fpm
RUN touch /usr/local/etc/msmtprc && chown ${CALLING_USER} $_

USER ${CALLING_USER}
