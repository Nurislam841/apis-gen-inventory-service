# Generated Inventory Service (Go + gRPC + Protobuf)

## Overview

This project represents a **generated gRPC Inventory Service** implemented in **Go**.
It is based on **Protocol Buffers (proto definitions)** and contains the generated `.pb.go` files used for gRPC communication.

The service exposes inventory-related operations through gRPC and follows a modular service structure.

---

## Architecture

The system is structured around:

* Protocol Buffers (`.proto` files)
* Generated gRPC server and client code
* Service implementation in Go
* gRPC communication layer

```text
Client
  ↓
gRPC Server (Inventory Service)
  ↓
Business Logic
```

---

## Project Structure

```text
apis-gen-inventory-service-master/
│
├── cmd/
│   └── main.go
│
├── proto/
│   ├── inventory.proto
│   └── generated *.pb.go files
│
├── internal/
│   ├── service/
│   │   └── inventory_service.go
│   └── model/
│       └── product.go
│
├── go.mod
└── go.sum
```

---

## gRPC Contract

The gRPC service is defined in:

```text
proto/inventory.proto
```

The proto file defines:

* Service name
* RPC methods
* Request messages
* Response messages
* Product message structure

Generated Go files (`*.pb.go`) are compiled from this proto definition.

---

## Service Responsibilities

The Inventory Service handles:

* Product management
* Inventory tracking
* gRPC-based request handling
* Structured response delivery

Core domain model:

* `Product`

---

## How to Run

### 1. Clone repository

```bash
git clone <your-repository-url>
cd apis-gen-inventory-service-master
```

### 2. Install dependencies

```bash
go mod tidy
```

### 3. Run the service

```bash
go run cmd/main.go
```

The service starts a gRPC server listening on the configured port (defined in `main.go`).

---

## Technologies Used

* Go
* gRPC
* Protocol Buffers
* Modular service structure

---

## Key Concepts Demonstrated

* gRPC server implementation in Go
* Protobuf contract definition
* Code generation from `.proto`
* Structured service layering
* RPC-based microservice communication

---

## Educational Purpose

This project demonstrates:

* Building a gRPC-based service
* Defining contracts with Protocol Buffers
* Generating strongly-typed Go code
* Implementing RPC handlers
* Structuring backend services for microservice environments
