cmake_minimum_required(VERSION 3.14)

project(MyOpenGLTest)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(test main.cpp /home/linuxdocx/.local/include/glad/src/glad.c)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

target_include_directories(test PRIVATE /home/linuxdocx/.local/include)

target_link_libraries(test 
    OpenGL::GL
    glfw
)
