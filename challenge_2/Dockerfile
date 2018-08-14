FROM postgres:10.3-alpine

ENV POSTGRES_DB marketing

COPY dump.sql /docker-entrypoint-initdb.d/
