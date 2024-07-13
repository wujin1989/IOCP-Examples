cmake_minimum_required(VERSION 3.16)

project(IOCP-Examples)

if (CMAKE_SIZEOF_VOID_P LESS 8)
	message(FATAL_ERROR "only 64bit supported")
endif()

set(CMAKE_POSITION_INDEPENDENT_CODE ON)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS ON)
set(CMAKE_CXX_STANDARD 20)

include_directories(include)
include_directories(src)

set(SRCS
	src/main.cpp
)

add_executable(IOCP-Examples ${SRCS})