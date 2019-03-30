## cloudkeeper gRPC generated classes for Python

This repository contains Python classes generated for gRPC communication within the [cloudkeeper](https://github.com/the-cloudkeeper-project/cloudkeeper) project.

## Depends
### git submodules
```
git submodule update --init --recursive
```

### Install gRPC:
```
python -m pip install grpcio
```

(see https://github.com/protocolbuffers/protobuf/blob/master/src/README.md for more)

## Compilation:
```
python -m grpc_tools.protoc --python_out=grpc --grpc_python_out=grpc -I=cloudkeeper-proto/ cloudkeeper.proto
```
