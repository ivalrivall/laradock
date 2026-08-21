ARG POSTGRES_VERSION=alpine
FROM postgres:${POSTGRES_VERSION}

RUN apk add --no-cache python3 py3-pip build-base libffi-dev git gawk make zlib-dev openssl-dev clang19 clang19-dev llvm19-dev postgresql-dev lz4-dev

RUN python3 -m venv /opt/venv \
    && . /opt/venv/bin/activate \
    && pip install pgxnclient

ENV PATH="/opt/venv/bin:$PATH"

EXPOSE 5432
CMD ["postgres"]
