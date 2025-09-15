FROM node:20
ENV DB_HOST=mysql
EXPOSE 8080
RUN groupadd -r expense && useradd -r expense -g expense \
    && mkdir /opt/server \
    && chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
RUN npm install
USER expense
CMD [ "node","index.js" ]