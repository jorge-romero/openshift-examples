FROM centos:8   

RUN yum install -y --nodocs --noplugins httpd && \ 
    yum clean all && \
    chgrp 0 -R /run/httpd /var/log/httpd && \
    chmod g=u -R /run/httpd /var/log/httpd && \
    sed -i 's/Listen 80/Listen 8080/g' /etc/httpd/conf/httpd.conf

USER 1001    
EXPOSE 8080
CMD ["httpd", "-D", "FOREGROUND"]
