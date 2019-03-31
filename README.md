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
WARNING: to generate grpc files in python3 valid format cloudkeeper.proto should be located into at least two sub folders (see https://github.com/grpc/grpc/issues/9575)
```
python -m grpc_tools.protoc --python_out=. --grpc_python_out=. -I=proto/ proto/cloudkeeper-proto/cloudkeeper.proto
```
