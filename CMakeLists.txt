cmake_minimum_required(VERSION 3.12)
project(Pulsar)

set(GLFW_INCLUDE_DIR external/glfw/include)
set(GLAD_INCLUDE_DIR external/glad/include)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

include_directories(${GLFW_INCLUDE_DIR} ${GLAD_INCLUDE_DIR})

add_executable(Pulsar main.cpp external/glad/src/glad.c)

target_link_libraries(Pulsar PRIVATE glfw OpenGL::GL)
