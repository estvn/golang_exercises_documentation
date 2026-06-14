# each operation in this file is called a "target"
# Defines wich target to run when "make" is executed without arguments
.DEFAULT_GOAL := build

fmt: # this is the name of the target
	go fmt ./... 
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

