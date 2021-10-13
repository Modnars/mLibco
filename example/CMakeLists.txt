cmake_minimum_required(VERSION 2.8)
project(example)

include_directories(${EXAMPLE_EXEC_INCLUDE_DIR} ${EXAMPLE_DIR})
link_directories(${EXAMPLE_EXEC_LIB_DIR})

# Macro for add example target
macro(add_example_target EXAMPLE_TARGET)
    add_executable("example_${EXAMPLE_TARGET}" "example_${EXAMPLE_TARGET}.cc")
    target_link_libraries("example_${EXAMPLE_TARGET}" colib_static pthread dl)
endmacro(add_example_target)

add_example_target(closure)
add_example_target(cond)
add_example_target(copystack)
add_example_target(echocli)
add_example_target(echosvr)
add_example_target(poll)
add_example_target(setenv)
add_example_target(specific)
add_example_target(thread)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR})
