cmake_minimum_required(VERSION 3.15..3.17)
project(
    Chapter6
    VERSION 0.1
    LANGUAGES CXX
)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_GENERATOR Ninja)

find_package(benchmark CONFIG REQUIRED)

add_executable(SmartPtr smartptr.cpp)
target_link_libraries(SmartPtr PRIVATE benchmark::benchmark benchmark::benchmark_main)