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

##Acknowledgements
This work is co-funded by the [EOSC-hub project](http://eosc-hub.eu/) (Horizon 2020) under Grant number 777536.
<img src="https://wiki.eosc-hub.eu/download/attachments/1867786/eu%20logo.jpeg?version=1&modificationDate=1459256840098&api=v2" height="24">
<img src="https://wiki.eosc-hub.eu/download/attachments/18973612/eosc-hub-web.png?version=1&modificationDate=1516099993132&api=v2" height="24">
