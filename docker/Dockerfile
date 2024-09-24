FROM httpd:2.4-alpine

EXPOSE 8091
COPY docker/httpd.conf /usr/local/apache2/conf
COPY docker/systemdate.sh /usr/local/apache2/cgi-bin/systemdate
COPY package/docker/index.html /usr/local/apache2/htdocs/