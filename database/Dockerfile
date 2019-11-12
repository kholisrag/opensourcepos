FROM alpine
MAINTAINER jekkos
WORKDIR /app

COPY tables.sql .
COPY constraints.sql .
RUN cat tables.sql constraints.sql > database.sql && mkdir -pv /docker-entrypoint-initdb.d/ && cp database.sql /docker-entrypoint-initdb.d/database.sql

VOLUME /docker-entrypoint-initdb.d
