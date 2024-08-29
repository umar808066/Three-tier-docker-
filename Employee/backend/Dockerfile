FROM golang:1.20 AS builder
WORKDIR /backend
COPY go.mod go.sum ./
RUN go mod download
COPY ./controller /usr/local/go/src/employees
COPY ./model /usr/local/go/src/employees
COPY ./repository /usr/local/go/src/employees
COPY ./service /usr/local/go/src/employees
RUN go build -o main /backend

FROM ubuntu:latest
WORKDIR /root/
COPY --from=builder /usr/local/go/src/employees/main .
EXPOSE 5432 8080

CMD ["./main"]


