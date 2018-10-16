FROM ruby:alpine
LABEL maintainer="Roald Nefs <info@roaldnefs.com>"

RUN apk add --no-cache build-base git && \
    gem install travis --no-rdoc --no-ri && \
    apk del build-base &&\
    mkdir repo

WORKDIR repo
VOLUME ["/repo"]
ENTRYPOINT ["travis"]
