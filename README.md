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
WARNING: if you want generated cloudkeeper_pb2_grpc.py file be compiled by python3 then edit importing by add 'from .' before import (see grpc bug  https://github.com/grpc/grpc/issues/9575)
```
python -m grpc_tools.protoc --python_out=. --grpc_python_out=. -I=cloudkeeper-proto/ cloudkeeper-proto/cloudkeeper.proto
```
