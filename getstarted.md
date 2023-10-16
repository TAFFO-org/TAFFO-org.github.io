---
layout: page
title: Getting Started
subtitle: How to install and use TAFFO
---

Taffo currently ships as 5 LLVM plugins, each one of them containing one LLVM optimization or analysis pass:

 - TaffoInitializer (Initialization pass)
 - TaffoVRA (Value Range Analysis pass)
 - TaffoDTA (Data Type Allocation pass)
 - LLVMFloatToFixed (Conversion pass)
 - LLVMErrorPropagator (Error Propagation pass of the Feedback Estimator)

To execute TAFFO, a simple frontend is provided named `taffo`, which can be substituted to `clang` in order to compile or link executables.
Behind the scenes, it uses the LLVM `opt` tool to load one pass at a time and run it on LLVM IR source files.

Up-to-date instructions to set up TAFFO are always available on the [GitHub repository](https://github.com/TAFFO-org/TAFFO).

<div class="centered">
    <a class="btn btn-primary btn-lg get-started-btn" href="https://github.com/TAFFO-org/TAFFO">Go to TAFFO's GitHub repository</a>
</div>
