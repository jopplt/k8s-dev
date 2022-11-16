# syntax=docker/dockerfile:1
FROM golang:1.19.3-alpine AS build
WORKDIR /app
COPY go.* ./
RUN go mod download
COPY *.go ./
RUN go build -o /app1

FROM alpine:3.16.3
WORKDIR /
COPY --from=build /app1 /app1
EXPOSE 8000
ENTRYPOINT [ "/app1" ]