FROM        --platform=$TARGETOS/$TARGETARCH node:20-alpine

LABEL       author="Felipe" maintainer="felipmoreira8@gmail.com"

RUN         apk update && \
            apk upgrade && \
            adduser -D -h /home/container container

RUN         npm install npm@latest -g

USER        container
ENV         HOME /home/container
WORKDIR     /home/container

COPY        entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]
