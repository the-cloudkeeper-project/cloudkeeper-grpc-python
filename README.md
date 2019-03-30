## cloudkeeper gRPC generated classes for Python

This repository contains Python classes generated for gRPC communication within the [cloudkeeper](https://github.com/the-cloudkeeper-project/cloudkeeper) project.

## Depends
### protoc (from source)
```
sudo apt-get install -y git autoconf automake libtool curl make g++ unzip
git clone https://github.com/google/protobuf.git
cd protobuf/
./autogen.sh
./configure
make
make check
sudo make install
sudo ldconfig # refresh shared library cache.
protoc -h
```

(see https://github.com/protocolbuffers/protobuf/blob/master/src/README.md for more)

## Compilation
```
python -m grpc_tools.protoc --python_out=. --grpc_python_out=. cloudkeeper.proto -I.
```
