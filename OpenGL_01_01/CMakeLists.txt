# CMakeList.txt : CMake project for OpenGL_01_01, include source and define
# project specific logic here.
#

set(target glad)
add_library(${target} glad.c)
target_include_directories(${target} PRIVATE E:/OpenGL/glad/include)

# Add source to this project's executable.
set(target OpenGL_01_01)
add_executable (${target} OpenGL_01_01.cpp  "glad.c")
target_link_directories(${target} PRIVATE E:/OpenGL/glfw-3.3.8/build/src/Debug )
target_link_libraries(${target} PRIVATE glfw3 glad)
target_include_directories(${target} PRIVATE E:/OpenGL/glfw-3.3.8/include E:/OpenGL/glad/include)

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET OpenGL_01_01 PROPERTY CXX_STANDARD 20)
endif()

# TODO: Add tests and install targets if needed.
