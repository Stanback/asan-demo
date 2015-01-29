#
# CMakefile for Asan demo project
#

cmake_minimum_required(VERSION 2.8.3 FATAL_ERROR)

project(asan-demo)

#------------------------------------------------------------------------------
# Compile flags
#------------------------------------------------------------------------------

add_definitions("-O -g -fno-inline -fno-omit-frame-pointer -Wextra -fsanitize=address")

set(CMAKE_CXX_FLAGS "-fsanitize=address")

#------------------------------------------------------------------------------
# Setup executables and linking
#------------------------------------------------------------------------------

add_executable(demo
  src/demo.cpp
)

#target_link_libraries(demo
#)

