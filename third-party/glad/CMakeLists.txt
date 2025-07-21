cmake_minimum_required(VERSION 3.10)

# Build glad as a static library
add_library(glad src/glad.c)

# Set include directory for glad
target_include_directories(glad PUBLIC include)