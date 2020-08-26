FROM nginx
LABEL io.openshift.expose-service="8080:http" \
      io.k8s.description="Official nginx tunned for Openshift" \
      io.k8s.display-name="Official nginx" 
RUN sed -i 's/^user/#user/g' /etc/nginx/nginx.conf && \
    sed -i 's/80;/8080;/g' /etc/nginx/conf.d/default.conf && \
    chmod -R g=u /var/log/nginx/ /var/run/ /usr/share/nginx/html /var/cache/nginx/ && \
    chgrp -R 0 /var/log/nginx/ /var/run/ /usr/share/nginx/html /var/cache/nginx/
ONBUILD COPY ./src /usr/share/nginx/html
USER 1001
EXPOSE 8080
