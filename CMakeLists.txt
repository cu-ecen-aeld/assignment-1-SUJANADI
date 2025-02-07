cmake_minimum_required(VERSION 3.10)
project(assignment_autotest C)

enable_testing()

add_subdirectory(assignment-autotest)

add_executable(test_example test/assignment1/test_example.c)
target_link_libraries(test_example PRIVATE unity)

add_test(NAME test_example COMMAND test_example)

