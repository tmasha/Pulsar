cmake_minimum_required(VERSION 3.12)
project(Pulsar)

set(GLFW_DIR external/glfw)
set(GLM_DIR external/glm)
set(GLAD_DIR external/glad)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

add_subdirectory(${GLM_DIR})

include_directories(
    ${GLFW_DIR}/include
    ${GLM_DIR}
    ${GLAD_DIR}
)

add_executable(main main.cpp ${GLAD_DIR}/glad.c)

target_link_libraries(main PRIVATE glfw ${OPENGL_LIBRARY})
