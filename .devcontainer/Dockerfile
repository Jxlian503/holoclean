FROM mcr.microsoft.com/devcontainers/python:3.8

RUN apt-get update \
 && apt-get install -y libpq-dev postgresql-client \
 && rm -rf /var/lib/apt/lists/*

# HoloClean-Requirements aus dem Repo (liegt im Repo-Root)
COPY requirements.txt /tmp/requirements.txt
RUN pip install --no-cache-dir -r /tmp/requirements.txt

ENV PGHOST=postgres PGPORT=5432 PGDATABASE=holo PGUSER=holocleanuser PGPASSWORD=abcd1234
