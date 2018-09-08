cmake_minimum_required(VERSION 2.8.11)
project(cparse)

set(cparse_core_src
    shunting-yard.cpp packToken.cpp functions.cpp containers.cpp
)

set(cparse_src
    ${cparse_core_src} builtin-features.cpp
)

add_library(cparse ${cparse_src})
target_include_directories(cparse INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
