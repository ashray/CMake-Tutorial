cmake_minimum_required(VERSION 2.6e)
project(CMake_Tutorial)

# The version nmber
set(Tutorial_VERSION_MAJOR 1)
set(Tutorial_VERSION_MINOR 0)

# configure a header file to pass some of the CMake settings to the source code
configure_file("${PROJECT_SOURCE_DIR}/CMake Tutorial Config.h.in"
        "${PROJECT_BINARY_DIR}/CMake Tutorial Config.h")

include_directories("${PROJECT_BINARY_DIR}")

set(SOURCE_FILES main.cpp)
add_executable(CMake_Tutorial ${SOURCE_FILES})