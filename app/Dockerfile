FROM golang:1.14.2-alpine

RUN apk update && \
  apk upgrade && \
  apk add --no-cache libc-dev gcc git openssh openssl bash && \
  go get github.com/oxequa/realize && \
  go get -u golang.org/x/lint/golint

WORKDIR /go/src/github.com/bmf-san/go-production-boilerplate/app

COPY go.mod go.sum ./

RUN go mod download

COPY . .

