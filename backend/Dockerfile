FROM node:20
ENV DB_HOST=mysql
EXPOSE 8080
RUN addgroup -S expense && adduser -S expense -G expense \
    && mkdir /opt/server \
    && chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
CMD [ "node","index.js" ]