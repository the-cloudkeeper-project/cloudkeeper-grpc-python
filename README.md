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
**WARNING**: to allow poetry work with generated files add 'from .' before `import cloudkeeper_pb2 as cloudkeeper__pb2` in `cloudkeeper_pb2_grpc.py`
```
python -m grpc_tools.protoc --python_out=. --grpc_python_out=. -I=cloudkeeper-proto/ cloudkeeper-proto/cloudkeeper.proto
```
