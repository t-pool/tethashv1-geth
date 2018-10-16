.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/tao-foundation/tethashv1-geth/cmd/swarm
	go build -o bin/geth     github.com/tao-foundation/tethashv1-geth/cmd/geth
	go build -o bin/bootnode github.com/tao-foundation/tethashv1-geth/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/tao-foundation/tethashv1-geth/swarm/...
