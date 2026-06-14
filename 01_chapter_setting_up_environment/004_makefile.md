# STRUCTURE OF A MAKEFILE ARCHIVE

## Structure of a Makefile

```
# each operation in this file is called a "target"
# Defines wich target to run when "make" is executed without arguments
.DEFAULT_GOAL := build

fmt: # this is the name of the target
	go fmt ./... # is the task of the target
.PHONY: fmt # This prevents make from getting confused if there is a file named "fmt" in the directory.

lint: fmt # word after the ":" is the target that must run before this one
	golint ./...
.PHONY: lint

vet: fmt
	go vet ./...
.PHONY: vet

build: vet
	go build hello.go
.PHONY: build
```

## Run the Makefile

- First, the directory must to be a go.mod

execute inside the project carpet:

```
make
```

Example of all:

```
PS C:\Users\User\OneDrive\Desktop\BOOKS_STUDY\GOLANG_IDIOMATIC\chapter_1\001_hello_world> go mod init hello
go: creating new go.mod: module hello
go: to add module requirements and sums:
        go mod tidy
PS C:\Users\User\OneDrive\Desktop\BOOKS_STUDY\GOLANG_IDIOMATIC\chapter_1\001_hello_world> make             
go fmt ./... 
go vet ./...
go build hello.go
PS C:\Users\User\OneDrive\Desktop\BOOKS_STUDY\GOLANG_IDIOMATIC\chapter_1\001_hello_world> 
```

## Run make with params

For example, if you have a target called fmt, can do this:

```
make fmt
```