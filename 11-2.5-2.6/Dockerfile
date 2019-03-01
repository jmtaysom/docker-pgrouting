FROM mdillon/postgis:11
MAINTAINER Hans Kristian Flaatten <hans@starefossen.com>

ENV PGROUTING_MAJOR 2.6
ENV PGROUTING_VERSION 2.6.1

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
      wget \
      postgresql-$PG_MAJOR-pgrouting && \
    rm -rf /var/lib/apt/lists/*

RUN mkdir -p /docker-entrypoint-initdb.d
COPY ./initdb-pgrouting.sh /docker-entrypoint-initdb.d/routing.sh
