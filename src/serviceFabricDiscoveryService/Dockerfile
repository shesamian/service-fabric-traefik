# syntax=docker/dockerfile:1

ARG ARCH
#UNCOMMENT
# FROM golang:1.20 as builder

WORKDIR /tmp/build

ENV CGO_ENABLED=0

COPY . .
RUN go build -o dist/serviceFabricDiscoveryService ./cmd

#UNCOMMENT
# FROM gcr.io/distroless/static

#UNCOMMENT
# COPY --from=builder /tmp/build/dist/serviceFabricDiscoveryService /

ENTRYPOINT ["/serviceFabricDiscoveryService"]
