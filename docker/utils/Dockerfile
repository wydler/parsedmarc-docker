# Reference image
FROM alpine:3.24.2@sha256:294b683cb724975bec92580e1e685676bd4b50bda910ddb8c51d4cabeaec77e6

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
