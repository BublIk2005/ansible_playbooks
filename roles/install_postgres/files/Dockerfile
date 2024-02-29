FROM postgres:16.1-alpine3.19

RUN apt-get update && apt-get install -y \
python \
&& rm -rf /var/lib/apt/lists/*

RUN pg_createcluster --start 11 main

ENTRYPOINT [ "tail", "-f", "/dev/null" ]