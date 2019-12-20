FROM alpine:latest
LABEL maintainer "Roald Nefs <info@roaldnefs.com>"

RUN apk --no-cache add valgrind

ENV HOME /home/valgrind
RUN adduser -h $HOME -D valgrind \
	&& chown -R valgrind:valgrind $HOME

WORKDIR $HOME
USER valgrind

ENTRYPOINT [ "valgrind" ]

