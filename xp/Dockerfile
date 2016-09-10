FROM debian:jessie

RUN apt-get update && apt-get install -y \
    xp-runners \
  && rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["/usr/bin/xp"]

CMD ["-v"]