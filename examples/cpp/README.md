#gRPC in 3 minutes (C++)

## Installation

To install gRPC on your system, follow the instructions to build from source [here](../../INSTALL.md). This also installs the protocol buffer compiler `protoc` (if you don't have it already), and the C++ gRPC plugin for `protoc`.

## Hello C++ gRPC!

Here's how to build and run the C++ implementation of the [Hello World](../protos/helloworld.proto) example used in [Getting started](..).

The example code for this and our other examples lives in the `examples`
directory. Clone this repository to your local machine by running the
following command:


```sh
$ git clone -b $(curl -L http://grpc.io/release) https://github.com/grpc/grpc
```

Change your current directory to examples/cpp/helloworld

```sh
$ cd examples/cpp/helloworld/
```

### Client and server implementations

The client implementation is at [greeter_client.cc](helloworld/greeter_client.cc).

The server implementation is at [greeter_server.cc](helloworld/greeter_server.cc).

### Try it!
Build client and server:
```sh
$ make
```
Run the server, which will listen on port 50051:
```sh
$ ./greeter_server
```
Run the client (in a different terminal):
```sh
$ ./greeter_client
```
If things go smoothly, you will see the "Greeter received: Hello world" in the client side output.

## Tutorial

You can find a more detailed tutorial in [gRPC Basics: C++](cpptutorial.md)
