cmake_minimum_required(VERSION 3.31)

project("myFirstGame")

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(${PROJECT_NAME} main.cpp)

add_subdirectory("raylib")

target_link_libraries(${PROJECT_NAME} PRIVATE raylib)