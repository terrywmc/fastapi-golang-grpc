# FastAPI + golang GRPC
A short grpc example

## Prerequisite
- docker-compose
- pipenv
- golang
- protoc [https://grpc.io/docs/protoc-installation/]
- protoc-gen-go [https://grpc.io/docs/languages/go/quickstart/]

## Usage
```sh
docker-compose up
```

## Create protobuf files
```sh
./build_proto_api-gateway.sh
./build_proto_auth-svc.sh
```

## License
MIT