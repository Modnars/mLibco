cmake_minimum_required(VERSION 2.8)
project(mlibco)

set(EXAMPLE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/example)
set(EXAMPLE_EXEC_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/libco)
set(EXAMPLE_EXEC_LIB_DIR ${CMAKE_CURRENT_SOURCE_DIR}libco)

add_subdirectory(libco)
add_subdirectory(example)
