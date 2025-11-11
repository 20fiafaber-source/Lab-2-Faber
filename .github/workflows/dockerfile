FROM golang:1.22-alpine AS build

WORKDIR /app

COPY . .

RUN go build -o Hello .

FROM alpine:latest

WORKDIR /root/

COPY --from=build /app/Hello .

CMD ["./Hello"]
