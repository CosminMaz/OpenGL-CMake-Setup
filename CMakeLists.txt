cmake_minimum_required(VERSION 3.31)
project(LearnOpenGL)

set(CMAKE_CXX_STANDARD 26)

# Add dependencies from third-party folder
add_subdirectory(third-party/glfw)
add_subdirectory(third-party/glad)

# Find OpenGL
find_package(OpenGL REQUIRED)

# Create main app
add_executable(LearnOpenGL main.cpp)

# Link libraries
target_link_libraries(LearnOpenGL PRIVATE glfw glad OpenGL::GL)

# Let CLion and CMake know where to find headers
target_include_directories(LearnOpenGL PRIVATE
        third-party/glad/include
        third-party/glfw/include
)
