# base image
FROM golang:1.21 as base
WORKDIR /builder
RUN apk add upx

ENV GO111MODULE=on CGO_ENABLED=0

COPY go.mod go.sum /builder/
RUN go mod download

COPY . .
# Profile-guided optimization & Compression
RUN go build -pgo=auto -o /builder/main /builder/main.go
RUN upx -9 /builder/main

# runner image
FROM gcr.io/distroless/static:latest
WORKDIR /app
COPY --from=base /builder/main main

EXPOSE 8080
CMD ["/app/main"]
