# MiniRedis

MiniRedis is a lightweight, multithreaded Redis-like in-memory data structure store written in C++17. It supports basic key-value operations, concurrent client handling using a thread pool, and persistence via Append-Only File (AOF) mechanisms.

## Features

* In-Memory Storage: Fast key-value store.
* Multithreading: Efficient concurrent connections handling using a custom ThreadPool.
* Redis Protocol Parsing: Custom parser for Redis serialization protocol (RESP).
* Persistence: Data safety through Append-Only File (AOF).
* Modern C++: Utilizes C++17 features for clean and efficient code.

## Project Structure

* include/: Header files for the project.
* src/: Source files containing the implementation.
  * main.cpp: Entry point of the application.
  * server/: Networking and concurrency logic (Server, ThreadPool).
  * storage/: Core data structures and persistence logic (Storage, AOF).
  * protocol/: RESP parsing logic (Parser).
* build/: Target directory for the compiled binaries.

## Prerequisites

* CMake 3.10 or higher
* C++17 compatible compiler (GCC, Clang, or MSVC)
* Pthreads (POSIX threads) for concurrency

## Build Instructions

1. Create a build directory:
   mkdir build
   cd build

2. Run CMake:
   cmake ..

3. Build the project:
   make

## Running

After a successful build, the mini-redis executable will be located in the build directory.

./mini-redis
