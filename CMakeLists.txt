cmake_minimum_required(VERSION 3.24)
project(PhotoGL)

set(CMAKE_CXX_STANDARD 17)

find_package(OpenGL REQUIRED)

include_directories(src)
include_directories(headers)
add_subdirectory(libraries/glfw)

add_executable(PhotoGL src/main.cpp)
target_link_libraries(PhotoGL glfw OpenGL::GL)
