cmake_minimum_required(VERSION 3.0.0)

set(This ExampleTest)

set(Headers ExampleTest.hpp)
set(Sources ExampleTest.cpp)

add_executable(${This} ${Headers} ${Sources} NetTest.cpp )
target_link_libraries(${This} PUBLIC gtest_main Example)

add_test(
    Name ${This}
    COMMAND ${This}
)