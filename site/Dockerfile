FROM node:7.5.0-alpine
# http://bitjudo.com/blog/2014/03/13/building-efficient-dockerfiles-node-dot-js/
ADD package.json /tmp/package.json
RUN cd /tmp && npm install
RUN mkdir -p /opt/app && cp -a /tmp/node_modules /opt/app/

WORKDIR /opt/app/

COPY . /opt/app/

EXPOSE 8002

CMD ["node_modules/.bin/http-server", "public", "-p 8002"]
