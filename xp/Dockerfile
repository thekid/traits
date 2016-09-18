FROM php:latest

RUN apt-get update && apt-get install -y \
    apt-transport-https \
  && rm -rf /var/lib/apt/lists/*

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D401AB61

RUN echo 'deb https://dl.bintray.com/xp-runners/debian jessie main' > /etc/apt/sources.list.d/xp.list

RUN apt-get update && apt-get install -y \
    xp-runners \
  && docker-php-ext-install -j$(nproc) bcmath \
  && rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["/usr/bin/xp"]

CMD ["-v"]