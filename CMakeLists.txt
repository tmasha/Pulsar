option(GLFW_BUILD_EXAMPLES OFF)
option(GLFW_BUILD_DOCS OFF)
option(GLFW_BUILD_TESTS OFF)

cmake_minimum_required(VERSION 2.6)
project(Pulsar)

add_subdirectory(external/glfw)
add_subdirectory(external/glad)
add_subdirectory(external/glm)

find_package(OpenGL REQUIRED)

include_directories(
  external/glfw/include
  external/glad/include
  external/glm
)

if(COMMAND cmake_policy)
  cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

add_executable(main main.cpp)
target_link_libraries(main PRIVATE glfw glad ${OPENGL_LIBRARY})
