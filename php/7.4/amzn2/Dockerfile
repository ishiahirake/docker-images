FROM amazonlinux:2

RUN amazon-linux-extras enable php7.4 \
    && yum clean metadata \
    && yum install -y php-cli php-pdo php-fpm php-json php-mbstring php-mysqlnd php-opcache php-xml \
       php-devel php-pear gcc make iputils tar git \
    && pecl install xdebug \
    && sed -i -e "s/^listen.*sock$/listen = 0.0.0.0:9000/g" /etc/php-fpm.d/www.conf \
    && sed -i -e "s/^listen.allowed_clients.*$/;listen.allowed_clients = 127.0.0.1/g" /etc/php-fpm.d/www.conf \
    && yum clean all \
    && rm -rf /var/cache/yum

COPY php.d/* /etc/php.d/

EXPOSE 9000

CMD ["php-fpm", "--nodaemonize"]
