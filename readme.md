# Sample gRPC

```sh
brew install protobuf
```

```sh
go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
```

## Generating go files

```sh
protoc --proto_path=proto --go_out=proto --go_opt=paths=source_relative --go-grpc_out=proto --go-grpc_opt=paths=source_relative proto/helloworld.proto
```

## Running the application

### Server

```sh
go run simple/server/server.go
```

### Client

```sh
go run simple/client/client.go
```
