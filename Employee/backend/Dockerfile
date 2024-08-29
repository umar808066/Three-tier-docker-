FROM golang:1.20 AS builder
WORKDIR /backend
COPY go.mod go.sum ./
RUN go mod download
COPY ./controller .
COPY ./model .
COPY ./repository .
COPY ./routes .
COPY ./service .

RUN go build -o main .

FROM ubuntu:latest
WORKDIR /root/
COPY --from=builder /backend/main .
EXPOSE 5432 8080

CMD ["./main"]


