cmake_minimum_required(VERSION 3.0)

project(nbsparser)

set(CMAKE_C_STANDARD 17)
set(CMAKE_BUILD_TYPE Debug)

file(GLOB_RECURSE SRC_FILES_DIR
    ${PROJECT_SOURCE_DIR}/src/*.c
)

include_directories(
    ${CMAKE_SOURCE_DIR}/include
)

add_library(nbsparser STATIC ${SRC_FILES_DIR})

set_target_properties(nbsparser PROPERTIES OUTPUT_NAME "nbsparser")
