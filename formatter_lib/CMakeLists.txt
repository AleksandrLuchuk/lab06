cmake_minimum_required(VERSION 3.5)
project(formatter)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter STATIC formatter.cpp)
target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

install(TARGETS formatter DESTINATION lib)
install(FILES formatter.h DESTINATION include)
