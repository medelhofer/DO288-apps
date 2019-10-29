# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.k8s.description="-med- Apache HTTPD Server" \
      io.k8s.display-name="-med- HTTPD" \
      io.openshift.expose-services="8080:http" \
      io.openshift.tags="apache, httpd, med"

RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

RUN chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

USER 1001

