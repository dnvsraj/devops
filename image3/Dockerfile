FROM alpine:latest
LABEL maintainer="DNVS Rajasekhar <dnvsraj@gmail.com>"
LABEL description="This example Dockerfile installs Apache & PHP."
ENV PHPVERSION 5
RUN apk add --update apache2 php${PHPVERSION}-apache2 php${PHPVERSION} && \
rm -rf /var/cache/apk/* && \
rm -rf /var/www/localhost/htdocs/index.html && \
echo "<?php phpinfo(); ?>" > /var/www/localhost/htdocs/index.php && \
chmod 755 /var/www/localhost/htdocs/index.php
EXPOSE 80/tcp
ENTRYPOINT ["httpd"]
CMD ["-D", "FOREGROUND"]
