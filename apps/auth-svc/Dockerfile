FROM golang:1.19-alpine AS build

WORKDIR /app

COPY go.mod .
COPY go.sum .
RUN go mod download

COPY . .

RUN go build -o ./main-app .

## Deploy
FROM alpine:3.9 

WORKDIR /

COPY --from=build /app/main-app /main-app

EXPOSE 8080

ENTRYPOINT ["/main-app", "-port", "8080"]
