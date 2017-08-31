
# Dockerfile
FROM haproxy:1.7
#copy letsencrypt cert -->  cat fullchain.pem privkey.pem > mysite.fullchain.privkey.pem
COPY mysite.fullchain.privkey.pem /ssl/mysite.fullchain.privkey.pem
RUN groupadd haproxy && useradd -g haproxy haproxy
RUN mkdir -p /var/lib/haproxy/run/haproxy/

COPY haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg
