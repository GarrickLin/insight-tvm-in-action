cmake_minimum_required(VERSION 3.0.0)
project(insight-tvm-in-action VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 17)

if (NOT DEFINED ENV{LLVM_CONFIG_PATH})
  message(FATAL_ERROR "LLVM_CONFIG_PATH environment variable not defined")
endif()
include(cmake/tvm_config.cmake)
add_subdirectory(tvm)