FROM debian:bullseye-slim
LABEL maintainer "Roald Nefs <info@roaldnefs.com>"

RUN apt-get update && apt-get install -y \
	gcc \
	g++ \
	icmake \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENV HOME /home/icmake
RUN useradd --create-home --home-dir $HOME icmake \
	&& chown -R icmake:icmake $HOME

WORKDIR $HOME
USER icmake

ENTRYPOINT [ "icmake" ]
