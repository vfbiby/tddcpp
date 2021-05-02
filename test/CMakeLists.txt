cmake_minimum_required(VERSION 3.0.0)

set(This ExampleTest)

set(Sources ExampleTest.cpp)

add_executable(${This} ${Sources})
target_link_libraries(${This} PUBLIC gtest_main Example)

add_test(
    Name ${This}
    COMMAND ${This}
)