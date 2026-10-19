FROM golang:1.13

ENV GOPATH=/go
# Compile sequentially within the executor's 128 MiB memory limit.
ENV GOMAXPROCS=2 GOFLAGS=-p=1
# Keep the driver compatible with Go 1.13 and the GOPATH-based exercises.
RUN git clone --depth 1 --branch v1.14.6 https://github.com/mattn/go-sqlite3.git "$GOPATH/src/github.com/mattn/go-sqlite3" \
    && go install github.com/mattn/go-sqlite3
