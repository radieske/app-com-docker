FROM golang:1.25.1-alpine3.22 AS builder
WORKDIR /app
COPY app.go .
RUN go mod init main && \
  CGO_ENABLED=0 go build

FROM scratch
EXPOSE 80
COPY --from=builder /app/main /go/main
CMD ["/go/main"]