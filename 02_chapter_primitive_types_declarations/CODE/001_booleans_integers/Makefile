.DEFAULT_GOAL := build

fmt:
	go fmt ./... 
.PHONY: fmt 

lint: fmt
	golint ./...
.PHONY: lint

vet: fmt
	go vet ./...
.PHONY: vet

run: vet
	go run booleans_integers.go
.PHONY: run

build: vet
	go build booleans_integers.go
.PHONY: build


