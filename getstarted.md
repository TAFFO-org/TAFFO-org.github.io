---
layout: page
title: Getting Started
subtitle: How to install and use TAFFO
---

TAFFO is based on LLVM 10 and has been tested on Linux (any attempt to compile on Windows, WSL or macOS is at your own risk and peril).

## How to use TAFFO

Taffo currently ships as 5 LLVM plugins, each one of them containing one LLVM optimization or analysis pass:

 - TaffoInitializer (Initialization pass)
 - TaffoVRA (Value Range Analysis pass)
 - TaffoDTA (Data Type Allocation pass)
 - LLVMFloatToFixed (Conversion pass)
 - LLVMErrorPropagator (Error Propagation pass of the Feedback Estimator)

To execute TAFFO, a simple frontend is provided named `taffo`, which can be substituted to `clang` in order to compile or link executables.
Behind the scenes, it uses the LLVM `opt` tool to load one pass at a time and run it on LLVM IR source files.

To use TAFFO it is encouraged to follow these steps:

### Step 1

Create a build directory, compile and install TAFFO.
You can either install TAFFO to the standard location of `/usr/local`, or you can install it to any other location of your choice.
In the latter case you will have to add that location to your PATH.

If you have multiple LLVM versions installed and you want to link TAFFO to a specific one, set the `LLVM_DIR` environment variable to the install prefix of the correct LLVM version beforehand.

Note that at the moment TAFFO supports only LLVM 10, and that LLVM plugins compiled for a given major version of LLVM cannot be loaded by any other version.
If you are building LLVM from sources, you must configure it with `-DLLVM_BUILD_LLVM_DYLIB=ON` and `-DLLVM_LINK_LLVM_DYLIB=ON` for the TAFFO build to succeed.

First, clone the TAFFO sources from [https://github.com/HEAPLab/TAFFO](https://github.com/HEAPLab/TAFFO){:target="_blank"}.

Then, build and install it as follows:

```sh
$ cd /path/to/the/location/of/TAFFO/sources
$ export LLVM_DIR=/usr/lib/llvm-10 # optional
$ mkdir build
$ cd build
$ cmake ..
$ make install
```

### Step 2

Modify your application by inserting annotations on the appropriate variable declarations, then use `taffo` to compile it.

```sh
<editor> program.c
[...]
taffo -O3 -o program-taffo program.c
```

See the [annotation syntax documentation](https://github.com/HEAPLab/TAFFO/blob/master/doc/AnnotationSyntax.md){:target="_blank"} or the examples in [`test/simple-test-cases`](https://github.com/HEAPLab/TAFFO-test/tree/master/simple-test-cases){:target="_blank"} to get an idea on how to write annotations. You can also test TAFFO without adding annotations, which will produce the same results as using `clang` as a compiler/linker instead of `taffo`.

See [`docs/CommandLineReference.md`](https://github.com/HEAPLab/TAFFO/blob/master/doc/CommandLineReference.md){:target="_blank"} for a reference of the command-line options supported by `taffo`.
Note that there is no `taffo++`; C++ source files are autodetected by the file extension instead.
