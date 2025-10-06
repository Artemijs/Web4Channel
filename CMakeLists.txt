cmake_minimum_required(VERSION 3.10)

project(GL_LIB_TEST)

set(GLAD C:/Dev/glad/)
set(GLFW C:/Dev/glfw/)

add_executable(${PROJECT_NAME} Main.cpp ${GLAD}/src/glad.c)

find_package(OpenGL REQUIRED)

#additional h files
include_directories(${GLAD}include/)

#										library shit
#lib h files
target_include_directories(${PROJECT_NAME} PRIVATE ${GLFW})
#lib .lib files
target_link_libraries(${PROJECT_NAME} PRIVATE ${GLFW}lib/glfw3.lib)
