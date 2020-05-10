# Amazone Linux 2 based PHP 7.4

**This image is intended for development use** as it enables **xdebug**.

## Build

```bash
docker build -t ishiahirake/php:7.4-amzn2 .
```

## Info

The php-fpm will listen on `0.0.0.0:9000`.

### Extensions

This image contains the following extensions:

```text
[PHP Modules]
bz2
calendar
Core
ctype
curl
date
dom
exif
fileinfo
filter
ftp
gettext
hash
iconv
json
libxml
mbstring
mysqli
mysqlnd
openssl
pcntl
pcre
PDO
pdo_mysql
pdo_sqlite
Phar
readline
Reflection
session
SimpleXML
sockets
SPL
sqlite3
standard
tokenizer
xml
xmlreader
xmlwriter
xsl
Zend OPcache
zip
zlib

[Zend Modules]
Xdebug
Zend OPcache
```
