# Marathon Dockerfile
FROM mesos-base

RUN    apt-get -y update \
    && apt-get install -y mesos marathon \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 8080
CMD ["--help"]
ENTRYPOINT ["/usr/bin/marathon"]