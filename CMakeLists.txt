cmake_minimum_required(VERSION 3.10)
project(CPP_Examples)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Add subdirectories
add_subdirectory(basics)
add_subdirectory(generic)
add_subdirectory(lib)
add_subdirectory(poly)

