
FROM golang:1.21-alpine AS builder

WORKDIR /app

COPY go.mod  ./
RUN go mod download

COPY . .

RUN go build -o service1

FROM alpine:latest

WORKDIR /app

COPY --from=builder /app/service1 .

RUN apk add --no-cache curl

EXPOSE 8001

CMD ["./service1"]
