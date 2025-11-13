cmake_minimum_required(VERSION 3.26)

set(PROJECT_NAME AnimationSystem)

project(${PROJECT_NAME} CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# project files
file(GLOB_RECURSE SOURCES
    "source/*.cpp"
    "source/*.h"
)

add_executable(${PROJECT_NAME} ${SOURCES})

set_target_properties(${PROJECT_NAME} PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin/
)
