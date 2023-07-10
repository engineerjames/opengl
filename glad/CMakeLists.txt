set(target glad)

add_library(${target} STATIC glad.c include/glad/glad.h include/KHR/khrplatform.h)
target_include_directories(${target} PUBLIC include)