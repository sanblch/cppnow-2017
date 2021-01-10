cmake_minimum_required(VERSION 3.8)

project(using)

find_package(Clang)
find_package(LLVM)

add_executable(${PROJECT_NAME}
  ${PROJECT_NAME}.cpp)

target_include_directories(${PROJECT_NAME} PRIVATE
  ${LLVM_INCLUDE_DIR})

target_link_libraries(${PROJECT_NAME}
	clangFrontendTool
	clangRewriteFrontend
	clangDynamicASTMatchers
	clangTooling
	clangFrontend
	clangToolingCore
	clangASTMatchers
	clangParse
	clangDriver
	clangSerialization
	clangRewrite
	clangSema
	clangEdit
	clangAnalysis
	clangAST
	clangLex
	clangBasic)