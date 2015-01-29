# Address-Sanitizer Demo Project

This a quick example for how to use the address sanitizer to discover
various programming errors in C and C++.

## How is memory allocated?
## What is a memory leak?
## Comparison against Valgrind

https://code.google.com/p/address-sanitizer/wiki/ComparisonOfMemoryTools
http://btorpey.github.io/blog/2014/03/27/using-clangs-address-sanitizer/

## Building on OSX

On OSX, address-sanitizer currently requires a custom build of clang:
  * See https://code.google.com/p/address-sanitizer/wiki/HowToBuild
  * Add compiler-rt and libcxx to llvm's projects/ dir
  * Run cmake with: CC=/your/custom/llvm-build/bin/clang CXX=/your-custom/llvm-build/bin/clang++ cmake ../src_dir/

## Experimenting with the test project

This project includes a CMakeLists.txt file that should let you get
started. Steps:

    git clone https://github.com/Stanback/asan-demo.git
    mkdir build
    cmake ../asan-demo
    make
    ./leak-demo
