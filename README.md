# hydra-proto

[![License](https://img.shields.io/badge/License-GPL--3.0-blue.svg)](LICENSE)

This repo holds all of the protobuf definitions for messages sent on
IPFS pubsub using a hydra client.

## Compiling

Make sure that you have the protobuf compiler `protoc`. If you do not you can use
the following command to install it:

```
go get -u github.com/golang/protobuf/protoc-gen-go
```

### Go

You can compile the Go classes by running the following:

```
$ mkdir $GOPATH/src/github.com/halonproject/hydra-proto-go
$ protoc -I=. --go_out=$GOPATH/src/github.com/halonproject/hydra-proto-go *.proto
```

If you are in the project root this will put the compiled Go classes into a folder
called `hydra-proto-go`. This can then be used by [hydra-go](https://github.com/halonproject/hydra-go).

### Python

You can compile the python classes by running the following:

```
$ mkdir $GOPATH/src/github.com/halonproject/hydra-proto-py
$ mkdir protoc -I=. --python_out=$GOPATH/src/github.com/halonproject/hydra-proto-py *.proto
```

If you are in the project root this will put the compiled Go classes into a folder
called `hydra-proto-py`. This can then be used by [hydra-python](https://github.com/halonproject/hydra-python).

## LICENSE

GPL-3.0
