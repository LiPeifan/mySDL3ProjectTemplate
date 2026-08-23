cmake_minimum_required(VERSION 3.20)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(project_name "SDL3Projects")

project(${project_name} VERSION 1.0
        DESCRIPTION "SDL3 Projects"
        LANGUAGES C CXX)

# set the output directory for built objects.
# This makes sure that the dynamic library goes into the build directory automatically.
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")

# Use vendored libs for SDL3_ttf
set(SDLTTF_VENDORED ON)

add_subdirectory(3rdlibs)
add_subdirectory(projects)