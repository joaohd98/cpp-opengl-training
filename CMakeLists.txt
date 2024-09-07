cmake_minimum_required(VERSION 3.29)
project(cpp_opengl_studies)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(cpp_opengl_studies main.cpp)

#find_package(glfw3 3.4 REQUIRED)
#target_link_libraries(cpp_opengl_studies glfw)

include_directories(${CMAKE_SOURCE_DIR}/glad/include)
add_library(glad ${CMAKE_SOURCE_DIR}/glad/src/glad.c)
target_link_libraries(cpp_opengl_studies glad)

#find_package(OpenGL REQUIRED)
#target_link_libraries(cpp_opengl_studies OpenGL::GL)