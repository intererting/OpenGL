cmake_minimum_required(VERSION 3.15)
project(OpenGL)

set(CMAKE_CXX_STANDARD 11)

set(GLFW_INC_DIR ${PROJECT_SOURCE_DIR}/glfw/include/GLFW)
set(GLFW_LIB_DIR ${PROJECT_SOURCE_DIR}/glfw/lib-mingw-w64/glfw3.dll)

set(GLEW_INC_DIR ${PROJECT_SOURCE_DIR}/glew/include/GL)
set(GLEW_LIB_DIR ${PROJECT_SOURCE_DIR}/glew/lib/Release/Win32/glew32.lib)

include_directories(${GLFW_INC_DIR})
include_directories(${GLEW_INC_DIR})

add_executable(OpenGL main.cpp)

target_link_libraries(OpenGL ${GLFW_LIB_DIR} ${GLEW_LIB_DIR})


