cmake_minimum_required(VERSION 3.21)
project(threadpool)

set(CMAKE_CXX_STANDARD 11)

# 可以使用中文正常显示
add_compile_options("$<$<CXX_COMPILER_ID:MSVC>:/source-charset:utf-8>")

# 头文件
include_directories(${PROJECT_SOURCE_DIR}/)

# 源文件
file(GLOB SRC_FILES 
    ${PROJECT_SOURCE_DIR}/*.cpp
)

add_executable(${PROJECT_NAME} main.cpp)