FROM amazonlinux:2

RUN amazon-linux-extras enable php7.4 \
    && yum clean metadata \
    && yum install -y php-cli php-pdo php-fpm php-json php-mbstring php-mysqlnd php-opcache php-xml \
    && yum clean all \
    && rm -rf /var/cache/yum

CMD ["php-fpm", "--nodaemonize"]
