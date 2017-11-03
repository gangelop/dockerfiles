FROM node
MAINTAINER George Angelopoulos

USER node
WORKDIR /home/node/

RUN git clone https://github.com/Upload/Up1

VOLUME /home/node/Up1/i

WORKDIR Up1
RUN cp server/server.conf.example server/server.conf
RUN cp client/config.js.example client/config.js
RUN sed -i 's/80/8088/' server/server.conf

WORKDIR server
RUN npm install

EXPOSE 8088

CMD node server.js
