cmake_minimum_required(VERSION 3.21)
project(github_actions_v3)
set(CMAKE_CXX_STANDARD 14)

enable_testing()

add_executable(tests.exe tests/test.cpp tests/catch.hpp)

add_test(FirstTest tests.exe)

set_tests_properties(FirstTest PROPERTIES
PASS_REGULAR_EXPRESSION "Tree works correctly"
FAIL_REGULAR_EXPRESSION "Tree works incorrectly")

add_executable(mainFunc.exe src/main.cpp)