cmake_minimum_required(VERSION 3.20)

# Project configuration
project(app
        VERSION 1.0.0
        DESCRIPTION "Example Application"
        LANGUAGES C CXX
)

# Set C++23 standard
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Static runtime linking for all configurations
set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")

add_executable(app
    src/main.cpp
)
