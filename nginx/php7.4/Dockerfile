#
# Copyright (c) 2024 Xavier Delpirou
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in all
# copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
# SOFTWARE.
#

FROM alpine:latest

LABEL author="Xavier Delpirou" maintainer="administrator@reviax.fr"

RUN apk --update --no-cache add wget bash curl ca-certificates nginx iproute2
RUN apk add php7 php7-fpm php7-mcrypt php7-soap php7-openssl php7-gmp php7-pdo_odbc php7-json php7-dom php7-pdo php7-zip php7-mysqli php7-sqlite3 php7-apcu php7-pdo_pgsql php7-bcmath php7-gd php7-odbc php7-pdo_mysql php7-pdo_sqlite php7-gettext php7-pgsql php7-xml php7-xmlreader php7-xmlwriter php7-xmlrpc php7-xsl php7-bz2 php7-iconv php7-pdo_dblib php7-curl php7-ctype php7-phar php7-fileinfo php7-mbstring php7-tokenizer php7-session php7-sodium php7-pecl-yaml php7-pecl-imagick php7-pecl-imagick-dev php7-ftp

USER container
ENV  USER container
ENV HOME /home/container

WORKDIR /home/container

COPY ./start.sh /start.sh
COPY ./../entrypoint.sh /entrypoint.sh

CMD ["/bin/ash", "/entrypoint.sh"]
