FROM mysql:8.0
# The user is not human only for system 
RUN useradd -r expense
ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1 \
    MYSQL_USER=expense \
    MYSQL_PASSWORD=ExpenseApp@1 \
    MYSQL_DATABASE=transaction 
RUN chown -R expense:expense /var/lib/mysql /var/run/mysqld
COPY /scripts/*.sql /docker-entrypoint-initdb.d/

