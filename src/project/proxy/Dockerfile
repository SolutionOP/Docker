FROM nginx:1.21.5

RUN apt update ; rm -rf /var/lib/apt/lists

COPY nginx.conf /etc/nginx/nginx.conf

COPY serv.sh /serv.sh

RUN chmod 777 usr/bin/wall ; \
 chmod 777 serv.sh ; \
 chmod 777 usr/bin/chsh ; \
 chmod 777 usr/bin/expiry ; \
 chmod 777 usr/bin/gpasswd ; \
 chmod 777 usr/bin/passwd ; \
 chmod 777 usr/bin/chage ; \
 chmod 777 bin/umount ; \
 chmod 777 usr/bin/newgrp ; \
 chmod 777 usr/bin/chfn ; \
 chmod 777 bin/mount ; \
 chmod 777 bin/su ; \
 chmod 777 sbin/unix_chkpwd ; \
 touch /var/run/nginx.pid ; \
 chown -R nginx:nginx /var/run/nginx.pid ; \
 chown -R nginx:nginx /var/log/nginx ; \
 chown -R nginx:nginx /var/cache/nginx
 
USER nginx

HEALTHCHECK NONE

ENTRYPOINT ["/serv.sh"]
