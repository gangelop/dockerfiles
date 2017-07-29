FROM node
MAINTAINER George Angelopoulos

RUN git clone https://github.com/Upload/Up1

WORKDIR Up1/server
RUN npm install

EXPOSE 80

CMD node server.js
