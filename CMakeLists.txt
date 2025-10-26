cmake_minimum_required(VERSION 3.31)

project("myFirstGame")

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB SRC_FILES "${CMAKE_SOURCE_DIR}/src/*.cpp")

include_directories(
    "${CMAKE_SOURCE_DIR}/include"
)

add_executable(${PROJECT_NAME} ${SRC_FILES})

add_subdirectory("raylib")

target_link_libraries(${PROJECT_NAME} PRIVATE raylib)