FROM node
MAINTAINER George Angelopoulos

RUN git clone https://github.com/Upload/Up1

WORKDIR Up1
RUN cp server/server.conf.example server/server.conf
RUN cp client/config.js.example client/config.js

WORKDIR server
RUN npm install

EXPOSE 80

CMD node server.js
