sleuth-echo-example
===================

An echo server and client using [github.com/ursiform/sleuth: A Go library for master-less peer-to-peer autodiscovery and RPC between HTTP services](https://github.com/ursiform/sleuth).

This is just a copy of [Examples (1)](https://github.com/ursiform/sleuth#examples).

## Prerequisite

Install and setup golang  [Getting Started - The Go Programming Language](https://golang.org/doc/install)

## Setup

Install libzmq 4.x library and header files.

On Ubuntu 16.04, use the following command.

```
sudo apt install -y libzmq3-dev
```

On CentOS 7, use the following command.

```
sudo yum install -y zeromq-devel
```

Install sleuth.

```
go get -u github.com/ursiform/sleuth
```


## Try echo server and client

Run the echo server.

```
go get -d github.com/hnakamur/sleuth-echo-example
(cd $GOPATH/sleuth-echo-example/echo-server && go run main.go &)
```

Run the echo client and see "It works." is printed.

```
$ (cd $GOPATH/sleuth-echo-example/echo-client && go run main.go)
It works.
```

Try the echo-service with curl.

```
$ curl -s -d Hello 127.0.0.1:9873/echo-service/
Hello
```
