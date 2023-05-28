FROM golang:1.16-alpine AS builder

WORKDIR /app

COPY main.go .

RUN go build -o app main.go

FROM scratch

COPY --from=builder /app/app /app/app

EXPOSE 8080

CMD ["/app/app"]
