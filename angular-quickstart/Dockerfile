# To build and run with Docker:
#
#  $ docker build -t ng2-quickstart .
#  $ docker run -it --rm -p 3000:3000 -p 3001:3001 ng2-quickstart
#
FROM node:6.5.0

RUN mkdir -p /quickstart /home/nodejs && \
    groupadd -r nodejs && \
    useradd -r -g nodejs -d /home/nodejs -s /sbin/nologin nodejs && \
    chown -R nodejs:nodejs /home/nodejs

WORKDIR /quickstart
#COPY package.json typings.json /quickstart/

COPY . /quickstart

RUN chown -R nodejs:nodejs /quickstart
USER nodejs

RUN npm install

CMD npm start
