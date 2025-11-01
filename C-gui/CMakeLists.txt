cmake_minimum_required(VERSION 3.10)
project(OpenGLApp C)

# Use Clang as default compiler
set(CMAKE_C_COMPILER "clang")
set(CMAKE_CXX_COMPILER "clang++")

# C standard
set(CMAKE_C_STANDARD 99)

# === Options ===
option(USE_RAYLIB "Build with Raylib" OFF)
option(USE_GLAD "Use GLAD for OpenGL loading" ON)

# === Source Files ===
set(SOURCES src/main.c)

if(USE_GLAD)
    list(APPEND SOURCES "include/glad.c")
    include_directories(include)
endif()

# === Raylib Setup ===
if(USE_RAYLIB)
    find_package(raylib REQUIRED)
    add_executable(OpenGLApp ${SOURCES})
    target_link_libraries(OpenGLApp raylib m pthread dl GL)
else()
    # === Raw OpenGL Setup ===
    find_package(OpenGL REQUIRED)
    find_package(PkgConfig REQUIRED)
    pkg_search_module(GLFW REQUIRED glfw3)

    include_directories(${GLFW_INCLUDE_DIRS})
    link_directories(${GLFW_LIBRARY_DIRS})

    add_executable(OpenGLApp ${SOURCES})
    target_link_libraries(OpenGLApp ${OPENGL_LIBRARIES} ${GLFW_LIBRARIES} dl m)
endif()