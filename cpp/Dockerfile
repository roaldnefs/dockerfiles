FROM debian:bullseye-slim
LABEL maintainer "Roald Nefs <info@roaldnefs.com>"

RUN apt-get update && apt-get install -y \
	gcc \
	g++ \
	gcc-10 \
	g++-10 \
	valgrind \
	icmake \
	flexc++ \
	--no-install-recommends \
	&& rm -rf /var/lib/apt/lists/*

ENV HOME /home/icmake
RUN useradd --create-home --home-dir $HOME cpp \
	&& chown -R cpp:cpp $HOME

WORKDIR $HOME
USER cpp

ENTRYPOINT [ "bash" ]
