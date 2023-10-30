# proto-go-grpc
proto-project-name


# sinh 

```
cd external/proto
protoc --go_out=. --go_opt=paths=source_relative --go-grpc_out=. --go-grpc_opt=paths=source_relative invoicer.proto
```

# lỗi

- nếu lỗi protoc-gen-go-grpc: program not found or is not executable. tức là khi go install vào ```go env GOPATH``` đang không có trong PATH để có thể thực thi. fix bằng cách ```export PATH="$PATH:$(go env GOPATH)/bin"```

- lỗi ```grpc with mustEmbedUnimplemented***```

```
--go-grpc_out=.
--go-grpc_out=require_unimplemented_servers=false:.
```