cmake_minimum_required(VERSION 3.19)
project(learningOpenGL)

set(CMAKE_CXX_STANDARD 14)

add_executable(learningOpenGL main.cpp)


#########################################################
# Find OpenGL
#########################################################

find_package(OpenGL REQUIRED)

#########################################################
# Include Subprojects
#########################################################
add_subdirectory("${PROJECT_SOURCE_DIR}/lib/glfw-3.3.2")
include_directories("${PROJECT_SOURCE_DIR}/lib/glfw-3.3.2/include")

target_link_libraries(learningOpenGL OpenGL)
target_link_libraries(learningOpenGL glfw)