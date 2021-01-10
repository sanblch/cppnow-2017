cmake_minimum_required(VERSION 3.8)

project(ast-dump)

find_package(Clang)
find_package(LLVM)

add_executable(ast-dump
  ast-dump.cpp)

target_include_directories(ast-dump PRIVATE
  ${LLVM_INCLUDE_DIR})

target_link_libraries(ast-dump
 libclang) 