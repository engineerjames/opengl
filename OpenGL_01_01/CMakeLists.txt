# CMakeList.txt : CMake project for OpenGL_01_01, include source and define
# project specific logic here.
#

# Add source to this project's executable.
set(target OpenGL_01_01)
add_executable (${target} OpenGL_01_01.cpp)
target_link_directories(${target} PRIVATE E:/OpenGL/glfw-3.3.8/build/src/Debug )
target_link_libraries(${target} PRIVATE glfw3 glad)
target_include_directories(${target} PRIVATE E:/OpenGL/glfw-3.3.8/include E:/OpenGL/glad/include)


if(UNIX)
  message("Adding additional Linux-specific libraries")
  target_link_libraries(${target} PRIVATE GL X11 pthread Xrandr Xi dl)
endif()

# TODO: Add tests and install targets if needed.
