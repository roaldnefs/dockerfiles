FROM debian:bullseye-slim
LABEL maintainer "Roald Nefs <info@roaldnefs.com>"

RUN apt-get update && apt-get install -y \
	valgrind \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENV HOME /home/valgrind
RUN useradd --create-home --home-dir $HOME valgrind \
	&& chown -R valgrind:valgrind $HOME

WORKDIR $HOME
USER valgrind

ENTRYPOINT [ "valgrind" ]
