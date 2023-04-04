cmake_minimum_required(VERSION 3.10)

project(restinio-vcpkg-helloworld CXX)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(restinio)

add_subdirectory(hello_world)

