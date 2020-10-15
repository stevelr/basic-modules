.PHONY: all deps codegen build clean doc test

all: deps codegen build

deps:

codegen:
	wapc generate codegen.yaml

build:
	cargo build --target wasm32-unknown-unknown --release
	mkdir -p build
	cp target/wasm32-unknown-unknown/release/*.wasm build/

clean:
	rm -Rf build

doc:
	ll

test: build
	cargo test
