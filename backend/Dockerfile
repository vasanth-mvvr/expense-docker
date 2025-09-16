FROM node:20.19.5-alpine
ENV DB_HOST=mysql
EXPOSE 8080

RUN addgroup -S expense && adduser -S expense -G expense \
    && mkdir /opt/server \
    && chown expense:expense -R /opt/server

WORKDIR /opt/server

COPY package.json ./
COPY *.js ./

RUN npm install

USER expense

CMD [ "node", "index.js" ]
