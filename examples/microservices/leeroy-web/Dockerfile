FROM harbor.t2cp.com/dev/golang:1.12.9-alpine3.10
COPY web.go .
RUN go build -o /web .

FROM harbor.t2cp.com/dev/alpine:3.10
CMD ["./web"]
COPY --from=builder /web .
