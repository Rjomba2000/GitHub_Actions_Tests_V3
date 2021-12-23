cmake_minimum_required(VERSION 3.21)
project(github_actions_v3)
set(CMAKE_CXX_STANDARD 14)

enable_testing()

add_executable(tests.exe tests/test.cpp tests/catch.hpp)

add_test(FirstTest tests)

add_executable(mainFunc src/main.cpp)