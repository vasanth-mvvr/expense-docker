FROM node:20
ENV DB_HOST=mysql
EXPOSE 8080
RUN mkdir /opt/server
RUN chown expense:expense -R /opt/server
WORKDIR /opt/server
COPY package.json .
COPY *.js .
CMD [ "node","index.js" ]