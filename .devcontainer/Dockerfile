FROM mcr.microsoft.com/devcontainers/python:3.7
RUN apt-get update && apt-get install -y libpq-dev && rm -rf /var/lib/apt/lists/*
COPY requirements.txt /tmp/requirements.txt
RUN pip install -r /tmp/requirements.txt
ENV PGHOST=postgres PGPORT=5432 PGDATABASE=holo PGUSER=holocleanuser PGPASSWORD=abcd1234
