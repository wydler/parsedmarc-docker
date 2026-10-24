# Reference image
FROM alpine:3.24.3@sha256:be2656061b536c1883c4034790e21d0a09c5aaaf51968b89368a3c0371ea2c9a

# Metadata
LABEL maintainer="Daniel Wydler"
LABEL org.opencontainers.image.authors="Daniel Wydler"
LABEL org.opencontainers.image.description="A Python package and CLI for parsing aggregate and forensic DMARC reports."
LABEL org.opencontainers.image.documentation="https://github.com/wydler/parsedmarc-docker/blob/master/README.md"
LABEL org.opencontainers.image.source="https://github.com/wydler/parsedmarc-docker"
LABEL org.opencontainers.image.title="wydler/parsedmarc-utils"
LABEL org.opencontainers.image.url="https://github.com/wydler/parsedmarc-docker"

# Install minimal runtime dependencies (bash, curl) without caching package index
RUN apk add --no-cache \
        bash \
        curl

# Kibana export file for later import/use inside container
COPY docker/kibana/export.ndjson /tmp/

#ENTRYPOINT [ "/bin/sh", "-c", "--" , "while true; do sleep 30; done;" ]
# Default command: start Bash shell
CMD ["/bin/bash"]
