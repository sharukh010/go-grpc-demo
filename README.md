# Go gRPC Demo

This repository showcases a basic implementation of gRPC in Go, demonstrating the four types of gRPC communication patterns:

* Unary RPC
* Server-side streaming RPC
* Client-side streaming RPC
* Bidirectional streaming RPC

## Project Structure

The project is organized into the following directories:

* **proto/**: Contains the `.proto` files defining the gRPC services and messages.
* **server/**: Implements the gRPC server that handles client requests.
* **client/**: Implements the gRPC client that communicates with the server.

## Prerequisites

Ensure you have the following installed:

* Go (version 1.16 or higher)

* Protocol Buffers Compiler (`protoc`)

* Go plugins for the Protocol Buffers Compiler:

```bash
  go install google.golang.org/protobuf/cmd/protoc-gen-go@latest
  go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@latest
```



Ensure that your `GOPATH/bin` is added to your system's `PATH` to access the installed binaries.

## Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/sharukh010/go-grpc-demo.git
   cd go-grpc-demo
   ```



2. **Generate Go code from `.proto` files:**

   ```bash
   protoc --go_out=. --go-grpc_out=. proto/*.proto
   ```



3. **Install dependencies:**

   ```bash
   go mod tidy
   ```



## Running the Application

1. **Start the gRPC server:**

   ```bash
   go run server/main.go server/bi_stream.go
   ```



2. **In a separate terminal, run the gRPC client:**

   ```bash
   go run client/main.go client/bi_stream.go
   ```



The client will interact with the server using the various gRPC communication patterns implemented.([DEV Community][1])

## Learn More

For a deeper understanding of gRPC in Go, consider exploring the following resources:([gRPC][3])

* [gRPC Basics Tutorial in Go](https://grpc.io/docs/languages/go/basics/)
* [gRPC-Go Examples](https://pkg.go.dev/google.golang.org/grpc/examples)
## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.



