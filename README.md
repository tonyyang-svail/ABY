# Notes on [ABY](http://encrypto.de/papers/DSZ15.pdf) source code

## Changes

I added `.devcontainer/` to contain the building environment so that we can use VSCode Remote-Containers extension to develop and navigate through source code.

## Code structure

- `src/abycore/` contains the core implementation. In particular, [src/abycore/circuit/arithmeticcircuits.h](src/abycore/circuit/arithmeticcircuits.h) and [src/abycore/circuit/booleancircuits.h](src/abycore/circuit/booleancircuits.h) contains a comprehensive list of supported gates.
- `src/examples/` contains example applications. Each application has a `/common` directory that holds the functionality (circuit). The idea is to re-use this circuit even outside of the application. The application's root directory contains a `.cpp` file with a main method that runs the circuit and is used to verify correctness.
