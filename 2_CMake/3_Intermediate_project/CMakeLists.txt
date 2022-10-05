cmake_minimum_required(VERSION 3.16)

project(CppProjectTemplate VERSION 1.0.0 LANGUAGES C CXX)

# we would like to use C++ standard for our targets 17
set(CMAKE_CXX_STANDARD 17)

# we require the compiler to fully require on
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD_EXTENSIONS OFF)

option(COMPILE_EXECUTALBE "Hint text: to compile or not to compile" OFF)

# here we define variables to use them later on in the project
set(LIBRARY_NAME Library)
set(EXECUTABLE_NAME Executable)

add_subdirectory(src)

if(COMPILE_EXECUTALBE)
    add_subdirectory(app)
else()
    message("We don't compile, because the logic says so.")
endif()
