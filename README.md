# identity

## Requirements

- [Go](https://golang.org)
- [Protobuf](https://github.com/google/protobuf)
- [gRPC](https://grpc.io)
- [Protoc](https://github.com/google/protobuf#protocol-compiler-installation) - Protobuf protocol compiler (Go, Swagger)
- [Go-swagger](https://github.com/go-swagger/go-swagger) generate Go HTTP server/client from Swagger definition

## Installation

```sh
brew install go
brew install protobuf
go get google.golang.org/grpc
go get -u github.com/golang/protobuf/protoc-gen-go
go get -u github.com/grpc-ecosystem/grpc-gateway/protoc-gen-swagger
brew tap go-swagger/go-swagger
brew install go-swagger
```

## Getting started

1. Modify `pb/identity.proto` - Optional HTTP annotations are defined [here](https://github.com/googleapis/googleapis/blob/master/google/api/http.proto)
2. Run `go generate`
3. Generation scripts are documented in doc.go
4. (Optional) Edit http handlers under restapi/configure_identity.go
5. (Optional) Write gRPC server from generated proto files
6. Run `go run cmd/identity-server/main.go --scheme=http`
