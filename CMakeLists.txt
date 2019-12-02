cmake_minimum_required(VERSION 3.15)
project(OpenGL)

set(CMAKE_CXX_STANDARD 11)

set(GLFW_INC_DIR ${PROJECT_SOURCE_DIR}/glfw/include)
#dll库需要添加到Edit Configuration Environment Variables的PATH中，或者放到系统变量PATH中
set(GLFW_LIB_DIR ${PROJECT_SOURCE_DIR}/glfw/lib-mingw/glfw3.dll)

set(GLEW_INC_DIR ${PROJECT_SOURCE_DIR}/glew/include)
set(GLEW_LIB_DIR ${PROJECT_SOURCE_DIR}/glew/lib/Release/Win32/glew32.lib)

set(OPENGL_LIB_DIR ${PROJECT_SOURCE_DIR}/opengl/opengl32.lib)

include_directories(${GLFW_INC_DIR})
include_directories(${GLEW_INC_DIR})

add_executable(OpenGL main.cpp)

target_link_libraries(OpenGL ${GLFW_LIB_DIR} ${GLEW_LIB_DIR} ${OPENGL_LIB_DIR})


