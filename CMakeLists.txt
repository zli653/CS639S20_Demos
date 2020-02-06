# Build instructions
# Copy this file into 'LaplacianStencil' directory
# From the 'LaplacianStencil' directory,
# mkdir build && cd build
# cmake .. && make

cmake_minimum_required(VERSION 3.10)
project(LaplacianStencil)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(OpenMP REQUIRED)
foreach(minor_version RANGE 7)
    set(target LaplacianStencil_0_${minor_version})
    add_executable("${target}"
            "${target}/Laplacian.cpp"
            "${target}/Laplacian.h"
            "${target}/main.cpp"
            "${target}/Timer.h")
    target_link_libraries(${target} PUBLIC OpenMP::OpenMP_CXX)
endforeach(minor_version)
