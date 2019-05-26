cmake_minimum_required(VERSION 3.0)

project(ctrl2esc)

add_executable(ctrl2esc ctrl2esc.c)
target_compile_options(ctrl2esc PRIVATE -Wall -Wextra)

install(TARGETS ctrl2esc RUNTIME DESTINATION bin)
