cmake_minimum_required(VERSION 3.14)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(hungarian-algorithm)

include_directories(${PROJECT_SOURCE_DIR})

add_library(hungarian-algorithm ./Hungarian.cpp)

add_executable(tests testMain.cpp)
target_link_libraries(tests hungarian-algorithm)

enable_testing()
include(CTest)
add_test(NAME tests COMMAND tests)