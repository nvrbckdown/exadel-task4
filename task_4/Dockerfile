FROM golang:1.16-alpine as builder

WORKDIR /app

COPY . .
RUN go build -o /gogo

FROM alpine
COPY --from=builder gogo .
CMD ["/gogo"]
